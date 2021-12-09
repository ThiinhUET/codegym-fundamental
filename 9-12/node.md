### Array - Mảng
let array = [1,2,3,4,5]

array[0] = 1
array[4] = 5
array[5] // Error : index out of range

### forEach()

array.forEach( function(value, index){
  // Thân loop
})

### Map

let newArr = oldArray.map(function(value, index){
  logic
});

### For ... in
for chỉ để dùng loop qua các object.
for( let i in smth) {
  //code here
}

### For ... of
chỉ xuất hiện từ ES6 trở đi
 duyệt qua Array, String

 for(variable of something){
   // code go here
 }