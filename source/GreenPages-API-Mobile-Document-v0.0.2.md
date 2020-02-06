--- 

title: Documentation GreenPages API 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

## GreenPages API Documentation
  This documentation aim to describe the API used in GreenPages application.
  Through API digital provide,user can manege their personal data, display organizational structure data,
  and can also display news. Actions that users can take are to add, update, view and delete data.

## Response Message

  When the API is run the response will appear according to the condition that accur.
  The response that will appear when running the API in the personal account model are:

  - 200 : OK
  - 201 : Create
  - 400 : Bad Request
  - 401 : Unauthorized
  - 403 : Forbidden
  - 404 : Not Found

## Example Of Request And Response
  As an example of a request  a user can do is display data using the API with the GET method.
  The following is endpoint view for the GET method.

     https://myplatform-dev.myindo.io/api/account/v0.0.1/personal/personalAddress/me

  The endpoint will appear as a response about the list of personal address data, all personal address data that has been added by the user will be appeared.
  Example for response that will be appeared are as follows :

        {
           "errors": [],
           "warnings": [],
           "data": {
             "personalAddressList": [
               {
                 "id": "a057ec91-5592-49f3-9e69-12fabe0d500e",
                 "name": "Rumah",
                 "address1": "Jl. Radio I No.21, RT.3/RW.4, ",
                 "address2": "",
                 "address3": "",
                 "countryId": "jakarta",
                 "provinceId": "province",
                 "cityId": "city",
                 "subDistrictId": "subDistric",
                 "villageId": "test",
                 "postCode": "12345",
                 "telp": "12345435555",
                 "handphone": "12345435555",
                 "sortSeq": 100
               },
               {
                 "id": "a49f48a7-d817-4f58-ac98-bcf36934d1d5",
                 "name": "Rumah",
                 "address1": "Jl. Radio I No.21, RT.3/RW.4, ",
                 "address2": "",
                 "address3": "",
                 "countryId": "jakarta",
                 "provinceId": "province",
                 "cityId": "city",
                 "subDistrictId": "subDistric",
                 "villageId": "test",
                 "postCode": "12345",
                 "telp": "0219087654",
                 "handphone": "081311053950",
                 "sortSeq": 100
               }
             ]
           },
           "dictionaries": {
             "params": {}
           }
         }

### Authorized
  Before users can use the API to be able to access the features available on GreenPages.
  The user must first registration using the API available on the Personal Account with the following endpoints:

     https://myplatform-dev.myindo.io/api/account/personal/v1.2.0/public/account/register

  For can do registration, parameter that be used is token. the response that will be results there are:

           {
               "errors": [],
               "warnings": [],
               "data": {
                   "personalAccountRegister": "success register"
               },
               "dictionaries": {}
           }

### E-Membership

  E-membership contains the user's personal data. users can manage personal profile data.
  in GreenPages application, users can manage (add, update, delete). Personal data available in the profile menu.
  There is data that can be manage by the users such as:

#### Personal Detail

   Personal identity is personal data that can be added, modified or deleted by the users.
   As for the type of identity that can be added are its cards, passports, visas, driving licenses, telephone
   the first time user log in, the personal identity data that will be filled in automatically that is
   email data and phone number and both of these data can not be deleted because the data is mandatory but the user  can still changes both.
   To increase data security and confidentiality, masking of data for personal identity is carried out.
   Users can manage the personal identity data by adding, changing and deleting data.
   For users who activate the pin to manage or view data, the user have to first enter the pin code in accordance with pin code has been created.
   The steps that users can take to manage data are as the follows :

   Step to add data
   - Click the personal identity feature. In the profile data menu, click on personal identity and then click the "Add" button.
   - Add personal identity data. The user can fill in the data added forms available, the data that needs to be added is the identity and card number.
     When filling in the user's identity will be given the option of the type of identity to be added. After that the user can fillin the chosen identification number.
     If all the data has been filled in correctly, then click the "save" button and a notification of personal identity has been successfully added will appear.
     To add data there is no maximum number of conditions to be added.

  Steps for editing data
  - Click personal identity. Feature to modify identity data click the personal identity feature then select the data to be modified.
  - Click the edit icon. In the editing process there are two conditions that can be done by the user, namely changing data or deleting data.
    After clicking the edit icon, a page to update your personal identity will appear with the option of updating or deleting actions.
    If the user only wants to change the data that has been previously saved, the user can change the old data with new data without no data being empty.
    After completing the data change, click the "Change" button and notification of the personally edited identity data will appear.
    But if the user wants to delete the data, the user can click the "Delete" button and notification of the personally deleted personal data will appear.

