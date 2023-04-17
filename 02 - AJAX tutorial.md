## Intro :

- AJAX stands for Asynchronous JavaScript and XML.
- Not a programming language. Rather it is a set of existing technology.
- Helps in fetching data asynchronously without interfering with the current page.
- No page reload/refresh - For example, on a web page when a btn is pressed, a request is sent to the server, server sends the data back and accordingly data is updated on web page.
- Modern websited use JSON instead of XML for data transfer.
- Instead of reloading/requesting the whole page, only a certain part of the page is updated, thus saving network bandwidth.

## How it works :

- AJAX uses XMLHTTPRequest (or xhr) object which is inbuilt in JS.
- Data can be transferred in any format and protocol

```html
<body>
    <button type="button" id="fetchbtn" class="btn btn-primary">Primary</button>
    <button type="button" class="btn btn-secondary">Secondary</button>
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe"
      crossorigin="anonymous"
    ></script>
    <script src="ajax.js"></script>
  </body>
```

```js
let fetchbtn = document.getElementById("fetchbtn")
fetchbtn.addEventListener("click", buttonClickHandler)

function buttonClickHandler() {
  console.log("clicked")
  // Instantiate an xhr object
  const xhr = new XMLHttpRequest()

  // open the object - xhr.open(type of request, type of data, true-sent/receive data asynchronously)
  xhr.open("GET", "nikhil.txt", true)

  // optional - You can write code for spinners/loaders here to show display them until data is fetched
  xhr.onprogress = function () {
    console.log("On progress")
  }

  xhr.onload = function () {
    console.log(this.responseText)
  }

  // send the request
  xhr.send()
}
```

- The nikhil.txt file should exist and contain some data which on calling function will be displayed in console.
