# Oh ternary operator is goated.

As an intermidiate java script developer, I have always shy away from anything that try to abstract my beginner's way of doing things in JS, Such as using fat function instead of using **function(){}**

```JS
document.addEventListener("DOMContentLoaded", ()=>{
//  (fat funky is cool too btw)
})
```

Or Writing if statement logic on a line with note **else{}**

```JS
const cat = 44
if (cat < 5) console.log("hello reader ")
```

But i have to say ternary operator is indeed goated. and i hope i get many chance to flex use it in my code hehe.

imagine writing all of these :

```JS
const storedTask = localstorage.getItem("newTask");
let taskList;
if (storedTask){
    taskList = JSON.parse(storedTask);
} else{
    taskList = [];
}
taskList.push({ task: todoInput });

```

When you can just write these 3 beautiful lines

```JS
const storedTask = localStorage.getItem("newTask");
let taskList = storedTask ? JSON.parse(storedTask) : [];
taskList.push({ task: todoInput });

```

Anyways ternary operator is all about
If (truthy) ** Do this ** other wise do that

eg

```JS
let cat = 5;
let newCat = cat > 0 ? cat + 1 : 0;
console.log(newCat); // Outputs: 6
```

That is all Happy coding