#### Personal Card

  The personal card feature allows users to add, change and delete personal card data.
  Types of personal cards that can be added are BPJS employment, and accounts. To increase data security and confidentiality,
  masking of data for personal cards is carried out. Users can process personal card data by adding, changing and deleting data.
  For users who enable the pin to be able to process or view data, the user must first enter the pin code in accordance with the pin code that has been created.
  The stages that users can take to be able to process data are as follows:

  Step to add data
  - Click personal card features. On the profile data menu, click personal card then click 'Add' button.
  - Add personal card data. The user can fill in the available personal card forms, the required data
    added are card type and card number. When filling in card types, the available options are
    BPJS health cards, occupations and BPJS accounts. Then fill in the card number of the selected card type.
    If all data has been filled in correctly then click the "Save" button and a notification will appear that the data has been successfully added.
    For additional data, there is no provision for the maximum amount to be added.

  Step for editing data
  - Click personal card feature. To be able to make changes to personal card data, click the personal card feature then select the data to edit.
  - Click the edit icon. in the editing process there are two conditions that can be done, namely making data changes or deleting data.
    After clicking the edit icon, a personal card data change page will appear with the replace and delete action options.
    If the user only wants to make changes to data that has been previously saved, users can change old data with new data without any data being emptied.
    After completing changes to the data, click the 'Change' button and a confirmation will appear that the data was changed successfully.
    But if the user wants to delete data, the user can click the 'Delete' button and a notification will appear that the data was successfully deleted.

