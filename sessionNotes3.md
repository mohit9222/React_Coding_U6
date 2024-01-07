E6 P3 - TOPICS

useEffect()
Syntax of useEffect()
When will the useEffect callback function be called?
Fetching data in React

--

useEffect()

> Hook is a normal JS function which react gives us and has its own use cases
> useEffect comes from the react library as a Named Import - import { useEffect } from 'react';
> Syntax:

    useEffect(() => {
        // code
    },[]);

> A function which takes two arguments -

## Arrow function (Which is a callback function)

## Dependency array []

When will the useEffect callback function be called?

> The callback function will be called after the "component renders"
> When the component is rendered, after the completion of the rendering of the component, the callback in the useEffect
> is called

If we want to do something after rendering the component, we make use of useEffect();
As soon as it sees the callback function it saves it for it to be called after rendering the component

Fetching data in React

> Logic for fetching data in react is the same way how we do it in Javascript
> ? We make use of a method/function/ superpower called as "fetch()"

useEffect(() => {

},[]);

const fectData = async () => {
const data = await fetch("https://www.swiggy.com/dapi/restaurants/list/v5?lat=13.0632293&lng=77.58211849999999&is-seo-homepage-enabled=true&page_type=DESKTOP_WEB_LISTING
");
const json = await data.json();
}

fetch()

> Superpower that is given to us by the browser
> Superpower that a JS Engine has
> fetches data from the API
> Fetch will return a promise
> how we resolve a promise?

## Traditional way using .then, catch, and handling errors

## New Approach - async and await

CORS Issue(Policy)
Who is blocking us?

> Our browsers is blocking us to call an API from one origin to another origin when they dont match
> Swiggys API from localhost (mis-match)
> If there is an origin mismatch the browser blocks that API call

Need to render data from API

> As soon we get the data from the API we will put the data inside the SetListOfResturants
> As soon as the SetListOfResturants updates, React will re-render the component and update the UI with new data

This is not a good practice :
setListOfResturants(
json.data.cards[4].card.card.gridElements.infoWithStyle
.restaurants

Instead we should use Optional Chaining
json?.data?.cards[1]?.card?.card?.gridElements?.infoWithStyle
?.restaurants
);
