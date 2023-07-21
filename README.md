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



1. ### Array method more using. Below Array can be used in all method 
    
    > const names = ["Ramesh", "Suresh", "Rajesh", "Jayesh"];
    
    1. #### The length property returns the length (size) of an array: 
    >   let size = names.length;
    
    2. #### The `push()` method adds a new element to an array (at the end):
    >   names.push("Bhavesh"); 
    
    2. #### The `pop()` method removes the last element from an array:
    >   names.pop();

    3. #### The `shift()` method removes the first array element and "shifts" all other elements to a lower index.
    names.shift();

    4. #### The `unshift()` method adds a new element to an array (at the beginning), and "unshifts" older elements:
    names.unshift("Rakesh");

    5. #### Array elements can be deleted using the JavaScript operator delete.
    //Using delete leaves undefined holes in the array.
    //Use `pop()` or `shift()` instead.
    >   delete names[0];

    6. #### The `splice()` method can be used to add new items to an array:
    //The first parameter (2) defines the position where new elements should be added (spliced in).

    //The second parameter (0) defines how many elements should be removed.

    ///The rest of the parameters ("Rakesh" , "Dinesh") define the new elements to be added.

    >   names.splice(2, 0, "Rakesh", "Dinesh");

    7. #### The slice() method slices out a piece of an array into a new array.
    //The slice() method creates a new array.

    8. #### The slice() method does not remove any elements from the source array.
    >   const citrus = names.slice(1);

    9. #### The slice() method can take two arguments like slice(1, 3).
    >   const citrus = names.slice(1, 3);

    10. #### The sort() method sorts an array alphabetically:
    >   names.sort();

    11. #### The reverse() method reverses the elements in an array.
    >   names.reverse();


    const arr1 = ["Cecilie", "Lone"];
    const arr2 = ["Emil", "Tobias", "Linus"];
    const arr3 = ["Robin", "Morgan"];
    const myChildren = arr1.concat(arr2, arr3);
    const myChildren2 = arr1.concat(arr2);
    //=============================

    const myArr = [[1,2],[3,4],[5,6]];
    const newArr = myArr.flat();
    console.log(newArr);
    //======================================


    //=========================================
    const points = [40, 100, 1, 5, 25, 10];
    points.sort(function(a, b){return a - b});
    points.sort(function(a, b){return b - a}); // descending
    // now points[0] contains the lowest value
    // and points[points.length-1] contains the highest value

    //=============================================
    const cars = [
    {type:"Volvo", year:2016},
    {type:"Saab", year:2001},
    {type:"BMW", year:2010}
    ];

    cars.sort(function(a, b){return a.year - b.year});
    //=====================================================

