# Bump, why so difficult?<br>2011-12-21<br>mobile<br>
---
I recently reviewed a content sharing Android app from [Bump Technologies](http://bu.mp/jobs).  Bump allows you to share content easily with another Bump user.  
  
It was easy to install.  Then the real fun began.  You have to configure the app, start it, then from the app specify what you want to share.  Here is the part that is supposed to be easy.  To select the recipient of your content you simply do a fist bump with the recipient while you both are holding your phones.  The accelerometer in the phones registers the event and starts the share.  
  
Hmmmm.  After the bump I needed to choose from my contacts who I'm sharing with (or set up a new contact).  Why?  
  
So a jillion questions come to mind; and they all have to do with the complexity of the design:  
  


  1. Why do I need to select the recipient?  How many Bump enabled devices had their accelerometers activated within bluetooth range in the last fraction of a second?  The answer is one.
  2. Why do I need to select the content to share from within the Bump app?  Android supports Intents.  One of those is the intent to share.  You've seen this every time you share a photo to Facebook or email.  You are viewing the photo and you select share from the system menu.  Bump could have easily added another Intent to share.
  3. Why do I need to select the content type?  OK, so this is related to the last item but really, if I'm in the photo viewer and want to share, the app can figure out what type of content I'm sharing.
  4. Why would the connection fail?  That's because you need to connect through the Bump servers which may be unavailable (e.g. down or overloaded).  So whats all this talk about Bluetooth?  Right, well what's the need for a network connection to the Bump website?  I did a switch-eroo from network to Bluetooth because what do we care?  Let the app decide the connectivity, just make it work.

There are architectural considerations also.  The sender doesn't need to be sucking down Bluetooth or GPS juice until the user selects the Bump Intent (before the bump event even happens). The recipient is the same, the Bump event itself can trigger the Bluetooth or GPS services.  
  
Why does a website need to be the middleman?  Bluetooth is a fine transport.  
  
The best UX in this instance is the UI that doesn't exist.  Bump doesn't need an explicit UI but could integrate with Android as an enhancement and provide all the functionality with no user overhead.
