E6 P5 - TOPICS

Conditional Rendering

> Rendering based on a certain condition is called as conditional rendering

Ternary Operator

return listOfResturants.length === 0 ? <Shimmer /> : (

<div className="body">
<div className="search">
.....
.....
</div>
</div>

why do we need a state variable?

> In Javascript it is not possible for the variable to dynamically change
> We need to use local state variables
> Thats why we use useState()

Building the login logout using useState

> Value of btnName changes but the state does not update

onClick={() => {

              btnName = "Logout";
              console.log(btnName);
            }}

> Here when we have btName = "login", Javascript doesnt know if the btnName has been updated or not

> Whenever state variable changes, react re-renders the component with the updated values
> React re-renders the entire component

Rendering a component

> Means it will call that entire component once again
> When we are calling the setState value in the onClick, react will re-render the entire component after the state has been
> updated with the new value

how are we modifying the const [state,setState] = useState() ?

> This is basically because the entire component is re-rendered and this const [state,setState] is a new variable

onClick={() => {
btnNameReact === "Login"
? setBtnNameReact("Logout")
: setBtnNameReact("Login");
}}

> If my btnNameReact is equal to "Login" then we need to change to Logout setBtnNameReact("Logout") else change to Login
