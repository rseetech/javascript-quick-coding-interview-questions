# Javascript Quick Coding Interview Questions

   > Click :star: if you like the project and follow me on LinkedIn [@RameshKumar](https://www.linkedin.com/in/ramesh-kumar-choudhary/) for more updates.


   ## JavaScript Coding Challenges and Interview Question list available here :-

   >1. Click here for [Javascript Quick Asking Coding Interview Questions](https://github.com/rseetech/javascript-quick-coding-interview-questions) more information.
   >  
   >2. Click here for [Javascript Basics Coding](https://github.com/rseetech/javascript-basics) more information.
   >  
   >3. Click here for [Javascript Coding Challenges](https://github.com/rseetech/javascript-coding-challenges) more information.


   ## React Coding Project and Interview Question list available here :-

   >1. Click here for [React Interview Questions & Answers](https://github.com/rseetech/React-interview-questions) more information.
   >
   >2. Click here for [React Routing Axios Search Counter App Using MUI](https://github.com/rseetech/react-routing-axios-search-counter-app-using-mui) more information.
   >
   >3. Click here for [React Routing Pass data Child to Parent](https://github.com/rseetech/react-router-axios-pass-data-child-to-parent) more information.
   >
   >4. Click here for [React Create Tic Tac Toe Game](https://github.com/rseetech/react-create-tic-tac-toe-game) more information.

### Table of Contents

| No. | Questions                                                                              |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [Array method more using Below Array can be used in all method](#array-method-more-using.-below-array-can-be-used-in-all-method)   |
| 2   | [Consolidate array into single array](#consolidate-array-into-single-array)                   |
| 3   | [Number array Sorting](#number-array-sorting)                   |
| 4   | [Number array sort without sort method](#number-array-sort-without-sort-method)                   |
| 4   | [Concat Array](#concat-array)                   |
| 5   | [Filter : Diffrent diffrent ways to use filter method in javascript](#filter-:-diffrent-diffrent-ways-to-use-filter-method-in-javascript) |
| 6   | [search using keyword from array](#search-using-keyword-from-array) |
| 7   | [Finding if an element exists in the array or not and updating the array](#finding-if-an-element-exists-in-the-array-or-not-and-updating-the-array)                   |
| 8   | [Finding all the occurrences of an elements](#finding-all-the-occurrences-of-an-elements) |

1. ### Array method more using Below Array can be used in all method 
    
        > const name = ["Ramesh", "Suresh", "Rajesh", "Jayesh"];
    
    1. #### The `length` property returns the length (size) of an array: 

        >   let size = name.length;
    
    2. #### The `push()` method adds a new element to an array (at the end):

        >   name.push("Bhavesh"); 
    
    2. #### The `pop()` method removes the last element from an array:

        >   name.pop();

    3. #### The `shift()` method removes the first array element and `shifts` all other elements to a lower index.

        >   name.shift();

    4. #### The `unshift()` method adds a new element to an array (at the beginning), and `unshifts` older elements:

        >   name.unshift("Rakesh");

    5. #### `delete` Array elements can be deleted using the JavaScript operator `delete`
        **Note:** Using delete leaves undefined holes in the array.

        Use `pop()` or `shift()` instead.

        >   delete name[0];

    6. #### The `splice()` method can be used to add new items to an array:
        **Note:** The first parameter (2) defines the position where new elements should be added (spliced in).

        The second parameter (0) defines how many elements should be removed.

        The rest of the parameters `("Rakesh" , "Dinesh")` define the new elements to be added.

        >   name.splice(2, 0, "Rakesh", "Dinesh");

    7. #### The `slice()` method slices out a piece of an array into a new array.
        **Note:** The `slice()` method creates a new array.

        The `slice()` method does not remove any elements from the source array.
            
        >   const citrus = name.slice(1);

    8. #### The `slice()` method can take two arguments like slice(1, 3).

        >   const citrus = name.slice(1, 3);

    9. #### The `sort()` method sorts an array alphabetically:

        >   name.sort();

    10. #### The `reverse()` method reverses the elements in an array.

        >   name.reverse();

   **[⬆ Back to Top](#table-of-contents)**

2. ### Use arr.reduce to print sum

    const arr = [1,2,3,4,5] // use arr.reduce to print sum
    const sum = arr.reduce((a, val) => a + val);
    console.log(sum);

2. ### Consolidate array into single array

    **Example: 1**

            const myArr = [[1,2],[3,4],[5,6]];
            const myArr = [[[1,2][,[[[3,4]]],[5,6]];
            const newArr = myArr.flat();
            console.log(newArr);

            Output: [1,2,3,4,5,6]

    **Without flat() method**

            function flattenArray(arr) {
                let result = [];
                arr.forEach((item) => {
                    if (Array.isArray(item)) {
                    result = result.concat(flattenArray(item));
                    } else {
                    result.push(item);
                    }
                });
                return result;
            }
            const nestedArray = [6, 7, [8], [[9]], [[10, 11]]];
            const flattenedArray = flattenArray(nestedArray);
            console.log(flattenedArray); // Output: [6, 7, 8, 9, 10, 11]
                        
    **Example: 2**
    
            const myArr2 = [[1,2],[[[[3,4]]]],[5,6]];
            const newArr2 = myArr2.flat(4);
            console.log(newArr2);

    **Example: 3**

            const multi_dimensional_array = [['a', 'b', 'c'], ['d', 'e', 'f'], ['g', 'h', 'i']];

            const single_array = multi_dimensional_array.flat();
            console.log(single_array);

            Output: ["a", "b", "c", "d", "e", "f", "g", "h", "i"]

   **[⬆ Back to Top](#table-of-contents)**

3. ### Number array Sorting

    **Example: 1** 

            const points = [20, 12, 1, 5, 25, 10];
            points.sort(function(a, b){return a - b});
            points.sort(function(a, b){return b - a}); // descending

            Output: [1,5,10,12,20,25] 

            **Note:** now points[0] contains the lowest value and 
                    points[points.length-1] contains the highest value

    **Example: 2** Object Array

            const birth = [
                {name:"Ramesh", year:1992},
                {name:"Suresh", year:2001},
                {name:"Bhavesh", year:2002}
            ];
            const sortedlist = birth.sort(function(a, b){return a.year - b.year});

            console.log(sortedlist);

            Output: [
                { name: "Ramesh", year: 1992 }, 
                { name: "Suresh", year: 2001 },
                { name: "Bhavesh", year: 2002 }
            ]
        
   **[⬆ Back to Top](#table-of-contents)**

4. ### Number array sort without sort method

    ** Example: 1 **

    ```
        function Numeric_sort(ar) {
            let i = 0, j;
            while (i < ar.length) {
                j = i + 1;
                while (j < ar.length) {
                    if (ar[j] < ar[i]) {
                        let temp = ar[i];
                        ar[i] = ar[j];
                        ar[j] = temp;
                    }
                    j++;
                }
                i++;
            }
        }
        let arr = [1, 15, 10, 45, 27, 100];
        Numeric_sort(arr);
        console.log(arr);

    ```

    ** Example: 2 **

        ```
            function bubbleSort(arr) {
                const len = arr.length;

                for (let i = 0; i < len - 1; i++) {
                    for (let j = 0; j < len - i - 1; j++) {
                    if (arr[j] > arr[j + 1]) {
                        // Swap elements if they are in the wrong order
                        const temp = arr[j];
                        arr[j] = arr[j + 1];
                        arr[j + 1] = temp;
                    }
                    }
                }
            return arr;
            }
            const arrayToSort = [12, 34, 21, 14, 67, 35, 64, 25];
            const sortedArray = bubbleSort(arrayToSort);
            console.log(sortedArray); // Output: [12, 14, 21, 25, 34, 35, 64, 67]

        ```

    ** Example: 3 **
    
    ```
        function bubbleSort(array) {
            var done = false;
            while (!done) {
                done = true;
                for (var i = 1; i < array.length; i += 1) {
                    if (array[i - 1] > array[i]) {
                    done = false;
                    var tmp = array[i - 1];
                    array[i - 1] = array[i];
                    array[i] = tmp;
                    }
                }
            }
            return array;
        }
        var numbers = [12, 10, 15, 11, 14, 13, 16];
        bubbleSort(numbers);
        console.log(numbers);
        
    ```

   **[⬆ Back to Top](#table-of-contents)**

4. ### Concat Array

    ```
        const arr1 = ["Ramesh", "Suresh"];
        const arr2 = ["Bhavesh", "Vinod"];
        const arr3 = ["Rakesh", "Raj"];

        const res1 = arr1.concat(arr2);
        const res2 = arr1.concat(arr2, arr3);
        
        console.log(res1)
        Output: ["Ramesh", "Suresh", "Bhavesh", "Vinod"]

        console.log(res2)
        Output: ["Ramesh", "Suresh", "Bhavesh", "Vinod", "Rakesh", "Raj"]

    ```

   **[⬆ Back to Top](#table-of-contents)**

5. ### Filter : Diffrent diffrent ways to use filter method in javascript

    **Example: 1**

            var numbers = [5, 4, 12, 3, 16, 8, 11];

            var greaterThanCondition = numbers.filter(function(number) {
                return number > 5;
            });
            const sortedArray = greaterThanCondition.sort((a,b) => a-b);

            console.log(sortedArray);

            Output: [8, 11, 12, 16]

    **Example: 2**

            1. Exp

                const names = ["Ramesh", "Ram", "Raj", "Jayesh"];
                const results = names.filter(name => name.length > 4);

                console.log(results);

                Output: ["Ramesh", "Jayesh"]

            2. Exp

                var res = names.filter(name => name.includes('Ram'))
                console.log(res);

                Output: ["Ramesh", "Ram"]

    **Example: 3**

            let team = [
                {
                    name: "Ramesh",
                    position: "developer"
                },
                {
                    name: "Rakesh",
                    position: "ui designer"
                },
                {
                    name: "Suresh",
                    position: "content manager"
                },
                {
                    name: "Bhavesh",
                    position: "backend engineer"
                },
                {
                    name: "george",
                    position: "developer"
                },
            ];

            let developers = team.filter(member => member.position == "developer")

            console.log(developers)
            Output: [{
                        name: "Ramesh",
                        position: "developer"
                        }, {
                        name: "george",
                        position: "developer"
                    }]
            let nondevelopers = team.filter(member => member.position !== "developer")

            console.log(nondevelopers)
            Output: [{
                    name: "Rakesh",
                    position: "ui designer"
                    }, {
                    name: "Suresh",
                    position: "content manager"
                    }, {
                    name: "Bhavesh",
                    position: "backend engineer"
                }]

    **Example: 3**
    
        function removeDuplicate(arr, p) {
            const unq = {};
            return arr.filter((obj) => {
                const value = obj[p];
                
                if(!unq[value]){
                    unq[value] = true;
                return true;
                }
                return false;
            })
        }

        const person = [
        { id: 1, name: "ramesh" },
        { id: 2, name: "suresh" },
        { id: 2, name: "rakesh" },
        { id: 1, name: "ramesh" },
        ];

        const unqperson = removeDuplicate(person, 'id');
        console.log(unqperson);

    **Example: 4**

        var input = [
            { brand: "apple", model: "iphone12", price: 70000 },
            { brand: "apple", model: "iphone11", price: 50000 },
            { brand: "motorola", model: "g4", price: 15000 },
            { brand: "samsung", model: "gx", price: 18000 },
            { brand: "samsung", model: "gx2", price: 25000 }
        ];

        var output = {};

        input.forEach(function (item) {
            var brand = item.brand;
            var price = item.price;

            if (!output[brand] || price < output[brand]) {
                output[brand] = price;
            }
        });
        console.log(output); 
        Output:- { apple: 50000, motorola: 15000, samsung: 18000 }

    **Example: 4**

            var dataList = [
                [
                    "Retail",
                    "22,477",
                    "24,549",
                    "19,580",
                    "15,358",
                ],
                [
                    "Online",
                    "8,653",
                    "7,586",
                    "2,432",
                    "4,321"
                ],
            ];
            filtArr = dataList.filter(arr => arr[0].trim() == 'Retail');
            
            console.log(filtArr);
            Output: [["Retail", "22,477", "24,549", "19,580", "15,358"]]
        
    
    **Example: 5**

        ```
            const ages = [32, 18, 25, 30, 28, 49, 40];

            function checkAdult(age){
                return age >= 30;
            }
            const result = ages.filter(checkAdult);

            console.log(result.sort());
            Output: [30, 32, 40, 49]

        ```

    **Example: 6**

        ```
            **1.**
                let people = [
                    {name: "suresh",age: 44},
                    {name: "ramesh",age: 26},
                    {name: "dinesh",age: 13},
                    {name: "rakesh",age: 33}
                ]

                let toddlers = people.filter(person => person.age <= 3)

                console.log(toddlers)
                Output: [{ age: 14, name: "suresh"}, 
                         { age: 13, name: "dinesh"}]

            **2.**
                let range = {
                    min: 13,
                    max: 16
                }

                let teenagers = people.filter(function(person) {
                    return person.age >= this.min && person.age <= this.max;
                }, range)

                console.log(teenagers)
                Output: [{ age: 26, name: "ramesh" }]

            **3.**
                var aquaticCreatures =  creatures.filter(function(creature) {
                return creature.habitat == "Ocean";
                });

                console.log(aquaticCreatures);

        ```

    **Example: 7**

        ```
            let total = ["10%", "1000", "5%", "2000"];

            let percentage = total.filter(function(item){
                return typeof item == 'string' && item.includes('%');
            });
        
            let absolute = total.filter(function(item){
                return typeof item == 'number' || !isNaN(item);
            });

            console.log(percentage);
            console.log(absolute);

        ```

    **Example: 8**

        ```
            let totals = ["10%", 1000, "5%", 2000];

            **1.**

                let percents = totals.filter(item => item.toString().includes('%'));
                let numbers = totals.filter(item => !item.toString().includes('%'));

                console.log(percents, numbers);

            **2.**

                var percentages = totalss.filter(e => isNaN(e));
                var absolutes = totalss.filter(e => !isNaN(e));

                console.log({percentage , absolute});

        ```

    **Example: 9**

        ```
            1. Exp : JavaScript to illustrate findIndex() method

                function canVote(age) {
                    return age >= 18;
                }
                
                function func() {
                    let filtered = [24, 33, 16, 40].filter(canVote);
                    console.log(filtered);
                }
                func();

            2. Exp

                function isPositive(value) {
                    return value > 0;
                }
                
                let filtered = [112, 52, 0, -1, 944].filter(isPositive);
                console.log(filtered);

            3. Exp
                function isEven(value) {
                    return value % 2 == 0;
                }
                
                let filtereds = [11, 98, 31, 23, 944].filter(isEven);
                console.log(filtereds);

        ```
   **[⬆ Back to Top](#table-of-contents)**


1. ### search using keyword from array

    ```
        var keywordToSearch = 'Arslan'; // word to search
        var keyword =   keywordToSearch.toLowerCase();
        var name = [{id: 1, name: 'Aqib'}, {id: 2, name: 'Arslan'}];

        //search keyword from name array by name
        var searchResult = name.filter(word => word.name.toLowerCase().indexOf(keyword) > -1);
        console.log(searchResult);
        output: > Array [Object { id: 2, name: "Arslan" }]
        
    ```
    //===================================
    ```
    const addOrRemove = (array, item) => {
        const exists = array.includes(item)
    
        if (exists) {
        return array.filter((c) => { return c !== item })
        } else {
        const result = array
        result.push(item)
        return result
        }
    }

    ```
    //=================================

    ```
    var newItem = "Ramesh";
    var array = ["Ramesh", "Jayesh"];
    array.indexOf(newItem) === -1 ? array.push(newItem) : array.splice(array.indexOf(newItem), 1);
    
    console.log(array)

    ```
    //========================================
    
    ```

    const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];
    
    console.log(beasts.indexOf('bison'));
    // Expected output: 1
    
    // Start from index 2
    console.log(beasts.indexOf('bison', 2));
    // Expected output: 4
    
    console.log(beasts.indexOf('giraffe'));
    // Expected output: -1
    
    ```

   **[⬆ Back to Top](#table-of-contents)**

2. ### Finding if an element exists in the array or not and updating the array

    ```
        function updateVegetablesCollection(veggies, veggie) {
            if (veggies.indexOf(veggie) === -1) {
            veggies.push(veggie);
            console.log(`New veggies collection is: ${veggies}`);
            } else {
            console.log(`${veggie} already exists in the veggies collection.`);
            }
        }
    
        const veggies = ["potato", "tomato", "chillies", "green-pepper"];
        
        updateVegetablesCollection(veggies, "spinach");
        // New veggies collection is: potato,tomato,chillies,green-pepper,spinach
        updateVegetablesCollection(veggies, "spinach");
        // spinach already exists in the veggies collection.
        
    ```

   **[⬆ Back to Top](#table-of-contents)**

3. ### Finding all the occurrences of an elements
    
    ```
        const indices = [];
        const arrays = ["a", "b", "a", "c", "a", "d", "a", "a"];
        const element = "a";
        let idx = arrays.indexOf(element);
        while (idx !== -1) {
            indices.push(idx);
            idx = arrays.indexOf(element, idx + 1);
        }
        console.log(indices);
        
        Output: [0, 2, 4, 6, 7]

    ```
3. ### Find the nth Fibonacci number in javascript.
    
    ```
        function fibonac(n){
            if(n <=1){
                return n;
            }
            return fibonac(n-1)+ fibonac(n-2);
        }

        const res = fibonac(4);
        console.log(res);
    ```

