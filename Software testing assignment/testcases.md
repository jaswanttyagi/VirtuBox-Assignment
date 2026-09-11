# Registration Scenario

# format

TestCase Number                 ||  Test scenario               ||            Test Case




TC01 -:                         ||    All Data required         ||        All important field should mark with (*) ex -: firstName , lastName , Email-id , Phone Number , password , new Password and these all data required for successfull registration



TC02 -:                         ||  Register with an already registered email   ||  registration is rejected with meaningfull error (ex -: account already exist)


TCO3 -:                         ||    Valid Registration        ||  register first name should not start with upper case letter (invalid first name)




TCO4 -:                         ||    Name Validation           || verify that name fields reject invalid characters formats and accept valid name according to the application rule




TC05 - :                        || valid Email format           ||  verify that invalid email format are rejected and valids email formats are accepted



TC06 _:                         || password criteria           || password should contain uppercase letter, lowercase letter , digit , speacialSymbol and length  > 8  &&  the password should not include the username or firstName (security) 



TC07 -:                         || password Confirmation      || confirm password and password both field should match and non empty




TC08 -:                         || Boundary long input        || Entering very long field values in registration fields are handled properly .



TC09 -:                         || refreshing on submit page  || submission registration multiple times or refresh during submission and verify that duplicate accounts are not created.

TC10 -:                         || Registration -> login       || verify that registerd user can log in succesfully 





# Login Scenario

# format

TestCase Number                 ||  Test scenario               ||            Test Case



TC01 -:                        ||     Valid login               || Registered user should be able to login successfully using valid email / usernmae and correct password 


TC02 -:                        ||    Valid password             ||  Login should be rejected if registered username is used and password is incorrect with a eeror message.


TC03 -:                        ||   unregistered user           ||  Login should be rejected when an unregistered email username is entered.


TC04 -:                        ||   session and Protected access ||     after successfull login the user should be able to access task features after logout protected data should not be accessible without login again


TC05 -:                        ||    Backend Validation and error handling   ||     verify that invalid login requests are rejected by the backend even if frontend validation is bypassed and server network should handled properly.


TC06 -:                        || multiple login attempts         ||    Try multiple incorrect passwords and verify that the application handles repeted failed attempts efficently without exopsing sensituve information







# CRUD OPERATIONS -: These opeartion are possible only when user is logged In

# format

TestCase Number                 ||  Test scenario               ||            Test Case



# CREATE

TC01 -:                         ||      Create Task             ||  Logged in user should be able to create a task with valid details and the task should appear in the task list



TC02 -:                         ||   Create task with empty data  ||  Application/website should not create the task when required task info is missing and should show a valid eror msg



TC03 -:                         ||  Create task with boundary Data ||  Enter minimum , maximum limit for input limit when user cerating a task



#  READ / VIEW / GET


TC04 -:                         ||          View Task             ||   only Logged in user can see their all task completed / uncompleted



TC05 -:                         ||         DATA PRESISTENCE       || if user create a task and task is stored in databse then it should shown in the task list.       



TC06 -:                         ||   DATA CONSISTENT              ||  if user refresh the page task should load correctly and if open the task in another Tab it should load correctly





# UPDATE / EDIT / PUT



TC07 -:                         ||         EDIT TASK            ||  Only Logged In user can edit a existing task and the update data should reflect in the list and should correctly updated in database also.      



TC08 -:                         ||           EMpty Updated Data   ||  The Update should contain the body empty space not allowed should reflect a valid error msg (No data / body provided)     



TC09 -:                         ||   Network disconnects while saving     ||     Proper error + user can retry   



TC010 -:                         ||  Refresh while editing               ||      Correct behavior ,  unsaved changes should not silently corrupt data





# DELETE


TC11 -:                         ||    Delete existing task              ||    Task deleted successfully and also remove from the task list and database also.      



TC12 -:                         ||    Click Delete → Cancel             ||      Click Delete → Cancel



TC13 -:                         ||    Network fails during deletion     ||     Error shown, task state handled correctly 



TC14 -:                         ||   Delete while task list is loading   ||     Button/state handled correctly



TC15 -:                         ||  Refresh immediately after delete     ||    Task should remain deleted






# INPUT VALIDATION AND ERROR HANDLING


# format

TestCase Number                 ||  Test scenario               ||            Test Case



TC01 -:                         || ALL FIELDS REQUIRED          ||      Submit a from Without filling mandatory field should reflect error with proper message.



TC02 -:                         ||    invalid input format      ||      Enter valid data such as an incorrect email format and verify that application reject with a clear message.




TC03 -:                         ||     Boundary Values           ||     Enter Values only in allowed limits and verify that the application handles correctly



TC04 -:                         ||  Invalid Opeartion            ||    if user Try to perform invalid operation then Application / website should not allow and show the clear error msg.


TC05 -:                         || Frontend - Backend Validation ||    verify that invalid data is rejected by the backend even when frontend- validation is bypassed.



TC06 -:                         ||  API/SERVER ERROR HANDLING   || when the server or API is unavialble then ensure application should show menaning full msg.



TC07 -:                         ||   Data consistency after failure  || if an opeartion fails midway , verify that application does not show successfull state. when the data actually not saved / updated / Deleted