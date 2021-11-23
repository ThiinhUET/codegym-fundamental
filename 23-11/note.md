Nội dung buổi trước:
  1. Biến là gì
  2. Cách khai báo và khởi tạo biến trong javascript,
  3. Các scope trong javascript
      + Function Scope (local scope - Biến địa phương)
      + Global Scope (Biến toàn cục)
      + Block Scope (Chỉ xuất hiện với JS phiên bản ES6 trở đi)
  4. Cách sử dụng var, let, const theo từng scope
  5. Các toán tử trong javascript
      + Các toán tử gán : x = y, x += y (x = x + y), x -= y (x = x - y ), x *= y (x = x * y), x /= y (x = x / y), x %= y (x = x % y)
      + Các toán tử so sánh: == (so sánh không chặt vd: 1 == '1' => True ),
                          === (so sánh chặt vd: 1 === '1' => False ),
                          != ( 1 != '1' => False - không chặt),
                          !== (1 !== '1' => True = so sánh chặt),
                          >, < , >=, <=
      + Các toán tử logic: && - vd (chỉ đúng khi cả 2 cùng đúng) vd: 1 === 1 && 2 === 2 => True , 1 === 3 && 2 === 2 => False
                         || - or (chỉ cần 1 điều kiện đúng sẽ trả về true ) vd: 1 === 1 || 2 === 3 => True
                         !  - not vd !true => False , 
                         
                         let a = api call;
                         if(!a) {
                           //code here
                           alert("cannot call api");
                         }

---------------------------------------------------------------------------------------------------------------
## Biến:
  - Biến là nơi lưu trữ dữ liệu;
  - Từ ES6 trở đi có 3 keyword để khai báo biến trong JS: var, let, const
  
                            let x; Khai báo biến
                            x = 1; Khởi tạo biến
  - Naming Convention: 
        Không đặt ký tự đặc biệt ở đầu hoặc trong biến (Ký tự duy nhất nên có là _)
        không để số ở đầu tên biến, không có space trong tên biến.

## Scope trong javascript;
  - Là gì ? : là một vòng đời của một biến.
  - Các loại scope: Function, Global, Block 
   
   for( var i = 0; i < 10; i++) {
     console.log("inside the loop", i);
   }
   console.log("outside the loop", i)

  - ### Function Scope:
    //code demo

    function local() {
      var number = 1;
      console.log(number); // 1
    }
    console.log(number); // reference error

  Khi khai báo một biến trong một hàm, biến đó chỉ được sử dụng cho hàm đó, không được sử dụng ở ngoài.

  - ### Global scope

    var number = 1;
    function local() {
      console.log(number); // 1
    }
    console.log(number);  // 1

  - ### Block scope
    Chỉ được ra đời khi từ khóa let xuất hiện.
      for( let i = 0; i < 10; i++) {
        console.log("inside the loop", i);
      }
      console.log("outside the loop", i)

  Tất cả các scopes trong js chỉ được tạo ra với function scope, các scope khác không được tạo ra trong các block statement.
    + var sẽ không có scope là block. Nếu var ở trong if, while, for, switch thì nó không tạo ra scope mới. 
    
    if(true) {
      let number = 1;
      let number = 3; // error

      var number_1 = 1;
      var number_1 = 2; //number_1 = 2
    }

    console.log(number) //1

    + var có thể khai báo lại biến. let không cho phép khai báo lại biến.


Ví dụ về let, var:
  for(var i = 0; i < 10; i++){
    setTimeout(function() {
      console.log('count', i);
    }, 3000);
  }

  có 2 cách sử:
    1. Thay "var i" thành "let i"
    2. sử IIFE
      for( var i = 0; i < 10; i++){
        (function(i){
           setTimeout(function() {
            console.log('count', i);
          }, 3000);
        }), (i);   
      }
