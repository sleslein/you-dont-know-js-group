# Perspectives on Chapter 2: Surveying JS
The content for Chapter 2 Surveying JS can be found [here](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md)

## Shea

- Dense chapter... lots of good "refresher" info.

**What I learned**
- [Each File is a Program](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md#each-file-is-a-program) - I'm starting to think we may not be structureing our files/modules in the best way.  I think I'll have a better persective when we read the [modules chapter in the "Scope and Closure" book](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/scope-closures/ch8.md).
  - [ESM Modules](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md#es-modules) - As noted in this section each file is a module.  Further convincing me, we are doing some things in sub-optimal ways... Like possibly where and how we declare types in the `/types` directory.

- [Arrays & Objects](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md#arrays-and-objects) - I forgot array's are objects!
- [Declaring and Using Variables](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md#declaring-and-using-variables) 
  - I apprecate his sentiment about the use of `var`, but I side with the of the JS-verse.... its best to avoid `var`.  If you have a need for what it offer, you better document that in the code also.
  - `let` vs `const` - I wonder if this tip would have helped us avoid some of the confusiong around those global objects we were `const`ing up?
- [How We Organzie JS](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md#how-we-organize-in-js) ) 
  - We don't use classes in our current projects. I don't think the fit the the FE web dev model well in most cases.  Server side is a different story.
  - Now I miss C# and OOP a bit.
  - OOP is all about data encapsulation and modifying via behaviors.  

**What I Liked**
> Should function expressions be named or anonymous? Opinions vary widely on this. Most developers tend to be unconcerned with using anonymous functions. They're shorter, and unquestionably more common in the broad sphere of JS code out there.
> **In my opinion, if a function exists in your program, it has a purpose; otherwise, take it out! And if it has a purpose, it has a natural name that describes that purpose.**
> *If a function has a name, you the code author should include that name in the code,* so that the reader does not have to infer that name from reading and mentally executing that function's source code.
> 
> ...
> 
> Since I don't think anonymous functions are a good idea to use frequently in your programs, **I'm not a fan of using the => arrow function form**. This kind of function actually has a specific purpose (i.e., handling the this keyword lexically), but that doesn't mean we should use it for every function we write. Use the most appropriate tool for each job.
> - [Appendix A, So Many Function Forms](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/apA.md#so-many-function-forms)

YES YES YES!!!!!

**Questions for the Group**
- What do you think about Kyle's perspective/tip on `let` vs `const`?
  > If you stick to using const only with primitive values, you avoid any confusion of re-assignment (not allowed) vs. mutation (allowed)! That's the safest and best way to use const. [Declaring and Using Variables](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch2.md#declaring-and-using-variables)  

- What do you make of Kyle's closing comments?  
  > I'm serious when I suggest: re-read this chapter, maybe several times. 

## Shipeng

- A lot of information, good to know but better to have real world examples to understand pros and cons for each feature easily.

**What I learned**
- double-quote = single-quote <> back-tick (interpolation)
- it's safest and best to use only undefined as the single empty value
- let (block scoping)
- function declaration vs function expression 
- functions are values
- equality comparison (===, Object.is(..), identity equality for object values, ==, >, <, <=, >= coercive equality) vs equivalence comparison.
- class vs module

**Questions**
- when use classes and when use modules

## Annie

- I like how he explained why things are working in JS the way they are.  

**What I learned**
- each file is a program... makes me think of `slickgrid`.  
- interpolation.... Ah... that's what it is..  I was like Hum.. new keyboard symbol! 
- nice to see the comparison of different function styles, module/class, etc. 
- new trick, Object.is(...).  Can't wait to use it.   
- === vs ==

https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/apA.md#so-many-function-forms
- function name inference

## Jay
- It was intersting to see the different ways the Javascript design patterns have evolved.
**What I learnd**
- back-tick vs double quote
- This i found intersting from my research- Why is Null an object?
    As promised, now let’s look as to why the type of null is an “object”. As it then indicates that null must be an object, which is not true. In fact, null is one of the primitive values in JavaScript.
    It is actually a bug in the language and unfortunately can’t be fixed that easily, as it will break the existing codebase. However, there is actually one logical explanation behind why null is an object in javascript.
    In the initial version of JavaScript, values were stored in 32 bit units. The first 3 bits represented the data type tag followed by the remaining bits that represented the value.
    For all objects it was 000 as the type tag bits. null was considered to be a special value in JavaScript from its very first version. null was a representation of the null pointer. However, there were no pointers in JavaScript like C. So null simply meant nothing or void and was represented by all 0’s. Hence all its 32 bits were 0’s. So whenever the JavaScrit interpreter reads null, it considers the first 3 bits as type “object”. That is why typeof null returns “object”.
- === vs == (where I have been burned in the past)
- My annoyance of Anonyous functions only only increased and definitely see named functions only in my future :slightly_smiling_face:

f = (x,y) => x * y;

## Discussion example
// High Order Function
f = (x) => (y) => x * y;

function multiply(x) {
  function inner(y) {
    returhn x * y;
  }
  return inner;
}

const multipleByMe = multiply(5);
const 5x7 = multiplyByMe(7); // 35

