# Execution Context

## 1 Variable Declarations
### Task 1.1
- Visualize execution context creation steps by step and explain the reason of output result

```
let a = 0;

for (let i = 0; i < 5; i++) {
   a++;
}
```

### Task 1.2
- Visualize execution context creation steps by step and explain the reason of output result

```
var b;

if (b > 2) {
    console.log(b);
}

b = 5;
```

## 2 Declaration Function & Function Expression

### Task 2.1
- Visualize execution context creation steps by step and explain the reason of output result

```
foo();

var foo;

function foo() {
    console.log( 1 );
}

```

### Task 2.1
- Visualize execution context creation steps by step and explain the reason of output result

```
foo();

var foo;

foo = function() {
    console.log( 2 );
};
```

## 3. Arguments
### Task 3.1
- Visualize execution context creation steps by step and explain the reason of output result

```
const sayHello = function (a,b) {
    return  arguments
};

console.log(sayHello(3,4));
```

### Task 3.2
- Visualize execution context creation steps by step and explain the reason of output result

```
const sayHelloArrow = (a,b) => {
    return  arguments
};

console.log(sayHelloArrow(6,7));
```

## 4 Exercises

### Task 4.1
- Why output is 1 and NOT 2?  

```
foo();

var foo;

foo = function() {
    console.log( 2 );
};

function foo() {
    console.log( 1 );
}
```

### Task 4.2
- What would be the output and why?
- How make a = 8 logged in console? Rewrite the code.

```
function foo() {
    console.log( this.a );
}
const a = 8;
const obj = {
    a: 2,
    foo: foo
};

obj.foo();
```

### Task 4.3
- How invoke foo() function to log 42 in console. Explain your answer.

```
function foo() {
    console.log( this.a );
}

const obj2 = {
    a: 42,
    foo: foo
};

const obj1 = {
    a: 2,
    obj2: obj2
};
```

### Task 4.4
- Why it would throw the error message? How you can get the value 18 in the output?

```
function foo() {
    var a = 1;
    var b = 9;

    if (a >= 1) {
        let b = 2;

        while (b < 5) {
            let c = b * 2;
            b++;

        }
    }
    console.log( a + c + b );
}

foo();
```

  
### Materials to read
- [Interpreter vs Compiler](https://www.youtube.com/watch?v=I1f45REi3k4)

- [V8 Engine](https://www.youtube.com/watch?v=p-iiEDtpy6I&t=732s)

- [Execution Context](https://www.freecodecamp.org/news/execution-context-how-javascript-works-behind-the-scenes/)