#### Family Data

  In the family feature, users can add, change, and delete family data. The family data needed for the GreenPages application is identity
  (the type of identity that can be added is resident identification card, passport, visa, driver's license, cellphone, telephone),
  identity number, relationship, first name, middle name, last name, gender, status, religion, date of birth, place of birth, education,
  occupation, information. Users can add, change and delete family data. The steps that users can take to manage family data are as follows:

  Step to add data
  - Click family features. On the profile data menu, then click the family features and click the 'Add' button.
  - Add family data. Users can fill in data on the form added family that has been provided.
    If all data has been filled in correctly then click the 'Save' button and a notification will appear that the data was added successfully.

  Step for editing data
  - Click family features. To be able to make changes to family data, click the family feature then select the data to edit.
  - Click the Edit Icon. In the editing process there are two conditions that can be done namely making changes to data or deleting data.
    After clicking the edit icon, the change family data page will appear with the change and delete action options.
    If the user only wants to make changes to the data that was saved before, the user can change the old data with the new data without any data being emptied.
    After completing changes to the data, click the 'Change' button and a notification will appear that the data has been changed successfully.
    But if the user wants to delete the data, the user can click the 'Delete' button and a notification will appear that the data was deleted successfully.

#### Address Data

  In the address feature, users can add, change, and delete address data. Address data required
  in this GreenPages application are address categories (home, office, apartment, shop), address, city, district, postal code,
  kelurahan / village, province, country, telephone number, cellphone number. Users can manage address data by making additions,
  changes and deleting data. The stages for managing address data are as follows:

  Step to add data
  - Click the Address Feature. On the profile data menu, click the Address feature and then click the 'Add' button.
  - Add Address Data. Users can fill in the address data on the form plus the address provided.
    If all data has been filled in correctly then click the 'Save' button and a notification will appear that the data was added successfully.

  Step for editing data
  - Click address features. To be able to make changes to address data, click the address feature then select the data to edit.
  - Click the edit icon. In the editing process there are two conditions that can be done, namely making data changes or deleting data.
    After clicking the edit icon, the change family data page will appear with the change and delete action options.
    If the user only wants to make changes to the data that was saved before, the user can change the old data with the new data without any data being emptied.
    After completing data changes, click the 'Change' button and a notification will appear that the data has been changed successfully.
    But if the user wants to delete the data, the user can click the 'Delete' button and a notification will appear that the data was successfully deleted.

#### Education Data

  In the education feature, users can add, change and delete address data.
  Educational data needed on this GreenPages application are name of institution, department, institution accreditation,
  grade / ipk, address, starting education, completion of education, description.
  Users can process educational data by adding, changing and deleting data. The steps that can be taken to process educational data are as follows:

  Step to add data
  - Click educational features. On the profile data menu, click the education feature then click the 'Add' button.
  - Add education data. Users can fill out education data on the form added education that has been provided.
    If all data has been filled in correctly then click the 'Save' button and a notification will appear that the data was added successfully.

  Step for editing data
  - Click educational features. To be able to make changes to educational data, click the education feature then select the data to edit.
  - Click the edit icon. In the editing process there are two conditions that can be done, namely making data changes or deleting data.
    After clicking on the edit icon, a page will change the educational data with action options change and delete. If the user only wants
    to make changes to the data that was saved before, the user can change the old data with the new data without any data being emptied.
    After completing changes to the data, click the "Change" button and a notification will appear that the data has been changed successfully.
    But if the user wants to delete data, the user can click the "Delete" button and a notification will appear that the data was deleted successfully.


#### Skill Data

  In the skill data feature the user can add, change and delete skill data. The skill data needed on this GreenPages application is the area of skill,
  name of skill, description, skill level, start date, end date. Users can process skill data by adding, changing and deleting data.
  The steps that can be taken to be able to process skill data are as follows:

  Step to add data
  - Click skill feature. On the profile data menu, click the skill feature then click the 'Add' button.
  - Add skill data. Users can fill in the expertise data on the form added expertise that has been provided.
    If all data has been filled in correctly then click the 'Save' button and a notification will appear that the data was added successfully.

  Step for editing data
  - Click skill Feature. To be able to make changes to the expertise data, click the expertise feature then select the data to edit.
  - Click the edit icon. In the editing process there are two conditions that can be done, namely making data changes or deleting data.
    After clicking the edit icon, the change expertise data page will appear with the change and delete action options.
    If the user only wants to make changes to the data that was saved before, the user can change the old data with the new data without any data being emptied.
    After completing data changes, click the 'Change' button and a notification will appear that the data has been changed successfully.
    But if the user wants to delete the data, the user can click the 'Delete' button and a notification will appear that the data was successfully deleted.

#### Work Experience Data

  In the work experience feature the user can add, change and delete work experience data. Work experience data needed on this GreenPages application are company name, position,
  description, address, portofolio link, name reference, telephone reference, start date. Users can do data processing
  work experience by adding, changing and deleting data. The stages that users can take to be able to process data are as follows:

  Step to add data
  - Click the work experience feature. On the profile data menu, click the work experience feature then click the 'Add' button.
  - Add work experience data. Users can fill in data on the form plus work experience data that has been provided.
    If all data has been filled in correctly then click the 'Save' button and a notification will appear that the data was added successfully.

  Step for editing data
  - Click the work experience Feature. To be able to make changes to work experience data,
    click the work experience feature then select the data to edit.
  - Click the edit icon. In the editing process there are two conditions that can be done, namely making data changes or deleting data.
    After clicking the edit icon, a change work experience data page will appear with the change and delete action options.
    If the user only wants to make changes to data that has been previously saved, the user can change the old data with new data without any data being emptied.
    After completing data changes, click the 'Change' button and a notification will appear that the data has been changed successfully.
    But if the user wants to delete the data, the user can click the 'Delete' button and a notification will appear that the data was deleted successfully.

#### Organization Data

  In the organizational features users can add and view organizational data. Organizational data has two categories namely PBNU Organizations
  and Non-PBNU Organizations. From these two categories there are differences in the data needed when filling out the form added to organizational data.
  PBNU Organization Data needed is the name of the organization (the user can choose the organization), member code, position, description,
  organization address, start date, end date. whereas for filling out Non-PBNU Organization data, the data required is the name of the organization,
  position, description, address of the organization, start date, end date. Organization data that has been successfully added cannot be changed,
  users can only view e-membership data. The stages that users can take to add organizational data are as follows:

  Step to add data
  - Click Organization Features. On the data profile menu, then click organization features.
    Users can choose to add PBNU or Non-PBNU Organization data then click the 'Add' button.
  - Add Organization Data. Users can fill in organizational data in the form added organization that has been provided.
    If all data has been filled in correctly then click the 'Save' button and a notification will appear that the data was added successfully.

### Direktory

  The directory containing the API that will be used to view the NU Organization Data structure.

  - List of Central Organizations = to show list of NU organization data with Type is Central
  - Organization Type Tree = to display the organization menu in the directory menu
  - organization tree = to display the organization list
  - Organization Structure Tree Id = to display the organizational structure
  - List of Organizational Management = to display organizational management data
  - Contact Organization Address = to display contact data and organization address
  - Organization Search = to display search data by name as a parameter

### News
  News containing the API will be used to view news on the GreenPages Application.
 

**Version:** 0.0.1 

# /PERSONALORGANIZATION/ORGANIZATIONINFO/LIST
## ***GET*** 

**Summary:** Personal organization list

**Description:** This API is used to show the list of PBNU organizational data with the ID of each organization. Organization ID is required when adding organizational data to the NU category.


### HTTP Request 
`***GET*** /personalOrganization/organizationInfo/list` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALORGANIZATION/ADD/ME
## ***POST*** 

**Summary:** Personal organization add for nu

**Description:** This API is used to add NU organizational data followed by users. The organizational category that can be added is NU organization.


### HTTP Request 
`***POST*** /personalOrganization/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| type | query |  | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALORGANIZATION/ADD/ME/
## ***POST*** 

**Summary:** Personal organization add for nonNu

**Description:** This API is used to add Non NU organizational data followed by users, the organizational category that can be added is the NU organization.


### HTTP Request 
`***POST*** /personalOrganization/add/me/` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| type | query |  | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALORGANIZATION/ME
## ***GET*** 

**Summary:** Get data personal organization

**Description:** This API is used to appear all details of data from organizations that have been added by users (NU organizations and Non NU organizations).


### HTTP Request 
`***GET*** /personalOrganization/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALORGANIZATION/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal organization

**Description:** This API is used to update organizational data that has been added previously. The parameter used is the ID of the data to be changed.


### HTTP Request 
`***PUT*** /personalOrganization/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query |  | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALORGANIZATION/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data personal organization

**Description:** This API is used to delete organizational data by using the organization ID to be deleted as a parameter.


### HTTP Request 
`***DELETE*** /personalOrganization/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query |  | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALIDENTITY/ME
## ***GET*** 

**Summary:** Get data personal identity

**Description:** This API is used to appear personal identity data that has been previously added by user.


### HTTP Request 
`***GET*** /personalIdentity/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALIDENTITY/ADD/ME
## ***POST*** 

**Summary:** Add new data personal identity

**Description:** This API is used to add user's personal data, as for the data that can be added are :
  1. Personal identity
      - identity card
      - passport
      - visa
      - driver's license
      - telephone
  2. Personal Card
      - Health Social Security Organizing Agency (BPJS)
      - Social Security employment agency (BPJSTK)
      - Bank Account


### HTTP Request 
`***POST*** /personalIdentity/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Ok |
| 403 | Forbidden |
| 404 | Not found |

# /PERSONALIDENTITY/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal identity

**Description:** This API is used to change personal data of user's that have been added previously.


### HTTP Request 
`***PUT*** /personalIdentity/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query |  | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALIDENTITY/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data personal identity

**Description:** This API is used to delete personal identity data by using the personal ID to be deleted as a parameter.


### HTTP Request 
`***DELETE*** /personalIdentity/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query |  | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALIDENTITY/DECRYPT/ME
## ***GET*** 

**Summary:** Get data personal identity decrypt

**Description:** This API is used to appear user identity data that has been masked.


### HTTP Request 
`***GET*** /personalIdentity/decrypt/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query |  | Yes |  |
| pin | query |  | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALIDENTITY/SECURED/PIN
## ***PUT*** 

**Summary:** Get data personal identity secured pin

**Description:** This API is used to set pins that can only be done by users. The pin is used to provide multiple security for the user's personal data the provisions for making pins are :
  - Maximum 8 characters
  - pin can only be filled in with numbers

* note * : there is no feature to forget pin, so it is hoped that all users always remember that a pin has been created


### HTTP Request 
`***PUT*** /personalIdentity/secured/pin` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 400 | Bad Request |
| 403 | Forbidden |

# /PERSONALIDENTITY/SECUREDUPDATE/PIN
## ***PUT*** 

**Summary:** Get data personal identity update pin

**Description:** This API is useful for changing previously created pins. the steps to make a pin change are :
   1. insert the old pin
   2. enter the new pin code
   3. confirm the new pin code


### HTTP Request 
`***PUT*** /personalIdentity/securedUpdate/pin` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 400 | Bad Request |
| 403 | Forbidden |

# /PERSONALIDENTITY/UNSECURED/PIN
## ***PUT*** 

**Summary:** Get data personal identity unsecured pin

**Description:** This API is used to cancel a pins that was created before. the steps that need to be taken to cancel a pin are insert pin on cancel pin form, then click *save*, the pin will be successfully canceled.


### HTTP Request 
`***PUT*** /personalIdentity/unsecured/pin` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 400 | Bad Request |
| 403 | Forbidden |

# /PERSONALADDRESS/ADD/ME
## ***POST*** 

**Summary:** Add new data personal address

**Description:** This API is used to add user address data, the address categories that can be added are :
  - House
  - Office
  - Apartment
  - Shop house


### HTTP Request 
`***POST*** /personalAddress/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALADDRESS/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal address

**Description:** This API is used to update address data that has been added previously.


### HTTP Request 
`***PUT*** /personalAddress/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALADDRESS/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data personal address

**Description:** This API is used to delete personal address data by using the personal address ID to be deleted as a parameter.


### HTTP Request 
`***DELETE*** /personalAddress/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALADDRESS/ME
## ***GET*** 

**Summary:** Get data personal address

**Description:** This API is used to appear personal address data that has been added by the users.


### HTTP Request 
`***GET*** /personalAddress/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALCONFIG/ME
## ***GET*** 

**Summary:** Get data personal config

**Description:** This API is used by users to add configurations of e-membership data, such as whether users enable pins or not.


### HTTP Request 
`***GET*** /personalConfig/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALEDUCATION/ADD/ME
## ***POST*** 

**Summary:** Add new data personal education

**Description:** This API is used to add user education data.


### HTTP Request 
`***POST*** /personalEducation/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 403 | Forbidden |
| 404 | Not found |

# /PERSONALEDUCATION/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal education

**Description:** This API is used to change user education data that has been added previously.


### HTTP Request 
`***PUT*** /personalEducation/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALEDUCATION/ME
## ***GET*** 

**Summary:** Get data personal education

**Description:** This API is userd to display educational data that has been added by the user.


### HTTP Request 
`***GET*** /personalEducation/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not found |

# /PERSONALEDUCATION/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data personal education

**Description:** This API is used to delete educational data by using the personal education ID to be deleted as a parameter.


### HTTP Request 
`***DELETE*** /personalEducation/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALWORK/ADD/ME
## ***POST*** 

**Summary:** Add new data personal work

**Description:** This API is used to add user work experience data.


### HTTP Request 
`***POST*** /personalWork/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALWORK/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal work

**Description:** This API is used to change user work experience data. The parameter used to change the user's work experience using the data ID to be changed.


### HTTP Request 
`***PUT*** /personalWork/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALWORK/ME
## ***GET*** 

**Summary:** Get data personal work

**Description:** This API is used to display personal work data that has been previously added by the user.


### HTTP Request 
`***GET*** /personalWork/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALWORK/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data personal work

**Description:** This API is used to delete personal work data by using personal work ID that will be deleted as a parameter.


### HTTP Request 
`***DELETE*** /personalWork/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONAL/ME
## ***GET*** 

**Summary:** Get data personal

**Description:** This API is used to display user identity data in detail.


### HTTP Request 
`***GET*** /personal/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONAL/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal

**Description:** This API useful for changing on user identity data.


### HTTP Request 
`***PUT*** /personal/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONAL/UPDATENAME/ME
## ***PUT*** 

**Summary:** Update name personal

**Description:** This API is used to change user names, the name will be shown on the profile.


### HTTP Request 
`***PUT*** /personal/updateName/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALSKILL/ADD/ME
## ***POST*** 

**Summary:** Add new data personal skill

**Description:** This API is used to add user skill data.


### HTTP Request 
`***POST*** /personalSkill/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALSKILL/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal skill

**Description:** This API is used to change previous user's skill data. The process of changing data uses the skill ID to be updated as a parameter.


### HTTP Request 
`***PUT*** /personalSkill/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALSKILL/ME
## ***GET*** 

**Summary:** Get data personal skill

**Description:** This API is used to display personal skills data that has been added by the user.


### HTTP Request 
`***GET*** /personalSkill/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALSKILL/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data personal skill

**Description:** This API is used to delete personal skill data by using the skill ID to be deleted as a parameter.


### HTTP Request 
`***DELETE*** /personalSkill/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALFAMILY/ADD/ME
## ***POST*** 

**Summary:** Add new data personal family

**Description:** This API is used to add user family data.


### HTTP Request 
`***POST*** /personalFamily/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALFAMILY/UPDATE/ME
## ***PUT*** 

**Summary:** Update data personal family

**Description:** This API is used to change user family data that was added previously.


### HTTP Request 
`***PUT*** /personalFamily/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALFAMILY/ME
## ***GET*** 

**Summary:** Get data personal family

**Description:** This API is used to display family data from users.


### HTTP Request 
`***GET*** /personalFamily/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderBy | query | Order By | Yes |  |
| sortBy | query | SortBy | Yes |  |
| page | query | Page | Yes |  |
| size | query | Size | Yes |  |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALFAMILY/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data personal family

**Description:** This API is used to delete user family data by using the personal family ID to be deleted as a parameter.


### HTTP Request 
`***DELETE*** /personalFamily/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /PERSONALREFERRER/ME
## ***GET*** 

**Summary:** Get data personal referrer

**Description:** This API is used to display the user's referral code.


### HTTP Request 
`***GET*** /personalReferrer/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /ACCOUNT/REGISTER
## ***GET*** 

**Summary:** Get data account register

**Description:** This API is used to register new token.


### HTTP Request 
`***GET*** /account/register` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANY/ME
## ***GET*** 

**Summary:** Get data company

**Description:** This API is used to display company data that has been added previously by the user.


### HTTP Request 
`***GET*** /company/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANY/ADD/ME
## ***POST*** 

**Summary:** Add new data company

**Description:** This API is used to add company data owned by users to add companies, users need to enter criteria and types of companies they have.


### HTTP Request 
`***POST*** /company/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANY/UPDATE/ME
## ***PUT*** 

**Summary:** Update data company

**Description:** This API is used to update information from companies that are owned by users.


### HTTP Request 
`***PUT*** /company/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANY/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data company

**Description:** This API is used to delete company data that has been added previously.


### HTTP Request 
`***DELETE*** /company/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANYPRODUCT/ME
## ***GET*** 

**Summary:** Get data company product

**Description:** This API is used to display product data available from companies owned by user.


### HTTP Request 
`***GET*** /companyProduct/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| companyId | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANYPRODUCT/ADD/ME
## ***POST*** 

**Summary:** Add new data company product

**Description:** This API is used to add product data from companies owned by users, using this API, users can add product data details such as : product name, product total, product price, product unit, product weight, product description. users can also add the product images.


### HTTP Request 
`***POST*** /companyProduct/add/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Create |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANYPRODUCT/UPDATE/ME
## ***PUT*** 

**Summary:** Update data company product

**Description:** This API is used to update product data that has been added previously, to update product data it requires the Company's product ID parameter of the product to be updated.


### HTTP Request 
`***PUT*** /companyProduct/update/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANYPRODUCT/DELETE/ME
## ***DELETE*** 

**Summary:** Delete data company product

**Description:** This API is used to delete product data available at user's company. To delete product data a company product ID is required to be deleted.


### HTTP Request 
`***DELETE*** /companyProduct/delete/me` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| token | query |  | Yes |  |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /KBLI/LIST
## ***GET*** 

**Summary:** Get data kbli

**Description:** This API is used to display KBLI data Lists. KBLI is a clasification used for the clasification of Indonesian economic activities  into several different business fields based on the type of economic activity that produces products in the form of goods or services.


### HTTP Request 
`***GET*** /kbli/list` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderBy | query |  | Yes |  |
| sortBy | query |  | Yes |  |
| page | query |  | Yes |  |
| size | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not Found |

# /COMPANYTYPE/LIST
## ***GET*** 

**Summary:** Get data company type

**Description:** This API is used to display types of companies that can be added by users. company type is used to add business profile data owned by users.


### HTTP Request 
`***GET*** /companyType/list` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderBy | query |  | Yes |  |
| sortBy | query |  | Yes |  |
| page | query |  | Yes |  |
| size | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Ok |
| 403 | Forbidden |
| 404 | Not found |

# /ORGANIZATION/PUSAT/LIST
## ***GET*** 

**Summary:** Get organization pusat list

**Description:** This API is used to display list of central organization data.


### HTTP Request 
`***GET*** /organization/pusat/list` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderBy | query |  | Yes |  |
| sortBy | query |  | Yes |  |
| page | query |  | Yes |  |
| size | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |

# /ORGANIZATIONTYPETREE
## ***GET*** 

**Summary:** Get organization type tree

**Description:** This API is used to display organization menu on the directory page and will show the type of organization that is in NU.


### HTTP Request 
`***GET*** /organizationTypeTree` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| code | query |  | Yes |  |
| level | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |

# /ORGANIZATIONTREE
## ***GET*** 

**Summary:** Get organization tree

**Description:** This API is used to show a list of organizations from the provincial, district, sub district,village, group level.


### HTTP Request 
`***GET*** /organizationTree` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| criteria | query |  | Yes |  |
| type | query |  | Yes |  |
| orderBy | query |  | Yes |  |
| sortBy | query |  | Yes |  |
| page | query |  | Yes |  |
| size | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |

# /ORGANIZATIONMANAGEMENT/LIST
## ***GET*** 

**Summary:** Get organization management list

**Description:** This API is used to show list of NU's organizational management structures.


### HTTP Request 
`***GET*** /organizationManagement/list` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| organizationId | query |  | Yes |  |
| orderBy | query |  | Yes |  |
| sortBy | query |  | Yes |  |
| page | query |  | Yes |  |
| size | query |  | Yes |  |
| type | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |

# /ORGANIZATIONADDRESSCONTACT
## ***GET*** 

**Summary:** Get organization address contact

**Description:** This API is used to display NU Organization contacts and addresses.


### HTTP Request 
`***GET*** /organizationAddressContact` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |

# /ORGANIZATIONSEARCH
## ***GET*** 

**Summary:** Get organization search

**Description:** This API is used to search for organizational data or members of an organization based on name or position.


### HTTP Request 
`***GET*** /organizationSearch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| name | query |  | Yes |  |
| orderBy | query |  | Yes |  |
| sortBy | query |  | Yes |  |
| page | query |  | Yes |  |
| size | query |  | Yes |  |
| type | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |

# /NEWS/LIST
## ***GET*** 

**Summary:** Get news list

**Description:** This API used to showing the news in GreenPages apllication.


### HTTP Request 
`***GET*** /news/list` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderBy | query |  | Yes |  |
| sortBy | query |  | Yes |  |
| page | query |  | Yes |  |
| size | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 403 | Forbidden |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
