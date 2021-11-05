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
