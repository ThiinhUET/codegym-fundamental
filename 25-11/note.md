## Truy xuât tới 1 thẻ HTML :
  ### Thông qua ID:
    let element = document.getElementById("idname");
  
  ### Thông qua tag name:
    let element = document.getElementsByTagName("tagname") //input, h1, h2,..
  
  ### Thông qua class:
    let element = document.getElementByClassName("classname")
  
  ### sử dụng querySelectorAll để tìm theo css selector:
    let element = document.querySelectorAll("css selector");

    link : https://www.w3schools.com/cssref/css_selectors.asp

  ### chỉnh sửa style của element thông qua dom:
    1. Lấy phần tử html bằng 1 trong các phương pháp trên
    2. sử dụng thuộc tính style của đối tượng đó

  ### inserBefore()
    Dùng để thêm 1 node vào đằng trước 1 node con nào đó
      insertBefore(node_insert, node_child)
    
    Trong đó:
      + node_insert là node mà bạn muốn them vào
      + node_child là node mà bạn muốn thêm vào đằng trước nó.
  
  ## Các cách để thêm sự kiện cho 1 thẻ HTML
  
  ### Cách 1: sử dụng hàm addEventListener
    là 1 phương được tích hợp sẵn vào đối tượng html thông qua DOM. Khi dử dụng addEventListener thì mình bổ sung được nhiều hành động tại nhiều thời điểm khác nhau.
        elementObject.addEventListener('eventName', function(e) {
          // do something
        })
      eventName : là tên sự kiện nhưng bỏ đi chữ 'on'
  
  ### Cách 2: gắn sự kiện vào đối tượng DOM
      <!-- HTML -->
      <input type="button" value="click me" id="btn">

      <!-- JS -->
      let myInput = document.getElementById('btn');
      myInput.onclick = function() {
        //do something        
      }
  
  ### Cách 3: gắn trực tiếp trên thẻ HTML

      <!-- HTML -->
      <input type="button" value="click me" id="btn" onclick="myFunction()">

      <!-- JS -->

        function myFunction() {
          // do something
        }