# Find Tuya Data Points
Tuya devices use a custom `manuSpecificTuya` cluster. Within the reported values of this cluster's data is a dp (so called “Data Point ID”) which is at the core of Tuya devices. From the point of view of a device the DPIDs are the functions that the device provides. The instructions below will help you use the Tuya IoT Platform with a Tuya gateway to determine the functions of the datapoints which, will later assist in the creation of a device converter.

## Requirements and caveats
1. You will need an up-to-date version of Google Chrome (other browsers may work but, instructions may differ)
2. You will require basic knowledge of using Chrome and its Dev Tools
3. You will need to sign up for the Tuya IoT Platform and bind your accounts (more details below)
4. You will require a Tuya Zigbee Gateway
5. You will need the Tuya app (Tuya Smart) installed on your mobile device

## Instructions
### 1. Standard part of the setup
Ensure that you have set up a Tuya account and bound your Zigbee device to the Tuya gateway (these instructions will assume this has already been done).

### 2. Signin up for Tuya IoT Platform
The Tuya IoT Platform is the backbone for how internet connected Tuya devices communicate back to the Tuya platform. It contains a suite of Application Programming Interfaces (API's) which allow for developers to embed the Tuya functionality within their own platforms.

Visit [Tuya IoT Platform](https://iot.tuya.com/) and sign up for a new account (if you don't already have one):

![01_sign_up](../../images/how_tos/tuya_dp/01_sign_up.png)

### 3. Select development plan
Once your account has been confirmed, use your new credentials to login to the Tuya IoT Platform. You will be greeted with a first time tutorial showing you around the platform. Once completed, you will be prompted to set up a Cloud Development Plan. Click on `Free Trial` - Please note, that unless you are doing millions of calls to your new service (which we won't be), the plan will be completely free, and auto-renews annually.

![02_development_plan](../../images/how_tos/tuya_dp/02_development_plan.png)

### 4. Confirm service purchase
Once you have selected the Free Trial plan, you will be taken to a confirm service purchase screen. Double check to make sure that the `TRIAL EDITION` option is selected, and the Total shows $0.00 then, click `Buy Now`.

![03_service_purchase](../../images/how_tos/tuya_dp/03_service_purchase.png)

### 5. Create a cloud project
Once you purchased your API service, click on `Cloud` in the side menu, `Development` in the sub-menu and then click on `Create Cloud Project`.

![04_create_cloud_project](../../images/how_tos/tuya_dp/04_create_cloud_project.png)

In the newly opened dialog box, fill in the details as required, enduring that the Development Method is selected as Smart Home, and the Data Center corresponds to the region that your Tuya account is associated with.

![05_project_creation](../../images/how_tos/tuya_dp/05_project_creation.png)

Once confirmed, a new dialog box will open. Ensure that the relevent Smart Home API services are populated in the right hand list.

![06_configuration_wizard](../../images/how_tos/tuya_dp/06_configuration_wizard.png)

### 6. Link your Tuya account with your new Tuya project
Once confirmed, you should be taken to your new Tuya project. Click on `Link Tuya App Account`, then `Add App Account`.

![07_link_tuya_account](../../images/how_tos/tuya_dp/07_link_tuya_account.png)

This should bring up a QR code. Go in to the Tuya app on your mobile device, click on `[+]` (as id you are adding a new device). At the top of the screen, you will see a scan barcode button `[-]`. Click the `[-]` button and give permissions to use the camera (if prompted). Scan the QR code with your mobile device, and your account should appear in the App Account List in the Tuya IoT Platform.

### 7. Find your devices
Click on the `All Devices` and find the device in-which you wish to find the Data Points. Click on `Debug Device`. If you do not find your device in the list, or the list is empty, plese check your project's region.

![08_devices](../../images/how_tos/tuya_dp/08_devices.png)

### 8. Display device logs
Click on the `Device Logs` tab, and you will see a list of all events that the device has sent to the Tuya platform. Ignore the Event Details section as this appears to be garbage.

![09_device_logs](../../images/how_tos/tuya_dp/09_device_logs.png)

### 9. Find your Data Point!!
Select the Data Point for-which you wish to find the ID for in the drop-down list above the events table. Open up Dev Tools by pressing `ctrl` + `shift` + `i` on your keyboard, or going to the `3-dot menu` at the top-right of the Chrome window->`More Tools`->`Dev Tools`. When Dev Tools is open, click on the `Network` Tab, then click the `Search` button in the Tuya IoT Platform window.

![10_dev_tools](../../images/how_tos/tuya_dp/10_dev_tools.png)

You should see a number of calls appear in the `Name` section of Dev Tools. The call that we are interested in it `list`. Click this, and scroll down in the right-hand pane until you see the `Request Payload` section. Within there, is a json encoded object which contains all of the data sent from the search function. One of the keys is labelled `code`. This `code` i.e. 112 is the value for your Data Point ID!

### 10. Rinse, and repeat!

You should now iterate through each of the Data Points that are available in the drop-down list. Once finished, follow the other How-To guides to map these Data Point's into converters.
