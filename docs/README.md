# Conferences
Here you can find my documentations about the conferences I have watches for the minor web development at the HVA.

## Table of contents
* [TypeScript: Seeing Past the Hype](#typeScript-seeing-past-the-hype)
    * [Types](#types)
    * [What is Typescript](#what-is-typescript)
    * [Typescript Is really smart](#typescript-is-really-smart)
    * [But Typescript can be very hard!](#but-typescript-can-be-very-hard!)
    * [Typescript is still worth implementing](#typescript-is-still-worth-implementing)
* [Design Principles of Vue 3.0 by Evan You](#design-principles-of-vue-3.0-by-evan-you)
    * [Diverse audience](#diverse-audience)
    * [CDN build & Vue CLI](#cdn-build-&-vue-cli)
    * [Options API & Composition API](#options-api-&-composition-api)
    * [Typescript vs Javascript](#typescript-vs-javascript)
    * [Template vs JSX](#template-vs-jsx)
    * [Power vs Size](#power-vs-size)
    * [Framework Coherence vs Low Level Flexibility](#framework-coherence-vs-low-level-flexibility)
* [Predicting the Future of the Web Development (2020 and 2025)](#predicting-the-future-of-the-web-development-2020-and-2025)
    * [Typscript](#typescript)
      * [Prediction1](#prediction-1)
    * [WebAssembly](#webassembly)
      * [Prediction2](#prediction-2)
    * [Packages](#packages)
      * [Prediction3](#prediction-3)
    * [Compile to Js](#compile-to-js)
      * [Prediction4](#prediction-4)
    
## TypeScript: Seeing Past the Hype

* Source: [Click here to see the conference](https://www.youtube.com/watch?v=KfluE6-wDSU)

In this talk the presentator is going to talk about what the is behind Typescript. 

### Types
First lets define what a type is. A type is:
```
A type is an attribute of data that tells the computer how the programmer inteds to use it.
```
Typescript makes heavily use of types, therefore the name typescript. It uses basic types like; `boolean`, `number`, `string`, `array`, `object`.
There also falsy types like; `null` and `undefined`, but Typescript adds two other falsy types like `never` and `void`.

Types can also be be derived from other types, like an object with a certain kind of shape.

In Typescript there is also an type called `any` which can be any kind of type. Its like an esape route.

### What is Typescript
Typescript is a strict superset of Javascript. Below you see a little example of how Typescript may look like. In this example below when you run the code through an complire and you pass in the function an string it will work just fine. But when you pass an diffrent type it will give you an error.
```typescript
const slytherin: string = 'slytherin';
const gryffindor: boolean = false;

function takesString(arg: String){
  console.log(arg);
}
takesString(slytherin) // works
takesString(gryffindor) // error
```

### Typescript Is really smart
With the use of typescript you get really fast error handling. When you for example defined what kind of property's there will be in a certian function it will give you an error if you pass it an property which the function cant accept. So it gives you realtime error feedback in your editor.

This also counts for methods. If you for example use the `slice` method on a number it will give you an error saying that the `slice` method doesnt exist on the number object.

### But Typescript can be very hard!
Typescript can ben very hard to implemend in diffrent situation. When you use Typescript with React and you got Higher Order components you got to takes lots of steps to make Typescript work with Higher order components. And when that happends people tend to use the `any` type to bypass the errors, but defeats the purpose of Typescript. With Typescript you add complexity to your app. Javascript is an untype language and with Typescript you make it an Typed language.

### Typescript is still worth implementing
Typescript is still worth implementing in your applications for the following reasons:
* It eleminates an entire class of buggs. Your editor catch buggs earlier on because Typescript gives you an error warning in your editor.
* When your application is big and you work with lots of people it helps with preventing errors.
* Typescript Allows to place constraints on engineers
  * Can constraint certain usage of newer feature for example.
  * Prevent using outdated methods in certiain packages
* Typescript allows you to forget about other parts of your codebase

## Design Principles of Vue 3.0 by Evan You

* Source: [Click here to see the conference](https://www.youtube.com/watch?v=WLpLYhnGqPA&feature=youtu.be)

This talk is about what the developers of Vue what changed and why they make those changes in the newer version of Vue aka Vue 3.

### Diverse audience
Vue has an extremely diverse audience

The audience are mainly:
* Beginners just progressing form HTML & CSS
* Proffesionals moving on from jQuery
* Veterans migrating from another framework
* Backend engineers looking for lightweight framework frontend solution
* Architects choosing the foundations for entire organization

With an extreme diverse audience they have extreme diversity in use cases. Some what an long lasting project, and some just wants to add some interactivity onto legacy applications.

So the developers of Vue has to make some trade offs in desigining the newer version of Vue. Do they what the API optimized for easy-ness but that leads to maintainablity issues and such.

### CDN build & Vue CLI
For the people with the use case of just simply implenting vue into their projects there is an option to use vue with an cnd link. This removes the barrier of getting into vue. But there is an option to add some more tooling for more complex applactions which uses the Vue cdn.

### Options API & Composition API
I have not used both the Otpions API or Composition API. But from the talk I have learned that they both serve the same purpose less or more. But the options API is easy to start with but has some scalability issues in largers applications. But Composition API is more complex and is u reusable and supports Typescript so it is better for in the long run.

### Typescript vs Javascript
Typescript is not neccessary for using Vue. It is just something that you can add to your Vue application to keep up the maintabality for your Vue apps. But ofcourse you need to have some knowledge about Typescript beforehand and is slower initial development.

Under the hood the developers of Vue added Typescript to their Vue3 source code so that users that dont use Typescript benefits of this because of the editor auto completion.

### Template vs JSX
Vue uses both Template and JSX. The reason for this is that Vue has an diverse audience. Vue uses initially templates, but for the people that want more contorl they can dive deeper and mess with the virtual dom which Vue uses under the hood.

By using the template initially on Vue it helps with the performance of the application. The reason for this is becuase the virual dom must constanlty recursvely listen to changes in the whole dom tree. 

### Power vs Size
Every new feature increases bundle size for every user. When you use vue by using ES modules, Vue can make use of tree shaking which webpack provides. The features that the user doesnt use with Vue it doesnt get imported. So the users of Vue dont pay for the features they never use. 

So the developers of Vue can keep adding features without bloating the size of the vue for everyone.

### Framework Coherence vs Low Level Flexibility
You got React on the one hand and Angular on the other hand. React tries to do very little and Angular tries to do alot.

React has a fewer concepts to start with which allows for more flexibility for the users. Because of this users can add diffrent solutions for one problem. And the second problem of this is there is no offical documentation about the things you use with React. You have to rely on the people who made that plugin that you have used for React.

Angular and other large scope frameworks has everything available for the users. The pro of this is that there is a consistent design proces and ecosystem. Most of the problem the users have there is an officale solution for that which works very well. But the cons of this that there is a higher upfront learing barier. Another con is that the maintance and introducing more ideas is more costly. Angular doesnt change alot and if it changes it is harder for the users to learn the newer ecosystem.

Vue is somewhere in the middle of React and Angular. Vue begins with the core of the framework which is the layer of activity and the user can adds more layers to it if he or she wishes to. But none of the layers you want to add is required knowledge when you first start using vue. Also when you need for a common problem, Vue almost everytime has a official solution for you. 

## Predicting the Future of the Web Development (2020 and 2025)

* Source: [Click here to see the conference](https://www.youtube.com/watch?v=24tQRwIRP_w&list=PLWYWTh1no3EgYPKtLoN-SMbP8EYB3ffEq&index=4&t=0s)

You always have to look into the future to figure out which technology stack you are going to use. Learning a stack is an mayor task because you have to learn alot, and it would be a waste when that particular stack wouldn't be used after a year or so. So it is important to kinda look into the future to determine what you would like to learn or invest your time in. Perl for example has dropped mayorly in popularity the last decade or so. 

But that doesnt mean that you have to choose a stack that has mayor popularity or one that is mainstream. You are still making a bet on the future because Perl for example was mayor popular in 2006 but nowadays no one uses it anymore. The big takeaway is that you choose a stack that you are comfortable using and that you will be happy for the coming years. 

**Predicting is safer than following blindly**

In this talk the presentator predicts that the following technologies will be used in the future:
* Typescript
* Web assembly
* Packages
* Compile to js

### Typescript
In the last 5 years Typscript surges in popularity. The popularity will only increase because the mayor frameworks are implementing typescript into their code. 

Typescript can give a false sense of security because the keyword any which bypasses the type checking. But that is the only negative side of Typescript. 

When working in teams it benefits alot when you use Typescript. Once teams used Typescript they almost never go back on normal javascript and that is an indication that Typescript will only increase in popularity

### Prediction 1
_Typescript takes over the JS world_

**by end of 2020:** TS is the most common choice for new commercial JS projects

**by end of 2025:** more people writing TS daily than JS without TS

### WebAssembly
What is WebAssmbly? An simplyfied description of WebAssembly is almost machine code that runs in a browser. WebAssembly can be use to improve existing JS libaries. But Javascript Perf is widely accepted so a  performance use case isnt really valid for using WebAssembly.

It is much more interesting for big application on the web like Figma, that competes with appstores and installers. In these cases performance is a big part. 

WebAssembly can allow web apps to use the same techonlogies as native apps do. So for example games can run on the web.

### Prediction 2
_WASM expands the Web App_

**by end of 2020:** Wasm Makes no significant diffrence to the makeup of the web

**by end of 2025:** wasm has created a new niche of heavyweight web apps

### Packages
When we talk about packages, you can mainly think of NPM. NPM is the biggest package system ecosystem. There are a lot of competing package ecosystems like Yarn and Github Package Registry. Are these signs of NPM going away? Not really, because lots of people and even the competing pacakge systems are using the same layout of holding packages aka the `package.json` file. 

But there is one other big problem with NPM, and that are the packages itself. When you download an npm package there always is an possibility that you download some malicous code. Even if you dont download an package that has malicious code that pacakge uses other packages which can contain some malicious code. So it is harder to discover malicious files.
But it hasnt happend yet, and you can prevent it from happening by using the followin code to prevent post-install scripts `npm config set ignore-scripts true`.

### Prediction 3
npm lasts, surviving futher problems

**by end of 2020:** at least one new npm security incident makes headlines

**by end of 2025:** at least one malicious npm package has infected many dev's machines except for people using the code above!

## Compile to JS
When you think about compile to JS you can think about Babel Typscript svelte and such. And Dart which doesnt actually compiles to Javascript but has the same dialect aka similart synthax as Javascript. And at least of course the big javascript frameworks. 

During this point i felt like it was more an commercial of elm because the presentator talks alot about elm and tries to sell it... So i dont think he eloborated much on this topic overall. He could rather call this section Elm instead of "compile to js"


### Prediction 4
_JS alternatives stay niche, and age well._

**by end of 2020:** compile to js langauges still growing, but none as fast as typescript

**by end of 2025:** non-JS dialects have aged well, although Typescript is more popular

## Joy - Maintaing Passion for Pgrogrammming

* Source: [Click here to see the conference]https://www.youtube.com/watch?v=GQFbUS2jnMc&list=PLWYWTh1no3EgYPKtLoN-SMbP8EYB3ffEq&index=6&t=1272s)

The speaker of this presentation is Bruce Tate. He is the author of the books 7 Languages in 7 days and Bitter Java. 

His talk is about having joy in going to your coding work and having joy when solving a programming problem.

