# WOW-LAB-HOL1264 - mvk@ca.ibm.com
- This is the instruction and links to the repository for the World of Watson LAB-HOL1264
- user: WOWHOL1264txx@gmail.com - (xx is the team number 01-10)
- pass: @WOWHOL1264 for all accounts (particle, bluemix and gmail)

### Step 1 - Deploy CarDashboard and Node-RED
- [CarDashboard](https://github.com/markusvankempen/WowHol1264-CarDash)
- [Node-RED](https://github.com/markusvankempen/WoWHoL1264-Node-RED)
Make sure you can launch both applications from Dashboard
### Step 2 - Configure Watson Conversation
- Save the json file to your desktop - [json file](https://raw.githubusercontent.com/markusvankempen/WowHol1264-CarDash/master/training/airfreshener.json)
 - Next go to watson conversation service and click "Launch" 
 - Import the json file you saved to your desktop
#### Launch the Watson Conversation service and import
 - Launch conversation service again from Dashboard
 - Click on the upper right corner of the dashboard card (thre dots, actions) 
 - Click "View Details"
 - Copy the Workspace ID
 - Go to Car Dashboard Application, 
 - Click Runtime and create User Defined Value at the bottom called "Workspace ID" no quotes 
 - Paste the workspace ID into the value field and click save
 - Test the conversation on the Dashboard
### Step 3 - Register devicestype and devices in the IoT Platform /Service
#### Launch the iot service 
#### for cardashboard 
- deviceType : "watson"
- deviceId : "speech"

Note down your token and iot org ID

- Update date and deploy your code:
- Go to Bluemix Dashboard, then select Edit Code, find the file: app.js and update with CarDashboard API Token and Orj ID
- Next, find the file: ui/js/api.js adjust the line of code which points to the name of your node-red instance (ie. var wsUri = 'ws://yourhostnamehere.mybluemix.net/toCarDashboard';)

#### for airfreshener 
- deviceType : "watson"
- deviceId : "airfreshener"

Note down your token and iot org ID

### Step 4 - Logon to particle.io 
Deploy you [code](https://raw.githubusercontent.com/markusvankempen/WowHol1264-CarDash/master/particle/airfreshener.json)

### Step 5 - Update the Photon code

### Step 6 / Extra - add feedback and context to Watson Conversation 

### Extra B -Create a Node-Red-Dashboard
