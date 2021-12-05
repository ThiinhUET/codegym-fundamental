# Câu lệnh lặp

let sum = 0;
const n = 100;
for (let i = 1; i <= n; i++) {
    sum += i;  // sum = sum + i
}

i++ : trả về i trước, sau đó mới tăng i lên 1 đơn vị
++i : tăng i lên 1 đơn vị, sau đó mới trả về i

let sum = 0;
const n = 200;
for (let i = 1; i <= n; ++i) {
    sum += i;  // sum = sum + i
}

for ( let i = 1; ++i < 5; ){
  console.log(i);
}

Khởi tạo i = 1;

1st	
i = 2 ( < 5)

2nd	
i = 3 ( < 5)

3rd	
i = 4 ( < 5)
------------------------------------------------
for ( let i = 1; i++ < 5; ){
  console.log(i); // 5
}

Khởi tạo i = 1;

1st	
i = 1 ( < 5)

2nd	
i = 2 ( < 5)

3rd	
i = 3 ( < 5)

4rd 
i = 4 ( < 5)


<!-- Recommend -->
for (let i = 1; i <= n; ++i) {
    sum += i;  // sum = sum + i
}

for (let i = 1; i <= n; i++) {
    sum += i;  // sum = sum + i
}

-----------------------------------------------------------------------

<!-- Multiple condition -->
for ( let i = 0, j = 10; i <= 10 && j >= 0; j--, i++ ){
  console.log(i,j);
}


-------------------------------------

while (loop-continuation-condition) { 
  statement(s);
}

