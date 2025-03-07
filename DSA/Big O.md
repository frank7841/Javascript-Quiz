# 🌟 BIG O Notation

Welcome to the world of Data Structures and Algorith
**What is a Data Structure?** It is a way to organise, store and access data
**What is an Algorith?** This is a step by step solution to a proble
**Why Data Structure?** **_To help you become a problem solver_**

## 🛠️ Lets dive in to the big 0

Big O notation helps us to understand **_How long_** an algorithim takes to run and **_How Much_** memory is needed as the amount to data input grows. i.e **_Time_**and **_Space_** complexity.

### 1. O(n)

THe execution time of an algorith grows linearly in proportion to the size of the input data (n)

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
