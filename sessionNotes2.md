E6 P2 - TOPICS

What are the different approaches web applications fetch data from the backend?
Why is the approach selected better in React?

---

- It is a good practice to fetch data from the api and not from the hard coded data.

What are the different approaches web applications fetch data from the backend?

## APPROACH I

> When our app loads, When to make a API Call?

          (PAGE LOADS)     -->        (API CALL)         -->        (RENDER)

> As soon as the page loads --> Then we make the Api call - {Wait for the data}-> Then we render the UI
> The App/page loads, it takes 500 ms and then the data is shown on the screen
> We initially dont see anything on the UI for 500 ms and then suddenly we see something (Poor UX)

## APPROACH II

          (PAGE LOADS)     -->        (RENDER)    -->     (API CALL)     -->    (RERENDER)

> As soon as the page loads --> We will quickly render what ever is available (the skeleton) -->
> Then we make the Api call - {Wait for the data}-> Then we re-render the UI

> In React we will always be using APPROACH II - Better Approach / Better UX

## WHY APPROACH II?

Better UX
React is very fast in rendering cycle
