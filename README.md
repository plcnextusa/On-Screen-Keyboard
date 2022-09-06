A new version is avaliable on the PLCnext Store.

# On-Screen-Keyboard

SETUP
1. Download the library.
2. Add the library to your project.
3. Under the "COMPONENTS - HMI" expand the "Keyboard" folder and then the "Page Templates" folder.
4. Right click on the "Keyboard" template and select "Create HMI Page".
5. Right click on the "Keypad" template and select "Create HMI Page".
6. Locate the "KeyboardsHandler" Function Block under the "COMPONENTS - Programming" section.
7. Add an instance of the "KeyboardsHandler" Function Block to a Program.  This Program should be scheduled in a Task with an Interval that is twice as fast as the eHMI Data        poll interval.
8. Assign an External variable to the Function Block.


NUMERIC KEYPAD USE
1. Use a "Text" object, not a "Text Input" object, in your HMI where a numeric value entry field is needed.
2. Set the "Stroke - Line width" to 1 to give this object an Input Box appearance.
3. Add a "Text" dynamic to this "Text" object.
    a. Select the desired "Variable" as appropriate.
    b. Set the "Format" as appropriate.
    c. Make sure the "Enabled" checkbox is checked.
4. Add an "Action on Click" dynamic to this "Text" object. 
    a. Set the "Action" to "Open dialog".    
    b. For "Page" select "Keypad".    
    c. Optionally, check the box to "Dim background".
    d. For the "KB" parameter, select the variable you assigned to the "KeyboardsHandler" Function Block.
    e. For the "Decimal" parameter, change the "Source Type" to "Constant" and set it to "True" to allow the operator to enter a decimal number or "False" if only a whole number should be entered.
    f. For the "Signed" parameter, change the "Source Type" to "Constant" and set it to "True" to allow the operator to enter a negative number or "False" if only a positive number should be entered.
    g. For the "Output" parameter, select the same variable you assigned to the "Text" dynamic.    
5. Repeat to add as many input fields as needed for your application.


KEYBOARD USE
1. Use a "Text" object, not a "Text Input" object, in your HMI where a string entry field is needed.
2. Set the "Stroke - Line width" to 1 to give this object an Input Box appearance.
3. Add a "Text" dynamic to this "Text" object.
    a. Select the desired "Variable" as appropriate.
    b. Make sure the "Enabled" checkbox is checked.
4. Add an "Action on Click" dynamic to this "Text" object. 
    a. Set the "Action" to "Open dialog".    
    b. For "Page" select "Keyboard".    
    c. Optionally, check the box to "Dim background".    
    d. For the "KB" parameter, select the variable you assigned to the "KeyboardsHandler" Function Block.
    e. For the "Output" parameter, select the same variable you assigned to the "Text" dynamic.    
5. Repeat to add as many input fields as needed for your application.

