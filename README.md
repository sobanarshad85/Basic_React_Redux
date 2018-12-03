# Basic_React_Redux
This repository is to give an idea about how react native uses redux as it's temporarily database. In redux you can strore your data for manupulation inside the whole app. This is the basic structure of redux with react native. Hope you guys will enjoy the repo.
so lets talk about a very basic react native's redux based counter.
our goal is to acheive an app where we'll be having 2 buttons.
one is increase and second is decrease.
incresae button will count '+1' in output and decrease will count '-1' in output.
first of all while structuring you whole try to use a component inside App.js, in other cases you start your app from the file called App.js but in redux example you'll start your app from the component wrapped inside App.js
in my case i have made another component called CounterApp and imported inside App.js
why i had to do this, the reason is i wrapped the CounterApp with 'Provider' so that through out my app our store is available to us.
In provider i provide the store as well, as you can see.
so, first of all make a store where all your data/state will be saved.
the second thing is to make a reducer, what it does, it is responsible of handling your action and taking/giving data from store.
reducer will take 2 argument, first is initial state and the second one is action, like which action you want to perform.
inside reducer you can check in switch condition or whatever you like, which action is what.
ok so fine upto here,
now goto CounterApp.js
there you can see at the bottom
i used connet, what is does it'll combine your component with your props for store and action accordingly
export default connect(mapStateToProps)(mapReducerToProps)(YourComponent);
inside your mapStateToProps(state) this argument state is coming form your store, 
your can set any propo using state.something, something=anything present in your store most likely as your initial state.(not necessarily)
as in our examply i set it as counter:state.counter, as you can see in App.js file i set couter:0 as my initial state.
ok now lets go to mapReducerToProps(dispatch) here we make our actions. as i made 2 action, 1 is increaseCounter and 2 is decreaseCounter.
increaseCounter:()=>dispatch({type:'INCREASE_COUNTER})
then i set these two actions with the buttons as you can check in CounterApp => TouchableOpacity => onPress={()=>this.props.increaseCounter()}
this is all that you need to learn for the basics of React using Redux
hope you enjoyed.

for any queries you can contact

//Developed by Soban Arshad
  //sobanarshad85@gmail.com
  //+92 303 4645 060
  //https://www.facebook.com/sobanarshad85
  //https://www.twitter.com/sobanarshad85
  //https://www.github.com/sobanarshad85
  //https://www.linkedin.com/in/sobanarshad85
