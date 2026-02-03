*Upcomming Task Deadlines*
**Presentation 2/3/2026 on OEBD,OCD, OABD/OAB, and SA() documents**



Current List of things to Revise/Do

[OEBD]
* [ ] Think of development.  There are development stations throughout the lab that will be used to test and develop the systems. They should be included.  If this is the processing unit, I would change the name to make it clearer. See similar [OCB] comment as well.
* [x] If you are going to do several SW releases, some "SW factory entity
* [x] There should also be a debug entity, either a maintainer actor (even if that is you) and an associated "provide system status" OC.
* [Not Needed] I would put the sonar and camera directly into the domain block.  When you do the [OAB] it will make the job easier and provide insight to what crosses between the sensors and the RP system.
* [x] There are many image transfers standards.  They should be an entity
  
[OCB]
* [Apart of our C2C 1.0] There is typically an Initiate/configure OC
* [x] There is typically an Provide System Status OC 
* [x] 2.0 and 3.0 Should be a generic Sense Objects - Sonar.  The Tx and Rx will come out in the activities and lower function
* [x] 6.0 Aggregate Sensor Data should go to the RP$ unless you are offloading data to be processed on an outside "Processing Unit."
* [x] Update display should go to the RP4.  Its graphics card is rendering the images which are displayed on the development environment monitors  This could likely be deleted and will be decomposed from the  Provide System Status I recommended.
* [x] If you are storing data then it is likely an OC.  Task camera should not need Data Storage
* [Not Needed] Same comment about putting the camera and sonar on the same level as the RP4.
  
[OABD]
* [ ] Most sensors need to be initiated /configured prior to tasking.  I would add the configure activities
* [ ] 2.2 the audible environment is a system entity and should not be an activity.  If the sensor needs any calibration, that should be an activity.  If the sonar pulse chain needs to gerated before it is sent, that should be another activity.
* [ ] 5.0 There is significant correction in image processing to include: Image filters, Dewarping (corrects for rounded lens), Contrast/Distortion control, Compression, Overlay addition, EO/IR fusion, Object detection, Chipping, etc.  You can keep this at a high level and make it an "Image Correction" Activity.
* [ ] If you add the Status System OC, there should be some get, send & process BIT Status Activities
