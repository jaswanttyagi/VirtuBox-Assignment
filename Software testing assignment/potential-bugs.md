# Potential Bugs

#    format

BUG NO         ||         Potential Bug            ||  

Situation      ||                  Imapct




BUG01 -:       ||   user may be able to access another user task by changing task related request 

||  critical  || this can expose private user data and may allow unauthorized user to another user tasks.





BUG02 _:       ||   user may be able to access task features even after logout the or without a valid login session 

|| critical    ||   Unauthorized users could access or modify the protected task data





BUG03 -:       ||   passowrd or other sensitive information (like login info  , registration info ) may be exposed in response or logs      ||      critical    || sensitive info could be exposed and create a security risk.





BUG04 -:        ||  A task may be appear successfully created / updated on UI even request failed in DATABASE 
|| MAJOR    || UI And Actual data become inconsisten.





BUG05 -:        || Deleted task may appear again after refreshing the page || MAJOR || Indicates deletion may not correctly saved in the database.



BUG06 -:       ||   Duplicate task records may be created when the user submits the same request multiplte time quickly   || MAJOR ||  can create the duplicate data which affect data reliablity.



BUG07 -:       ||   Application may crash or show a technical error when the server / database is Unavilable 
|| MAJOR       ||   User Experince affected.



BUG08 -:        ||  Error message may be unclear or may incorrectly reflect success / failure 
||    Minor     || users may not understand wwhat went wrong .


BUG09 - :       || Task list may show outdated if  multiple action perform quickly across diffrent session 
|| MAJOR        || user may see an incorrect task state , which can lead to confusion and data inconsistency.