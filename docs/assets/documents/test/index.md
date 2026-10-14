<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [EHMI Testspecifications](#ehmi-testspecifications)
- [End User Application (EUA)](#end-user-application-eua)
   * [Sending EUA (corner 1)](#sending-eua-corner-1)
      + [Request data from EAS ](#request-data-from-eas)
      + [Registrations sent to EDS ](#registrations-sent-to-eds)
   * [Receiving EUA (corner 4)](#receiving-eua-corner-4)
      + [Registrations sent to EDS](#registrations-sent-to-eds-1)
- [Message Service Handler (MSH)](#message-service-handler-msh)
   * [Sending MSH (corner 1)](#sending-msh-corner-1)
      + [Registrations sent to EDS](#registrations-sent-to-eds-2)
      + [ehmiSBDH and ehmiSBDHAcknowledgement](#ehmisbdh-and-ehmisbdhacknowledgement)
   * [Receiving MSH (corner 4)](#receiving-msh-corner-4)
      + [Registrations sent to EDS](#registrations-sent-to-eds-3)
      + [ehmiSBDH and ehmiSBDHAcknowledgement](#ehmisbdh-and-ehmisbdhacknowledgement-1)
   * [Receiving EMR MSH (corner 4)](#receiving-emr-msh-corner-4)
      + [Registrations sent to EDS](#registrations-sent-to-eds-4)
      + [ehmiSBDH and ehmiSBDHAcknowledgement](#ehmisbdh-and-ehmisbdhacknowledgement-2)
- [Access Poin (AP)](#access-poin-ap)
   * [Sending AP (corner 2)](#sending-ap-corner-2)
      + [Registrations sent to EDS](#registrations-sent-to-eds-5)
   * [Receiving AP (corner 3)](#receiving-ap-corner-3)
      + [Registrations sent to EDS](#registrations-sent-to-eds-6)
   * [Receiving EMR AP (corner 3)](#receiving-emr-ap-corner-3)
      + [Registrations sent to EDS](#registrations-sent-to-eds-7)
- [Other service ](#other-service)
   * [EAS](#eas)
   * [EDS component](#eds-component)

<!-- TOC end -->

<a name="ehmi-testspecifications"></a>

## EHMI Testspecifications

Testing is performed in the ITB testtool and with a testprotocol

Corners are defined from this illustration (ehmi core --> ### Layers)

<a name="end-user-application-eua"></a>

## End User Application (EUA)

As End User Application the system must be able to send and/or receive the messages and display the relevant content to the users of the application. Test of the standards containing the clinical content is not defined on this page. The EUA ensures the traceability of sent and received messages by registering their dispatch and receipt in the EDS service (EHMI Delivery Status), which serves as the track-and-trace system of the eDelivery Health Domain.

In regards to communication on the EHMI infrastructure, the relevant tests for a sending and receiving application is shown. 


<a name="sending-eua-corner-1"></a>

### Sending EUA (corner 1)

When a clinical message needs to be sent to a receiving EUA, the clinical system ensures that the message is structured according to the relevant clinical format (e.g., a HomeCareObservation) and identifies the intended recipient through EAS. The message and recipient information are then passed to MSH. 


<a name="request-data-from-eas"></a>

#### Request data from EAS 

<a name="registrations-sent-to-eds"></a>

#### Registrations sent to EDS 

Run through of **EDS Shared Tests (All Corners)** and **EDS Sending EUA Test Suite (Corner 1 EUA)** in the ITB

<a name="receiving-eua-corner-4"></a>

### Receiving EUA (corner 4)

The receiving EUA must be able to receive a clinical message from the receiving MSH and acknowledge the clinical message with a FHIR Acknowledgement. 

<a name="registrations-sent-to-eds-1"></a>

#### Registrations sent to EDS

<a name="message-service-handler-msh"></a>

Run through of **EDS Shared Tests (All Corners)** and **EDS Receiving EUA Test Suite (Corner 4 EUA)** in the ITB.


## Message Service Handler (MSH)

An MSH is responsible for wrapping messages into the ehmiSBDH and to sent and receive emhiSBDHAcknowledgement. 

MSH ensures the traceability of sent and received messages by registering their dispatch and receipt in the EDS service (EHMI Delivery Status), which serves as the track-and-trace system of the eDelivery Health Domain.

<a name="sending-msh-corner-1"></a>

### Sending MSH (corner 1)
The sending MSH is responsible for preparing and sending clinical messages from EUA to a designated recipient. Preparation involves wrapping the clinical message in the digital envelope (ehmiSBDH) used for exchanging clinical messages within the eDelivery Health Domain. MSH handles success or error acknowledgements from the recipient (ehmiSBDH Acknowledgement). Following successful delivery, a copy of the message is sent to EMR, a service for archiving clinical messages transmitted via the eDelivery Health Domain.

<a name="registrations-sent-to-eds-2"></a>

#### Registrations sent to EDS
Run through of **EDS Shared Tests (All Corners)** and **EDS Sending MSH Test Suite (Corner 1.5 MSH)** in the ITB.

<a name="ehmisbdh-and-ehmisbdhacknowledgement"></a>

#### ehmiSBDH and ehmiSBDHAcknowledgement

**Sender MSH Creation Validation Suite**

<a name="receiving-msh-corner-4"></a>

### Receiving MSH (corner 4)
As a receiving MSH you must be able to receive the clinical messages from the AP, unwrap it from the digital envelope (ehmiSBDH), return an envelope acknowledgement (ehmiSBDH Acknowledgement) to the sender, and forwards the unwrapped clinical message to EUA.

<a name="registrations-sent-to-eds-3"></a>

#### Registrations sent to EDS
Run through of **EDS Shared Tests (All Corners)** and **EDS Receiving MSH Test Suite (Corner 3.5 MSH)** in the ITB.
 
<a name="ehmisbdh-and-ehmisbdhacknowledgement-1"></a>

#### ehmiSBDH and ehmiSBDHAcknowledgement
**Receiver MSH Creation Validation Suite**


<a name="receiving-emr-msh-corner-4"></a>

### Receiving EMR MSH (corner 4)

As a receiving EMR MSH you must be able to receive the clinical messages from the AP, unwrap it from the digital envelope (ehmiSBDH) and pass it on to the Document Sharing Service (DDS), and return an envelope acknowledgement (ehmiSBDH Acknowledgement) to the sender.

<a name="registrations-sent-to-eds-4"></a>

#### Registrations sent to EDS

Run through of **EDS Shared Tests (All Corners)** and **EDS Receiving EMR MSH Test Suite (Corner 3.5 MSH)** in the ITB.

<a name="ehmisbdh-and-ehmisbdhacknowledgement-2"></a>

#### ehmiSBDH and ehmiSBDHAcknowledgement

**Receiver EMR MSH SBDH Validation Suite**


<a name="access-poin-ap"></a>

## Access Point (AP)

AP handles the actual digital exchange of clinical messages transmitted via the eDelivery Health Domain. The recipient's digital address is retrieved through the Danish Business Authority's SMP service. Messages and acknowledgements are wrapped and encrypted in accordance with the EU eDelivery protocol and then transmitted to the recipient's AP via the Danish Health Data Network (Sundhedsdatanettet).

When AP receives a message from another AP via the Danish Health Data Network, AP is responsible for decrypting and unwrapping the message before forwarding it to MSH.

AP ensures the traceability of sent and received messages by registering their dispatch and receipt in the EDS service (EHMI Delivery Status), which serves as the track-and-trace system of the eDelivery Health Domain.

<a name="sending-ap-corner-2"></a>

### Sending AP (corner 2)
<a name="registrations-sent-to-eds-5"></a>

#### Registrations sent to EDS

Run through of **EDS Shared Tests (All Corners)** and **EDS Sending AP Tests (Corner 2 AP)** in the ITB

<a name="receiving-ap-corner-3"></a>

### Receiving AP (corner 3)
<a name="registrations-sent-to-eds-6"></a>

#### Registrations sent to EDS
Run through of **EDS Shared Tests (All Corners)** and **EDS Receiving AP Tests (Corner 3 AP)** in the ITB.

<a name="receiving-emr-ap-corner-3"></a>

### Receiving EMR AP (corner 3)
No tests for this application, as it is build together with the MSH.

<a name="registrations-sent-to-eds-7"></a>

#### Registrations sent to EDS

<a name="other-service"></a>

## Other service 

<a name="eas"></a>

### EAS
The EHMI addressing service (EAS) is developed to solve the wellknown challenges for a sender to find the right recipient. The service will draw necessary information from the proper authoritative sources and present this information to the sender of the message, thereby assisting the sender in finding the proper recipient.

<a name="eds-component"></a>

### EDS component

The EHMI delivery status (EDS) component collects the delivery status of a sent message at selected points along the delivery path and subsequently exposing the delivery status via a service to both healthcare professionals and citizens, allowing them to follow the status of a message in close to real-time to the benefit of the citizens/patients’ safety.

Run through of **EHMI Delivery Status Server Component (EDS)** in ITB

