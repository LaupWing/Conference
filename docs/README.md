# Conferences
Here you can find my documentations about the conferences I have watches for the minor web development at the HVA.

## Table of contents
* [TypeScript: Seeing Past the Hype](#typeScript-seeing-past-the-hype)
* [Design Principles of Vue 3.0 by Evan You](#design-principles-of-vue-3.0-by-evan-you)
    * [Diverse audience](#diverse-audience)
    * [CDN build & Vue CLI](#cdn-build-&-vue-cli)
    * [Options API & Composition API](#options-api-&-composition-api)
    * [Typescript vs Javascript](#typescript-vs-javascript)
    * [Template vs JSX](#template-vs-jsx)
    * [Power vs Size](#power-vs-size)
    * [Framework Coherence vs Low Level Flexibility](#framework-coherence-vs-low-level-flexibility)
    
## TypeScript: Seeing Past the Hype

* Source: [Click here to see the conference](https://www.youtube.com/watch?v=KfluE6-wDSU)

In this talk the presentator is going to talk about what the is behind Typescript. 

## Design Principles of Vue 3.0 by Evan You

* Source: [Click here to see the conference](https://www.youtube.com/watch?v=WLpLYhnGqPA&feature=youtu.be)

This talk is about what the developers of Vue what changed and why they make those changes in the newer version of Vue aka Vue 3.

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
Typescript is a strict superset of Javascript. Below you see a little example of how Typescript may look like
```typescript
const slytherin: string = 'slytherin';
const gryffindor: boolean = false;

function takesString(arg: String){
  console.log(arg);
}
takesString(slytherin) // works
takesString(gryffindor) // error
```



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
