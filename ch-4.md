# Perspectives on Chapter 3: Digging to the Roots of JS
The content for Chapter 4: The Bigger Picture can be found [here](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch4.md)

## Shea


**What I learned**

- Pillar 1: Scope and Closure
  Hoisting!  OMG Hositing!  With the addition of `let` and `const` hoisting has been much less discussed.  I suspect [Kyle Simpson](https://github.com/getify/You-Dont-Know-JS/blob/4c6b88f842694b3784b32024b552b7f07fb5f1fa/get-started/ch2.md?plain=1#L264) disagress with [Eric Elliot](https://medium.com/javascript-scene/javascript-es6-var-let-or-const-ba58b8dcde75) on use of `let` vs `const`.  But something worth thinking about from time to time.  I hadn't hear the term "Temporal Dead Zone".
  
  [Simpson's recommendation for `const`](https://github.com/getify/You-Dont-Know-JS/blob/4c6b88f842694b3784b32024b552b7f07fb5f1fa/get-started/ch2.md?plain=1#L264)
  > The best semantic use of a `const` is when you have a simple primitive value that you want to give a useful name to, such as using `myBirthday` instead of `true`. This makes programs easier to read.


**What I Liked**

- Pillar 2
  > Even if you love TypeScript/Flow, you are not going to get the most out of those tools or coding approaches if you aren't deeply familiar with how the language itself manages value types.

  This resonates with me.  We need to understand JS reguardless to our use of TS.  It all compiles down to JS in the end.
  
- [With the Grain](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch4.md#with-the-grain)
  - What a great section!  So much empathy and kindness!  Own your opinions! 
  - > Can you make your JS program look like a Java, C#, or Perl program? What about Python or Ruby, or even PHP? To varying degrees, sure you can. But should you?
    > No, I don't think you should.  

  - > But if you choose to align with my opinions, you have to be prepared to back up those choices with why you feel that way. Don't just parrot what I say. Own your opinions. Defend them. And if someone you were hoping to work with disagrees, walk away with your head still held high. It's a big JS, and there's plenty of room for lots of different ways.
  - **FAVORITE!!!** 
    > That's the most important advice I can impart to help you learn JS. *Always keep looking for better ways to use what JS gives us to author more readable code.* Everyone who works on your code, including your future self, will thank you!

**Questions for the Group**

## Shipeng
I like the pillars!
- Pillar 1: Scope and Closure
  - JS is lexically scoped
  - "Temporal Dead Zone" (TDZ)
- Pillar 2: Prototypes
  - JS is one of very few languages where you have the option to create objects directly and explicitly, without first defining their structure in a class.
  - prototypal inheritance vs behavior delegation
- Pillar 3: Types and Coercion
   - foundation of JS 
