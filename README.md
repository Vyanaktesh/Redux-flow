# Redux-flow

![image](https://user-images.githubusercontent.com/68580579/218009491-1fd7c086-aade-43c8-a4cc-31bef0f65215.png)

# Introduction of Redux Flow
-	Redux is a JavaScript framework for managing state in an application
-	Redux follows one direction flow of data.
-	It starts in the view.View means the item on a screen that a user sees.
-	If a user clicks a button or types something in. This is called an action.
-	When an action happens we need to make sure to change what is displayed to the user.
-	That action is dispatched through a reducer function.
-	The reducer must receive the action object and based on that it will figure out what to change and how to make that change. This is how the state management works in Redux.
-	The reducer then pass new object back to the store.
-	The store holds the state. It then updates the state and gives it to the view to update

-	Create a authActionConstant.js file in actionConstants folder then export the constant Variables to this file,
file. Variables are must be in Upper_case and value is same as variable name. Variable names are unique.


 - export const UPDATE_USERNAME= 'UPDATE_USERNAME';

- export const UPDATE_PASSWORD= 'UPDATE_PASSWORD';

-	Next select the index.js file in actionConstants.js and add
-	export* from './authActionConstant';

•	Create a file in action and give name as authAction.js. In this file first import the Variables from './actionConstants' then export the action using arrow function syntax to dispatch the type to debugger.

![Screenshot 2023-02-09 173448](https://user-images.githubusercontent.com/68580579/218013207-93a80b04-274d-484a-8a0e-282f79a0cebf.png)

-	Create authReducer.js file in reducers and add

![Screenshot 2023-02-09 174516](https://user-images.githubusercontent.com/68580579/218015196-76381d5a-2c90-4530-98e1-d149165fad53.png)
![Screenshot 2023-02-09 174634](https://user-images.githubusercontent.com/68580579/218015355-3fa39748-3879-48c2-be6f-e69dab269015.png)
- In this program intialstate of both username and password  set to false.
-	Select rootReducer.js file. Add
- import authReducer from './authReducer'
-	And also add state to store
-  auth: authReducer.
  [UPDATE_USERNAME]: updateUsername,
    [UPDATE_PASSWORD]: updatePassword,
    [LOGIN_CLICKED]: loginClicked,
- CreatPingPongButton into components/Home folder.
