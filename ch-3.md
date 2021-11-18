# Perspectives on Chapter 3: Digging to the Roots of JS
The content for Chapter 3: Digging to the Roots of JS can be found [here](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch3.md)

## Shea

**What I learned**
- Iterables: I've never thought deeply about this topic...
  - Strings are iterables 🤯
  - 3 form, `.keys`, `.values`, `.entries`
- Closure:
  - I like this definition:
    > Closure is when a function remembers and continues to access variables from outside its scope, even when the function is executed in a different scope.

- `this` Keyword
  - Is still confusing 😂
  - But here is now I see it now with the idea of execution context
    ```js
    function classroom(teacher) {
        return function study() {
            console.log(
                `${ teacher } says to study ${ this.topic }`
            );
        };
    }
    var assignment = classroom("Kyle");
    
    assignment(); 
    //Kyle says to study undefined  -- Oops :(
    
    // unless the global window has "topic"
    let topic = "Global Topic"
    assignment();
    // Kyle says to study Global Topic
    
    var homework = {
    topic: "JS",
    assignment: assignment
    };

    // homework is the execution context
    homework.assignment();
    // Kyle says to study JS
    
    var otherHomework = {
        topic: "Math"
    };

    // other homework is now the executionContext.
    assignment.call(otherHomework);
    // Kyle says to study Math
    ```

**What I Liked**
- Mention of how important closures are!  Eric Elliot considers closures a key interview question.

**Questions for the Group**
