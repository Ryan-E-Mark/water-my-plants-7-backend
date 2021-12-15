# API For Water My Plants App

A web app that allows users to track the watering schedule of their plants by creating an account and posting, updating, or deleting plants to the library.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## User Endpoints

### --Register--

https://water-my-plants-7-ft.herokuapp.com/api/users/register
To create a new user, you'll submit a post request to this url, the object you'll send the API will include a username and password. I don't have it set up to store a phone number at the moment, if that's a feature we want I can do that pretty easily.
Upon successful registration the response from the API should show a user_id, username, and your encrypted password.

### --Login--

https://water-my-plants-7-ft.herokuapp.com/api/users/login
To login, submit a post request to this url containing an object with the same username and password you registered.
Upon successful login the response from the API should include a token that you can save to local storage for later authorization.

### --Updating User Information--

Submit a put request to https://water-my-plants-7-ft.herokuapp.com/api/users/:id with the id of the user you'd like to update in the url. In the body of the request, send the updated username / password / phoneNumber
On a successful update the API will respond with the updated user info

### --Logout--

https://water-my-plants-7-ft.herokuapp.com/api/users/logout
To logout, submit a get request to the url.
It will check to see if you have a token saved in local storage and if so will respond with "successfully logged out" but the removing of the token occurs on the client side by deleting it from local storage

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Plants Endpoints

### --Post New Plant--

https://water-my-plants-7-ft.herokuapp.com/api/plants
To create a new plant, you'll submit a post request to this url, the object you'll send the API will include a nickname, species, and h20frequency, image(optional)
Upon successful registration the response from the API should show a plant_id, nickname, species, h20frequency, and image (image is optional if you want to include a url of the plant)

### --Get All Plants--

https://water-my-plants-7-ft.herokuapp.com/api/plants
To get a list of all plants submit a get request to this url

### --Get Plant by ID--

https://water-my-plants-7-ft.herokuapp.com/api/plants/:id
to get a specific plant, send a get request to this url with the id of the plant you're looking for in place of the :id at the end of the url
If a plant with that id exists, you should get it back in the response from the API

### --Updating Plant Information--

Submit a put request to https://water-my-plants-7-ft.herokuapp.com/api/plants/:id with the id of the plant you'd like to update in the url. In the body of the request, send the updated nickname / species / h20frequency / etc.
On a successful update the API will respond with the updated plant info

### --Deleting Plant--

Submit a delete request to https://water-my-plants-7-ft.herokuapp.com/api/plants/:id with the id of the plant you'd like to delete.