```
    var creatures = [
    {name: "Shark", habitat: "Ocean"},
    {name: "Whale", habitat: "Ocean"},
    {name: "Lion", habitat: "Savanna"},
    {name: "Monkey", habitat: "Jungle"}
    ];

    var aquaticCreatures =  creatures.filter(function(creature) {
    return creature.habitat == "Ocean";
    });

    console.log(aquaticCreatures);
    ```
    //========================
    ```
    let total = ["10%", "1000", "5%", "2000"];
    let percentage = total.filter(function(item){
    return typeof item == 'string' && item.includes('%');
    });
    console.log(percentage);
    let absolute = total.filter(function(item){
    return typeof item == 'number' || !isNaN(item);
    });
    console.log(absolute);
    ```
    //===================================
    ```
    let totals = ["10%", 1000, "5%", 2000];

    let percents = totals.filter(item => item.toString().includes('%'));
    let numbers = totals.filter(item => !item.toString().includes('%'));
    console.log(percents, numbers);
    ```
    //===================================
    ```
    let totalss = ["10%", 1000, "5%", 2000];
    var percentages = totalss.filter(e => isNaN(e));
    var absolutes = totalss.filter(e => !isNaN(e));
    console.log({percentage , absolute});
    ```
    //=========================================================
    ```
    const ages = [32, 18, 25, 30, 28, 49, 40];

    function checkAdult(age){
        return age >= 30;
    }
    const result = ages.filter(checkAdult);

    console.log(result.sort());
    ```
    //==================================
    ```
    var numbers = [5, 4, 12, 3, 16, 8, 11];

    var greaterThanCondition = numbers.filter(function(number) {
    return number > 5;
    });

    const sortedArray = greaterThanCondition.sort((a,b) => a-b);
    console.log(sortedArray);
    ```
    //==============================================
    ```
    let people = [
        {name: "aaron",age: 65},
        {name: "beth",age: 2},
        {name: "cara",age: 13},
        {name: "daniel",age: 3},
        {name: "ella",age: 25},
        {name: "fin",age: 1},
        {name: "george",age: 43},
    ]

    let toddlers = people.filter(person => person.age <= 3)

    console.log(toddlers)

    let range = {
    lower: 13,
    upper: 16
    }

    let teenagers = people.filter(function(person) {
        return person.age >= this.lower && person.age <= this.upper;
    }, range)

    console.log(teenagers)
    ```
    //================================
    ```
    let team = [
        {
            name: "aaron",
            position: "developer"
        },
        {
            name: "beth",
            position: "ui designer"
        },
        {
            name: "daniel",
            position: "content manager"
        },
        {
            name: "ella",
            position: "cto"
        },
        {
            name: "fin",
            position: "backend engineer"
        },
        {
            name: "george",
            position: "developer"
    },

    ]

    let developers = team.filter(member => member.position == "developer")

    console.log(developers)
    let nondevelopers = team.filter(member => member.position !== "developer")

    console.log(nondevelopers)
    ```
    //=============================================
    ```
    // JavaScript to illustrate findIndex() method
    function canVote(age) {
        return age >= 18;
    }
    
    function func() {
        let filtered = [24, 33, 16, 40].filter(canVote);
        console.log(filtered);
    }
    func();
    ```
    //================================
    ```
    function isPositive(value) {
        return value > 0;
    }
    
    let filtered = [112, 52, 0, -1, 944].filter(isPositive);
    console.log(filtered);
    ```
    //===============================
    ```
    function isEven(value) {
        return value % 2 == 0;
    }
    
    let filtereds = [11, 98, 31, 23, 944].filter(isEven);
    console.log(filtereds);
    ```
    //===============================
    ```
    var myArray = ["bedroomone", "bedroomonetwo", "bathroom"];

    var bedrooms = myArray.filter(name => name.includes('bedroom'))
    console.log(bedrooms);
    ```
    //===================================
    ```
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
    [
        "In Store",
        "2,532",
        "2,836",
        "5,632",
        "7,325"
    ]
    ];
    filtArr = dataList.filter(arr => arr[0].trim() == 'Retail');
    console.log(filtArr);
    ```
    //===============================
    ```
    const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

    const results = words.filter(word => word.length > 6);

    console.log(results);
    // expected output: Array ["exuberant", "destruction", "present"]

    // search using keyword from array

    var keywordToSearch = 'Arslan'; // word to search
    var keyword =   keywordToSearch.toLowerCase();
    var names = [{id: 1, name: 'Aqib'}, {id: 2, name: 'Arslan'}];

    //search keyword from names array by name
    var searchResult = names.filter(word => word.name.toLowerCase().indexOf(keyword) > -1);
    console.log(searchResult);
    // expected output: > Array [Object { id: 2, name: "Arslan" }]
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
    //================================
    ```
    //Finding if an element exists in the array or not and updating the array
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
    
    ```
    //Finding all the occurrences of an elements
    
    const indices = [];
    const arrays = ["a", "b", "a", "c", "a", "d", "a", "a"];
    const element = "a";
    let idx = arrays.indexOf(element);
    while (idx !== -1) {
        indices.push(idx);
        idx = arrays.indexOf(element, idx + 1);
    }
    console.log(indices);
    // [0, 2, 4]
    ```


