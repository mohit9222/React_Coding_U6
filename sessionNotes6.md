E6 P6 - TOPICS

Input search

> To track the value of the input box, we have to bind the value with the local state variable

- IMP - whenever the state variable updates, react triggers a reconciliation cycle(re-renders the component)

why does the input box not working?
const [searchText, setSearchText] = useState("");
<input
type="text"
placeholder="Search for Resturant"
value={searchText}
/>

<button
className="search-button"
onClick={() => {
console.log(searchText);
}}

> We have bind the value on line 12 to the state variable searchText and that is bind to the input box
> What ever value is there in the searchText variable, it will be there in the input box
> when the value of searchText is being changed it is bind to the input box which is the same value
> Input search text will not change untill the searchText value doesnt change
> for this we write a onChange handler over here

## When ever we change the LOCAL STATE VARIABLE , React Re-RENDERS the component
