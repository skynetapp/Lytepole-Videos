#### Step 1:

Function **controlVideoListFlow** will be called first from index.php to controller which takes the inputs from the user. we call the wsdl to get the video list and displays.

- Function **createVideoListInputVO** takes the inputs array and send to data file and prepares the list object.
- In action, function **createVideoListInputVO** will be called from VideoData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create video
