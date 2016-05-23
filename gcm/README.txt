Google Cloud Messaging
=================================

This App registers for GCM and handles the receipt of a GCM message. 

Things to Note 
--------------- 
Server API Key:
AIzaSyBZniLxyr5LdzMY2_CyN7tSAOZ0c5burFc

Sender ID: 
669366832903

Send GCM messages to this URL: 
https://gcm-http.googleapis.com/gcm/send


Actuall HTTP requests
----------------------

//To send notification to ALL DEVICES 

Content-Type:application/json
Authorization:key=AIzaSyBZniLxyr5LdzMY2_CyN7tSAOZ0c5burFc

{
  "to": "/topics/global",
  "data": {"message": "This is a GCM Topic Message!"}
}


// To send to a SINGLE DEVICE 
// My Phone Token : d2dfXkwgqjs:APA91bEoDudd-yqK1lqiq5-Kb6cVUK1CR-_4VgA4Zu8Dz-HgdRzR3vaKTN_cwL41rUaSn5WVitgss8CLDnQSzs4fZUCgeAkpTAtLXkvbhWefn-n4Fsb-wPLt3XrEE_OvgDjGectfKgj-

Content-Type:application/json
Authorization:key=AIzaSyBZniLxyr5LdzMY2_CyN7tSAOZ0c5burFc

{       
  "registration_ids":["d2dfXkwgqjs:APA91bEoDudd-yqK1lqiq5-Kb6cVUK1CR-_4VgA4Zu8Dz-HgdRzR3vaKTN_cwL41rUaSn5WVitgss8CLDnQSzs4fZUCgeAkpTAtLXkvbhWefn-n4Fsb-wPLt3XrEE_OvgDjGectfKgj-"],
  "data": {
    "message" : "This is a GCM Message to a single device"
  } 
}

