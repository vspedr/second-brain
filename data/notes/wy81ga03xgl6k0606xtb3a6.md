
`call` sets its first argument to the `this` value for the function it's invoked on. the following arguments are passed to that function and it is immediately invoked.

```javascript
function test(arg1, arg2){
  console.log(this.num, arg1, arg2); // 100, 10, 20
}

test.call({num: 100}, 10, 20);
```

`apply` sets its first argument to the `this` value for the function it's invoked on. the second arguments is an array of values to be passed as arguments to that function and it is immediately invoked.

```javascript
function test(...arguments){
  console.log(this.num, arguments);//100, [1,2,3]
}

test.apply({num: 100}, [1,2,3]); 
```

`bind` sets its first argument to the `this` value for the function it's invoked on. the following arguments are passed to that function and a new function is returned.

```javascript
function test(arg){
 console.log(this.number, arg);
}

let bindedFn = test.bind({number: 99}, "argument");

bindedFn(); // 99, "argument"
```

[Reference](https://www.educative.io/answers/what-is-the-difference-between-call-apply-bind)