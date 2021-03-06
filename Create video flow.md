#### Date: 15/03/2017

#### Description: This document explains the code flow of creating video.

#### Step 1:

Function **createVideoFlow** will be called first from index.php to controller which is used to create video, and uploads to sugar folder using curl.

- Function **createVideoListInputVO** takes the inputs array and send to data file and prepares the list object.
- In action, function **createVideoListInputVO** will be called from VideoData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create video.
- Input parameters will be meeting id,meeting name and Action name.
- Result returns the video list value object array to controller.

#### Step 2:

- Function **createVideo** takes the input value object and passes to the wsdl call to create a video.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **createVideo** will be called from VideoWS.php which is used to create a new video using wsdl calls **set_entry**. 
- Create the parameters for wsdl using object and passing parameter array to ws call.
- Result returns the video id to controller.

#### Step 3:

- Function **createMeetingVideoRelation** takes the input value object and set relation between video and meeting.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **createMeetingVideoRelation** in VideoWS.php which is used to create a relation between meeting and video using wsdl calls **set_relationship**.
- Creating parameters for wsdl using object and passing the parameter array to ws call.
- Result returns the relation id.
- Video will be saved using curl call.

