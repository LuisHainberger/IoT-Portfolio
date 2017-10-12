# Lesson 4
## scaling issues:
- data storage
- consitency
- data failure
- Cost, Maintenance, Reliability
- The more devices, the more interconnectivity, increasing cost, maintenance and reliability.
- Predictive maintenance
- Windmills start vibrating, integrating a vibration sensor can predict, before one is actually failing depending on the vibrations its emitting.
09:14
- Too small subnets in combination with a Client-Server pattern might lead to too few IP addresses in an old IPv4 Network to supply every member in a network with an IP address
- Continuous integration would be "nice".

## testing:
- add devices until failure happens
- analysing stories
- multiple simulators for data stress testing
- latency testing (publisher, subscriber) with timestamping
- unit testing
- device stress testing (lifespan test)
- corner case testing (defined by stories)


## what role will play:
 ### Simulator: 
 - test large Systems 
 - test new function
 - Can be used for used for testing the systems by using defined values
- Scaling
- Error handling (e.g. String to topic which is usually used for Integers etc)
- Mock test cases which are hard to achieve in a real environment (degree: 700°)
- No hardware needed to test
 ### MQTT: 
 - Textcommunication with security
 - limit number of devices
 - Helps subscribesbs to easily only receive the topics they are interested to
 -(Only one bus => one central point if we only have one broker)
 - Takes control of the publish/subscribe pattern
 - Single point of failue when not implementing more brokers
 - Pretty mature and tested a lot
 ### Stories: 
 - show cases
 - proof of concept
 - With stories we can describe the problem easily
 - Non-technical level of abstraction
- Help to communicate between stakeholder
- Defines the necessary devices and components
- Used for finding corner - cases / tests
 
 
 # IoTivity
 The IoTivity is an open source project. The IoTivity project is hosted by the Linux Foundation.
 ## Doku
 - has good documentation at iotivity wiki and tons of tutorials 
 - open source
 ## Security
 - secure resource manager which filters ressource requests and manages security relatet materiels
 ## Functionality
 - Core functionality written in C for deployment to constrained devices. Most functionality available from C and C++.
Other bindings available:
	Java (Android)
	JavaScript (in progress)
- Android support

 