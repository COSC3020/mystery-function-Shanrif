[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11799887&assignment_repo_type=AssignmentRepo)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    // I'm assuming a is a string, so if string a has length 1 then it just returns its element. 
    if(a.length == 1) return a[0];
    // Now, this is recursively calling mystery and shortening the string a, removing the first element every single time. 
    // ie a == Happy goes to, Appy, to PPy, to Py, to P. 
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    // Okay now this bit is comparison, I think was its doing is returning the maximum element in a string or maybe an array because this bit is saying 
    // if foo (the sliced element) is bigger than the first index of an object. then return foo i.e the max element. 
    else return a[0];
    //  If foo is smaller than value at the first index then return that first index value (I said index initially and I had meant value at index) 
    //So it looks like this function is recursively slicing up large elements and returning the largest value of those elements?
}
```
