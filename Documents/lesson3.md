# Lesson 1

## XML (Luis Hainberger)
In computing, Extensible Markup Language (XML) is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable.

SOAP (originally Simple Object Access Protocol) is a protocol specification for exchanging structured information in the implementation of web services in computer networks.(uses XML)

SOAP has three major characteristics:

- extensibility (security and WS-Addressing are among the extensions under development)
- neutrality (SOAP can operate over any protocol such as HTTP, SMTP, TCP, UDP, or JMS)
- independence (SOAP allows for any programming model)
```
<?xml version="1.0"?>
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:m="http://www.example.org/stock/Manikandan">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <m:GetStockPrice>
      <m:StockName>GOOGLE</m:StockName>
    </m:GetStockPrice>
  </soap:Body>
</soap:Envelope>
```
Advantages
- SOAP's neutrality characteristic explicitly makes it suitable for use with any transport protocol. Implementations often use HTTP as a transport protocol, but other popular transport protocols can be used. For example, SOAP can also be used over SMTP, JMS and message queues.
- SOAP, when combined with HTTP post/response exchanges, tunnels easily through existing firewalls and proxies, and consequently doesn't require modifying the widespread computing and communication infrastructures that exist for processing HTTP post/response exchanges.
- SOAP has available to it all the facilities of XML, including easy internationalization and extensibility with XML Namespaces.

## Json

In computing, JavaScript Object Notation or JSON, is an open-standard file format that uses human-readable text to transmit data objects consisting of attribute–value pairs and array data types (or any other serializable value). It is a very common data format used for asynchronous browser–server communication, including as a replacement for XML in some AJAX-style systems.

Syntax:
```
{
  "firstName": "John",
  "lastName": "Smith",
  "isAlive": true,
  "age": 25,
  "address": {
    "streetAddress": "21 2nd Street",
    "city": "New York",
    "state": "NY",
    "postalCode": "10021-3100"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "212 555-1234"
    },
    {
      "type": "office",
      "number": "646 555-4567"
    },
    {
      "type": "mobile",
      "number": "123 456-7890"
    }
  ],
  "children": [],
  "spouse": null
}
```
JSON Schema specifies a JSON-based format to define the structure of JSON data for validation, documentation, and interaction control. It provides a contract for the JSON data required by a given application, and how that data can be modified.

## AllSeen

AllSeen is based on AllJoy


The AllSeen Alliance is a non-profit organization dedicated to making it easy for devices, appliances and apps to connect to the Internet of Things.

Enable industry standard interoperability between products and brands with an open source framework that drives intelligent experiences for the Internet of Things.

The initiative includes more than 200 member companies including leading consumer electronics manufacturers, home appliance makers, automotive companies, cloud providers, enterprise technology companies, innovative startups, chipset manufacturers, service providers, retailers and software developers.

Premier Members: Canon, Microsoft,LG,Qualcom,....



## MQTT
MQTT(MQ Telemetry Transport or Message Queue Telemetry Transport) is an ISO standard (ISO/IEC PRF 20922) publish-subscribe-based "lightweight" messaging protocol for use on top of the TCP/IP protocol. It is designed for connections with remote locations where a "small code footprint" is required or the network bandwidth is limited. 

The publish-subscribe messaging pattern requires a message broker. The broker is responsible for distributing messages to interested clients based on the topic of a message.

Users:

- Facebook Messenger. Facebook has used aspects of MQTT in Facebook Messenger for online chat. However, it is unclear how much of MQTT is used or for what.
- IECC Scalable, DeltaRail's latest version of their IECC Signaling Control System uses MQTT for communications within the various parts of the system and other components of the signaling system. It provides the underlying communications framework for a system that is compliant with the CENELEC standards for safety-critical communications.
- The EVRYTHNG IoT platform uses MQTT as an M2M protocol for millions of connected products.
- Amazon Web Services announced Amazon IoT based on MQTT in 2015.

## Methods: 
### Connect
Waits for a connection to be established with the server.
### Disconnect
Waits for the MQTT client to finish any work it must do, and for the TCP/IP session to disconnect.
### Subscribe
Waits for completion of the Subscribe or UnSubscribe method.
### UnSubscribe
Requests the server unsubscribe the client from one or more topics.
### Publish
Returns immediately to the application thread after passing the request to the MQTT client.

