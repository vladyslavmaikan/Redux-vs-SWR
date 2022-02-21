# Redux-vs-SWR

## The purpose of this research is to understand the difference between Redux and SWR and whether the last can replace Redux in our projects.

## This repository includes two applications - one created with redux and the second one with SWR.
## The goal of spike - find the better solution for our projects, we will compare optimisation, development speed and application complexity.

## Why Redux is Awesome
It's unopinionated. Redux requires you to put your global state in a store, and to manage that state via reducers and actions. An action is a simple JavaScript object with a type property, and a reducer is a pure function that transforms the old state into the new state based on an action. Beyond this, everything else is up to you.
It has a minimal API surface. Redux only has 5 top-level exports, and only one of those, createStore, is essential.
It's extremely versatile. Do you want your store to contain only the ID of the current user? Or do you want your store to track the state of every entity, page, widget, and input in your massive enterprise app? Whatever your use case, Redux and its large ecosystem have you covered.

## Why Redux is Hard
Redux is hard for the same reasons it is awesome.

It's unopinionated. Redux doesn't tell you how to structure your application's state, reducers, or actions, so you have to make your own decisions.
It has a minimal API surface. You'll quickly realize you need more than just createStore to create a useful application with Redux. A prime example of this is the need to fetch data from an API in response to an action.
It's extremely versatile. There are so many different frontend architectures that are possible with Redux that it's easy to get lost. It took me a long time to figure out how Redux fit into the React applications I was building.


## SWR
1. It allowed us to delete code
Pull requests that delete code, rather than add code, are my favourite to open. The less code in our application, the less chance for bugs, the better. As I get older, I have started to appreciate simplicity more and more. It allowed us to delete entire unstated stores and made our application simpler and easier to understand.
2. It made it easier to onboard new developers to the project
useSWR, like most open source projects, has great documentation. Rolling our own solution meant we needed to write documentation and teach developers new to the project how to deal with data fetching. Now that we use SWR, we don’t have to do this.
3. It makes the hard things easy
Our application, like most applications out there, has lots of API calls. Some of those API calls depend on the results of other API calls. With useSWR, it’s easy to write hooks for dependant fetching.
4. Perceived performance has improved
The app looks and feels snappier. Users appreciate this, and the feedback has been good.
5. It refreshes stale data
useSWR refreshes stale data on focus. This means our users always have the most up to date version of their data, without the loading times.
#SWR Conclusion
useSWR has had a huge impact on our application. It simplified our code and bettered our user experience. I can’t think of another library that was this easy to implement and offered benefits as useSWR. For more information about useSWR, be sure to check out both their website and their Github repository.

## The app
Testing app - it's a common todo list where we can able add, delete and check our todo items.
![image](https://user-images.githubusercontent.com/99946293/154915898-ee6444aa-a642-4027-b53b-1faba89ec24f.png)

## Steps to measure perfomance:
1. Add item
2. Check item
3. Delete item

## Lighthouse Perfomance almost similiar for both apps
![image](https://user-images.githubusercontent.com/99946293/154919646-f07dc889-d46f-44b4-a341-ae09f2dfbb16.png)


## General Perfomance
- Redux ![image](https://user-images.githubusercontent.com/99946293/154921310-14eff50d-df51-4d5f-9490-e28aadbbea30.png)

- SWR ![image](https://user-images.githubusercontent.com/99946293/154921372-a9296a26-c034-46b5-9390-78b83e80f6d5.png)

