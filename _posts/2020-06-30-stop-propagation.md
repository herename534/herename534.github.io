---
   layout: post
   title:  "AST to for event.stopPropagation"
   date: 2020-06-30 10:16:01 +0200
   categories: programming angular javascript frontend
   tags: programming angular javascript frontend
   published: false
   language: English
---

Let's say we have an angular component with the following template

    <div (click)="callFinalMethod()">
        <button (click)="callSomeMethod($event)"> button text </button>
    </div>
    
There is a button wrapped in a div and a callback attached to the button as well as the div
Considering how events work in JavaScript, callSomeMethod will be executed first and then
callFinalMethod. Because of event bubbling. If we want to prevent the bubbling, we could include
something like this code in the callSomeMethod:

    callSomeMethod(event) {
        event.stopPropagation();
    }
    
It's how usually events are prevented from bubbling up. Sometimes we might get bugs in our apps
due to a fact that one of developers may wrap one DOM element in another one and forget to call
the method when it's needed.

If we want to make that event argument conditional, then the code would become:

    callSomeMethod(event?) {
        if (event) {
            event.stopPropagation();
        }
    }
    
We may need it in some situations.

Then what if we have a bunch of methods like callSomeMethod where we could place the if with a call to 
prevent? Then we would have to paste it all over the place, breaking DRY.

But how could we put all this code in one single place? Let's suggest that we would have to call these 3
lines in few components.

We could introduce another layer of complexity and create an abstract component or a class from which those components
would inherit the method. Something like this:



<!--excerpt-->


##### *{{page.content | number_of_words}} words in the post*
