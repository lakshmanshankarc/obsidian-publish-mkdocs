# Arrays (TS)

1. Arrays are contiguous portion of blocks in the memory
2. Accessed via Index

[https://drive.google.com/file/d/1SX7MZL_zSaySdueaYekdI_vsElv7B3HE/view?usp=drive_web](https://drive.google.com/file/d/1SX7MZL_zSaySdueaYekdI_vsElv7B3HE/view?usp=drive_web)

# Static Arrays

Simplest form of array represented by contiguous blocks of memory

![main.excalidraw.png](main.excalidraw.png)

Memory address refers to the address of values → as u can see that the values are differ exactly by 4  because they are integers and each integer takes up 4 Bytes space Max Size chart below on Typed Arrays

- Advantages
    
    Access Elements at O(1) and efficient use of memory
    
    compaction. Remember the College Days
    
- Disadvantages
    1. Insertion and deletion is not efficient
    2. cannot use small spaces while we need a large portion thus wasting spaces

```cpp
#include <iostream>
using namespace std;
int main () {
  int arr[5] = {1,2,3,4,5};
  cout << arr[0] << "...." << arr[4] << endl;
  // cout << &arr[0] <<"\n"<< &arr[1] << "\n" << &arr[2]; // exactly by 4
  cout << *(arr+0) << "..." << *(arr+4);
  return 0;
}
```

1. static arrays can be accessed via the index.
2. well you can also access via pointer. really the pointers and arrays are similar than u think

# Dynamic Arrays

Dynamic Arrays are also similar to static arrays but they have some advantages like dynamically increase or decrease its size

though it also comes with its own disadvantages as well. In C++ vectors in STL are the common example for dynamic arrays

## How Dynamic Arrays work:

dynamic arrays are also like static arrays but the can increase the size by current size when N-1th element is added we assume that more values are added to this array and increment the size by the current length. you’re right

we cannot increment the instead create new array and copy all the contents to the new array. well this is way more efficient than many other ways

Python List and JavaScript Arrays and C++ Vectors are examples of Dynamic Arr

## Example

![main.excalidraw(1).png](main.excalidraw(1).png)

As we can clearly see that when we add elements closer to the size of arr it will increase the size and copy all the elements to the new array

<aside>
💡 There are other ways also we can use like increase the Size to huge number but that is not efficient as we did before

</aside>

# Array Buffer & Typed Arrays

```tsx
ArrayBuffer -> basket of size (4)
Uint16Array(2KG) watermelon -> we can put 2 Melon on ArrayBuffer
Uint8Array(1KG) Muskmelon -> we can put 4 on current basket
```

[ArrayBuffer - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer)

[TypedArray - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray)

Size chart for typed arrays

Base class for u int<size> Arrays provide efficient way to handle binary data

```tsx
const buffer= new ArrayBuffer(4); // 4 bytes [0,0,0,0]
buffer[1]=23 // ! you cant do this
const oneByte=new Uint8Array(buffer) // create 4 (1 Byte arrays)

for (let i = 0; i < 4; i++) 
    oneByte[i]=2*i;

console.log(oneByte);//Uint8Array(4) [ 0, 2, 4, 6 ]
console.log(buffer); //ArrayBuffer(4) [ 0, 2, 4, 6 ]
```

<aside>
💥 they cannot be directly modified (instead new typed array can be used)

</aside>

> Array Buffer provide fixed binary space for typed arrays like Uint8Array…..
> 

> Provide a way for efficient Bit wise operations
> 

## Typed Arrays

```tsx
// typed arrays
const bigBuffer=new ArrayBuffer(16);
const oneByte = new Uint8Array(bigBuffer) // 16 (we can create 16 oneByteArrays)
const fourByte=new Uint32Array(bigBuffer);
console.log(oneByte.length);// 4 (each one is 4Bytes)
```

Typed Arrays are views → underlying buffer sizes

<aside>
💥 typed → views that modify the array Buffer

</aside>

Think of a interface to modify the Array buffer

<aside>
💡 same array buffer can be shared across two views but it need enough spaces

</aside>

$$
Typed Arrays (Views) => ArrayBuffer(TotalBytes)
$$

# Linear Search

$$
Time Complexity=BigOh(N) 
$$