# 🌟 BIG O Notation

Welcome to the world of Data Structures and Algorith
**What is a Data Structure?** It is a way to organise, store and access data
**What is an Algorith?** This is a step by step solution to a proble
**Why Data Structure?** **_To help you become a problem solver_**

## 🛠️ Lets dive in to the big 0

Big O notation helps us to understand **_How long_** an algorithim takes to run and **_How Much_** memory is needed as the amount to data input grows. i.e **_Time_** and **_Space_** complexity.

### 1. O(n)

THe execution time of an algorithm grows linearly in proportion to the size of the input data (n)

```javaScript o(n)
const groceryDataBase = ['banana','milk','kales','tomatoes'] //this is our array of groceries
//iterate through the array members to find a specific item
const searchItem =(groceries, groceryItem)=>{
    for(let i = 0; i < groceries.length; i++ ){
        if(groceries[i] === groceryItem){
            console.log(`Found ${groceryItem}`)
        }
    }

    //having two loops dependent on the grocerydata Array
    for(let j = i+1; j < groceries.length; i++ ){
        if(groceries[i] === groceryItem){
            console.log(`Found ${groceryItem}`)
        }
    }//You will never do this.
}
searchItem(groceryDatabase, 'tomatoes')
```

**If the list contains more items, it will take longer to iterate through the array.**
Having two loops dependent on the groceryDataBase Array, we have **_n + n => O(2n)_** This is acurate However for representation we remove the constant (2) and arrive to **_O(n)_**

### 2. O(1) -- favourite

THe execution time of an algorithm remains constant despite inputsize change

```javaScript o(1)
const numbers = [1,2,3,4,5,6] //this is our array of numbers
//get a prticular element from the array
//the position of the element must be known
const getElement =(arr, index) => arr[index]//
    console.log(`Found ${getElement(numbers, 0)}`)

```

This is a **_constant_** time complexity since we aready know the position of the element we are looking for in the array No need to traverse the array.

### 3. O(n^2) -- Expensive One

THe execution time of an algorithm grows quadratically with the size of the input data (n)

```javaScript o(n^2)
const numbers = [1,2,3,4,5,6] //this is our array of numbers
//find pairs whose sume is an elemt of the array
function findPairs(arr, index){
    for(i = 0; i < arr.length; i ++){
        for(j = i+1; j < arr.length; j++ ){
            if(arr[i] + arr[j] === arr[index]){
                console.log(`The pair is :${arr[i]} : ${arr[j]} The sum is ${arr[index]} `)
            }
        }
    }
}
findPairs(numbers, 4);
```

For a nested loop we get our big O as **_O(n^2)_**

If we have a nother loop outside the nested loop for example

```javaScript o(n^2)
const numbers = [1,2,3,4,5,6] //this is our array of numbers
//find pairs whose sume is an elemt of the array
function findPairs(arr, index){
    for(i = 0; i < arr.length; i ++){
        for(j = i+1; j < arr.length; j++ ){
            if(arr[i] + arr[j] === arr[index]){
                console.log(`The pair is :${arr[i]} : ${arr[j]} The sum is ${arr[index]} `)
            }
        }
    }
    for(let q = 0; q < arr.length; q ++ ){
        console.log('-------',q )
    }
}
findPairs(numbers, 4);
```

Our Big O becomes **_O(n^2 + n )_** This is accurate but **_O(n^2)_** is the dominant term thus we discard the non-dominant (n) and remain with our dominant term **_o(n^2)_** as the time complexity

### 4. O(log n)

THe execution time of an algorithm grows lograthimically. It increases slowly as the the size of the input data (n) increases

```javaScript o(log n)
//Look at this array
const numbers = [1,2,3,4,5,6,7,8] //this is our array of numbers
///We are looking for an element 2
// 1. Devide the array in to two and discard the subset without our element
const numbers =[1,2,3,4,]
const numbersB =[1,2,3,4,]//Discard

//2.  Devid arry numberA  in to two untill we find our element while discarding the subset without our element
const numbers = [1,2]
//3. locate number two
const number = [2]
```

Our big on notaion is
log<sub> 2</sub> 8 = ?

###### hint 2 pow what? = 8

log <sub> 2 </sub> 8 = 3
**_O (log n)_**
