# Friday

Friday is an Home Assistant you will be building as part of your interview round. Friday is a mobile app that keeps track of your room's appliances and their statuses. (ON/OFF)

## Friday Capabilities 

* Users (your roommates) can register themselves and login with username and password.
  * The Login and Registration functionality should be implemented using AWS Cognito Service.
  * The user should recieve an OTP over his/her email during the registration process. 
* The primary interaction within the app would be a Bottom Navigation Menu having tabs Appliances, Users and Settings.  
  * Once the user in logged in, he should be in the Appliances Tab where a list of cards with Appliance names as text on them should be displayed from an array. An example of the appliances array is given below.
  * ```[{"appliance_name": "Light", "appliance_status": "On"}, {"appliance_name": "Fan", "appliance_status": "Off"}, {"appliance_name": "Study Lamp", "appliance_status": "Off"}]```
  * Rest of the Tabs (Users Tab and Settings Tab) would have only an heading text showing which tab the user is in.
* Users should be able to delete and update the Appliance List and when they do, the updated appliance list should be reflected in all the other users appliances tab.
  * Now the App should be integrated with AWS DynamoDB in order to get the appliance list of the logged in user. The above appliances array should be retrieved from DynamoDB Table.
  * Add a Floating Action Button in the Appliances Tab Screen for adding a new appliance.
  * For deleting an appliance the user should touch and hold the respective appliance cars on the screen.
* On clicking the appliance, the card should be highlighted (indicating the toggle of appliance state) and that state of the card should be updated on the DynamoDB.
  * Make sure that any change made by the user (Add, Delete, Toggle Appliance) is reflected in the Database as well as to other users who are logged in.

## Application UX Design

### Login Screen

* You can use AWS Cognito's UI Component to render the Login and Registration Screens of the App.

### Appliance Tab Screen

![picture alt](http://via.placeholder.com/200x150 "Title is optional")


