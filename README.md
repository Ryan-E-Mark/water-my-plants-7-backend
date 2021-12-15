# API For Water My Plants App
A web app that allows users to track the watering schedule 

## User Endpoints

### --Register--

https://water-my-plants-7-ft.herokuapp.com/api/users/register
To create a new user, you'll submit a post request to this url, the object you'll send the API will include a username and password. I don't have it set up to store a phone number at the moment, if that's a feature we want I can do that pretty easily.
Upon successful registration the response from the API should show a user_id, username, and your encrypted password.

### --Login--

https://water-my-plants-7-ft.herokuapp.com/api/users/login
To login, submit a post request to this url containing an object with the same username and password you registered.
Upon successful login the response from the API should include a token that you can save to local storage for later authorization.

### --Logout--

https://water-my-plants-7-ft.herokuapp.com/api/users/logout
To logout, submit a get request to the url.
It will check to see if you have a token saved in local storage and if so will respond with "successfully logged out" but the removing of the token occurs on the client side by deleting it from local storage


## Plants Endpoints



## Starting a New Project


