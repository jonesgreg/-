---
layout:     post
title:      Hawk Ride - Ride sharing escort services for college students (iOS Mobile App)
date:       2019-01-28 14:31:19
summary:    Computer Science Project (CSC495)
categories: swift
---
### Abstract
Hawk Ride is a convenient student ride-sharing service that allows college students to request a ride, and a student driver provides transportation to the student throughout the campus.
<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/hawkride.png" height="400">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/homescreen.png" height="400">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/rider.png" height="400">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/driver.png" height="400">
</p>
&nbsp;<center><strong>Problem</strong></center>
Most Colleges and Universities are using **aging and inefficient technology**. For instance, a radio dispatch. When I was a college student, I would call Public Safety our campus security for an escort to my dorm. My issue with using Public Safety is the **long wait period**. I had no clue how long it would take them to get to my location. There was no way for me to track the driver to see if he or she was close. **Uber and Lyft** became a hit in the transportation industry due to using sufficient technology that prevents these obstacles. Not to mention, most students at my school stop depending on Public Safety.

&nbsp;<center><strong>Solution</strong></center>
Hawk Ride provides a **quick and efficient** student escort service program, **automate dispatch to reduce wait-time**, and it is a **free service** that would be used to keep our students safe on and off campus.

&nbsp;<center><strong>How it all works?</strong></center>
<p align= "center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/works.png" height="300" width="800">
</p>
&nbsp;<center><strong>Safety & Training</strong></center>
<center> - Drivers will be conducting a <strong>DMV and Background checks</strong>.</center>
<center> - Drivers will use a  <strong>University vehicle</strong>, so they must go through a <strong>certification training process</strong>.</center>
<center> - Drivers must complete the <strong>Authorized Driver Application Form</strong>.</center>

&nbsp;<center><strong>How to pay for a ride?</strong></center>
<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/ride.png" height="400" width="900">
</p>

&nbsp;<center><strong>Restricted Locations & Ride History</strong></center>

Students have a list of pick up and drop off locations. My intent with the ride-sharing app is to provide a **safe and reliable service** that is useful for students to use as escort to their dorm halls and campus sites. This platform is not an **Uber or Lyft service**, so students **cannot be pick up or drop off at any location**.Not to mention, students rides are **tracked** and can be **viewed**.&nbsp;
<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/riderequest1.png" height="500">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/riderequest2.png" height="500">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/ridehistory.png" height="500">
</p>
### Development Stages

&nbsp;<center><strong>Technologies Used & Cocoapods</strong></center>
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/tech.png" height="400" width="800">

&nbsp;<center><strong>Registering and Log in Feature</strong></center>
Hawk Ride allows students to register with their **first name**, **lastname**, and a **University Email**. This information is stored in **Google Firebase** real-time database.
<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/usersData.png" height="200" width="700" />
</p>

&nbsp;<center><strong>Pick up & Drop Off Locations</strong></center>
Like I mentioned before, students are **limited** to where they can be picked up and dropped off. I decided to develop a **tableview** that displays the list of locations that students can choose from. I stored each location including the **longitude** and **latitude** of the location inside of an **array list**.
<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/locations.png" height="400" width="700" />
</p>

<center>I developed a tableview which displays the list of locations.</center>
<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/tableview.png" height="400" width="700" />
</p>
&nbsp;<center><strong>Booking Feature</strong></center>
This allows drivers the option to **accept** or **deny** incoming ride requests and get information on the **current location and destination** of the student passenger. When the passenger clicks the **request ride button it sends a notification to the driver**, and the driver has a chose to accept or deny the request. If the driver accepts the request, then the passenger **pick up location will display on the drivers screen**.
<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/acceptRide.png" height="200" width="700" />
</p>

This is a code snippet of the function that I created. When the drivers accept the ride, it will pass the **passengerID** which has the **current location** and gives it to the driver, so the drivers know the **passenger's pickup**. Down below is a screenshot of how the notification pop up looks on the driver's screen.
<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/acceptTrip.png" height="700" width="300" />
</p>

&nbsp;<center><strong>Point to Point Directions</strong></center>
Hawk Ride app provides directions to both the driver and the passenger. I used **MapKit** for iOS(Moving to Google Maps) to calculate the route and make directions available.

The green map annotation is the passenger's current location where they want to be picked up form.

<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/directionspath.png" height="700" width="300" />
</p>

Once the driver accepts the trip, the map will **draw a route** from the driver's current location to the passenger current location.


When the driver clicks get directions, the app will use **Apple maps** to get directions.
<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/applemaps.png" height="700" width="300" />
</p>


&nbsp;<center><strong>The ability to Identify a Device's Location</strong></center>
Hawk Ride, via **CoreLocation Framework**(for iOS platforms) obtains the **geographic location and orientation** of a device to schedule location and delivery.

&nbsp;<center><strong>What Technology is Hawk Ride Built on?</strong></center>
The tech side of the app is mainly written in **Swift** for the iOS platform. I programmed everything in Swift. The UI design was programmed in Swift. Also, the real-time dispatch system being built in Swift. Not to mention, I used **Google Firebase API** for the real time database the stored users location and profile information. **Twilio** is the force behind Hawk Ride's text messages, and push notifications are implemented through **Apply Push notifications Service** on the iOS platform.

&nbsp;<center><strong>Next Steps</strong></center>
<center> - Re-developed database.</center>
<center> - Support all iPhone device screen resolution.</center>
<center> - Migrate to Google Maps.</center>
<center> - Single sign on Authentication feature.</center>
<center> - Develop an android version.</center>

&nbsp;<center><strong>Live Demo</strong></center>

<iframe src="https://player.vimeo.com/video/339689006" width="900" height="400" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>


<p align="center">
  <img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/ridefastandridefree.png" height="400" />
</p>
