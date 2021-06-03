# Setup  

1. Install Twilio CLI following [these instructions](https://www.twilio.com/docs/twilio-cli/quickstart) 
1. Install the Infra Plugin for Twilio CLI 
```
$ twilio plugins:install plugin-twilio-infra
```
3. If you've never used the Twilio CLI with this project, create a new profile with 
```
$ twilio login
```
4. Login to the project using
```
$ twilio profile:use <profile name>
```
5. Add the following environment variables: 

* `CHAT_SERVICE_SID`
* `FLEX_WORKSPACE_SID`
* `SMS_TASK_CHANNEL_SID` 
* `EVERYONE_TASK_QUEUE_SID`
* `TWILIO_PHONE_NUMBER`
* `FLEX_PROXY_SERVICE_SID`

6. If you don't have an environment defined, use the following command
```
$ twilio infra:environment:new <environment name>
```
7. Deploy the solution using: 
```
$ TWILIO_AUTH_TOKEN=xxxxxx twilio infra:deploy
```
8. In the Twilio [Console Settings page for Flex](https://www.twilio.com/console/flex/settings) make sure that the "Enable Dialpad" is Enabled

# Usage 
1. In Flex click the dialpad button (next to the microhpne on the top right corner). At the bottom of the dialpad you will find the "Outbound SMS" section. 
1. Type the destination number and press on START
1. A new Task / Reservation is generated: Click the accpet button to accept and start chatting 
