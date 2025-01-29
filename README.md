# DSA notes
## Array
Collection  of data
Operations :

 - Creating array
 - Inserting / removing data or elements
 - Access elements using index
 - Itrating on array
 - Updating value at any index

**Q : Find good pairs**

    // good pair;
    // arr[i] == arr[j] & i<j
    
    // Input
    const arr = [1, 2, 3, 1, 1];
    
    let sum = 0;
    let runCount = 0;
    
    // SOLUTION 1 ----------------------------
    sum = 0;
    runCount = 0;
    for (let i = 0; i < arr.length; i++) {
      for (let j = i + 1; j < arr.length; j++) {
        runCount = runCount + 1;
        if (arr[i] == arr[j]) {
          console.log(`(${i}, ${j})`);
          sum = sum + 1;
        }
      }
    }
    console.log("runCount", runCount);
    // ---------------------------------------
    
    // SOLUTION 2 ----------------------------
    const f = (x) => {
      for (i = 0; i < x; i++) {
        runCount = runCount + 1;
        if (arr[i] == arr[x]) {
          console.log(`(${i}, ${x})`);
          sum = sum + 1;
        }
      }
    };
    for (let x = 1; x < arr.length; x++) {
      f(x);
    }
    console.log("runCount", runCount);
    // ---------------------------------------
