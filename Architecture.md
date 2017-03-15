#### Date: 15/03/2017

#### Description: This document explains the code flow of Videos.

#### The Folder Structure is as follows:

 Root Directory | Sub Directory 
------------ | -------------
index.php | 
Global | LytepoleWSConnection
Lib | Smarty,nusoap
Modules | Videos
Views | VideoListForm, emptyVideoListForm


#### Architecture

- After login into lytepole, if we want to upload videos we can go into messages and there we can upload the video for a member in chat.
- The upload video size should be less than 2MB.
- If the video is empty, form will be redirected to empty video list.
- Function **controlVideoListFlow** will call the wsdl to get the video list and displays the output.
- Function **createVideoFlow** will create a video and uploads the sugar folder using curl call.

