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
   * [EER](#eer)

<!-- TOC end -->

<a name="ehmi-testspecifications"></a>

## EHMI Testspecifications

Testing is performed in the ITB testtool and with a testprotocol

Corners are defined from this illustration (ehmi core --> ### Layers)

<a name="end-user-application-eua"></a>

## End User Application (EUA)

As End User Application the system must be able to send and/or receive the messages and display the relevant content to the users of the application. Test of the standards containing the clinical content is not defined on this page, but can be found.... 

In regards to communication on the EHMI infrastructure, the relevant tests for a sending and receiving application is shown. 



<a name="sending-eua-corner-1"></a>

### Sending EUA (corner 1)

<a name="request-data-from-eas"></a>

#### Request data from EAS 

<a name="registrations-sent-to-eds"></a>

#### Registrations sent to EDS 

<a name="receiving-eua-corner-4"></a>

### Receiving EUA (corner 4)

<a name="registrations-sent-to-eds-1"></a>

#### Registrations sent to EDS

<a name="message-service-handler-msh"></a>

## Message Service Handler (MSH)

<a name="sending-msh-corner-1"></a>

### Sending MSH (corner 1)

<a name="registrations-sent-to-eds-2"></a>

#### Registrations sent to EDS
All applications must comply to the test suite "EHMI Shared ...

<a name="ehmisbdh-and-ehmisbdhacknowledgement"></a>

#### ehmiSBDH and ehmiSBDHAcknowledgement

<a name="receiving-msh-corner-4"></a>

### Receiving MSH (corner 4)

<a name="registrations-sent-to-eds-3"></a>

#### Registrations sent to EDS

<a name="ehmisbdh-and-ehmisbdhacknowledgement-1"></a>

#### ehmiSBDH and ehmiSBDHAcknowledgement


<a name="receiving-emr-msh-corner-4"></a>

### Receiving EMR MSH (corner 4)

<a name="registrations-sent-to-eds-4"></a>

#### Registrations sent to EDS

<a name="ehmisbdh-and-ehmisbdhacknowledgement-2"></a>

#### ehmiSBDH and ehmiSBDHAcknowledgement


<a name="access-poin-ap"></a>

## Access Poin (AP)

<a name="sending-ap-corner-2"></a>

### Sending AP (corner 2)
<a name="registrations-sent-to-eds-5"></a>

#### Registrations sent to EDS

<a name="receiving-ap-corner-3"></a>

### Receiving AP (corner 3)
<a name="registrations-sent-to-eds-6"></a>

#### Registrations sent to EDS

<a name="receiving-emr-ap-corner-3"></a>

### Receiving EMR AP (corner 3)
<a name="registrations-sent-to-eds-7"></a>

#### Registrations sent to EDS

<a name="other-service"></a>

## Other service 

<a name="eas"></a>

### EAS

<a name="eds-component"></a>

### EDS component

<a name="eer"></a>

### EER

