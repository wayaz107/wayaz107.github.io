---
layout: post
title:      "State vs Props in React"
date:       2021-05-12 11:40:08 +0000
permalink:  state_vs_props_in_react
---


The state and props have differences but are also closely related. Let's start by defining them:

The state is an instance of a React Component Class that can be described as an object of noticeable properties that manage the behavior of the component. In general, the state component is an object that holds some information that can change during the lifetime of that component.

For example:

class User extends React.Component {

state = {
username: '',
password: "
}

changeHandler = (e) => {
this.setState({[e.target.name]:  e.target.value })
}

render (){
  return(
	 <form>
	 <input type="text"  value={this.state.username} onChange={this.changeHandler} />
	 	 <input type="text"  value={this.state.password} onChange={this.changeHandler} />
	 
	 </form>)}
	 
	 This User component holds the state of the username and password properties. The values of the form in the render method are set to display the state of the username and password respectively. When the component initially mounts the state of the username and password is just empty strings. The changeHandler function sets the state of username and password anytime there is a change in the input field. Whenever setState is classed, the component is then re-rendered, which updates the text being displayed in the input fields. The state of the User component is an object that holds information that can change overtime. 
	 
Props refers to properties. Its mainly used for passing down data from one component to another. For example:

class ProductsContainer extends React.Component{


    render() {
        return (
            <div>
                <Wish_List products={products}/>
						</div>
					)}
			}
			
				
The component is rendering a child component called Wish List and passing it a prop called products. The child component can then use this prop. 

In summary, the difference between prop and state is that prop is used to pass down data while state is used to store data. Though there are clear differences between the two, it' s also important to note that they are also related. State of one component can be passed down to child components as props. 

For example: 

<Product path="/posts" render={() => <ProductContainer productArray={this.state.productArray}/>} />

This example shows, state of a component productArray being passed down to a child component. 


Important thing to note is that is that the prop is immutable, meaning it can't be changed. If it needs to be changed, the parents should just change its own state which would then update the prop that was passed down to the child. If the child needs to change its props, this instance is usually handled through child events and parent callbacks. A parent would pass down a function to the child, that the child would reference when a specific event happens. When that event occurs the child references the event, which then lets the parent component know to change the state of the data it’s passing down to its child and automatically triggers a re-render with the new data for the child component. These are the ways state and props are used in React and it’s important for any developer to understand how these tools differ and relate to one and other.
