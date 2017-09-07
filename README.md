---

# Naming function parameters
## And creating readable methods
--------------------------------------------------------

> //Image here

###Little but important
--------------------

In swift, naming parameters is a bit different. In my learning process I had a lot of stuff to pick up in swift , so I didn't want to pay my attention to the little details like naming the parameters of function besides I didn’t know that swift has this feature.

As days pass by I had to read others swift codes and figure out what does the developer wanted to do then I saw separate parameter names in his/her methods that made me to stop and think about it. This was very cool feature for readability. 
So let’s see how do we use them;

###beautify(swift functions: )
Let’s start with example:

``` 
func introTo(parameter naming: String) -> String{
//we use naming here
return naming
}
//when we call our function we use parameter
introTo(parameter: "swift functions")
//returns -> swift functions
```

As you can see above when you give the name for your parameter there are two separate names. So the first one is for external which means your parameter there are two separate names. So the first one is for external which means you use it when you call your function outside of the method and the second one is for internal which means local variable that you use inside of your method

##Apple
> Each function parameter has both an argument label and a parameter
> name. The argument label is used when calling the function; each
> argument is written in the function call with its argument label
> before it. The parameter name is used in the implementation of the
> function. By default, parameters use their parameter name as their
> argument label. — Swift programming language book (swift 4 edition)

So if we look at our example:

```
func introTo(parameter naming: String,... 
```

`parameter` is an argument label and the `naming` is a parameter name.
By the way, All parameters must have unique names. But multiple parameters can have same argument label. Unique argument labels are preferred for readability.

> argument label == external name, parameter name == internal name

The last sentence in apple’s explanation was:

> By default, parameters use their parameter name as their argument
> label.

let’s see with example what swift engineers wanted to say;

```
func global(firstParameter: String, secondParameter: String){
print(“\(firstParameter) , \(secondParameter)”)
 }
global(firstParameter: “Hello”, secondParameter: “buu”)
//prints -> Hello , buu
```



There is no argument labels so parameter name will be both internal and external. This is what we all use in general and it is the default one.

But what if we want to omit external name? Then we use underscore( _ ).
Here it is:

```
func ignoreExternalName(_ firstParameter: String, _ secondParameter:String){
print("\(firstParameter), \(secondParameter)")
}
ignoreExternalName(“first”, “second”)
//prints -> first, second
```

You can also ignore your parameter name(internal) but it will be meaningless because you can’t use it inside of your method.

###Wrapping Up

Let’s use all of these in one example to wrap up

```
func namingParameters(iAm name: String, from country: String, _ job: String, yearOld: Int, comment _: String){
//As you see I omitted parameter name in the last parameter now I can't use it here
print(“I am \(name) from \(country), I am a \(job) who is \(yearOld). Thanks for reading this blog, hope to see you in the next blogs”)
}
//This is how it looks like when you call it
namingParameters(iAm: <#T##String#>, from: <#T##String#>, <#T##job: String##String#>, yearOld: <#T##Int#>, comment: <#T##String#>)
//Done
namingParameters(iAm: "Davut", from: "Turkmenistan", "student", yearOld: 20, comment: "Done")
//prints -> I am Davut from Turkmenistan, I am a student who is 20. Thanks for reading this blog, hope to see you in the next blogs
```
Wohoo 🎉 looks awesome right?
Time to beautify your own methods. 😉
> If anything else just leave a comment 


---
