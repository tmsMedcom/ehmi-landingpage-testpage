<style>
/* Gælder kun i HTML-browser – GitHub ignorerer dette blok */
details {
  margin: 1.2em 0;
  padding: 0.5em 0.75em;
  border-left: 3px solid #d0d7de;
  border-radius: 0 4px 4px 0;
}
details[open] {
  border-left-color: #0969da;
  background: #f8faff;
}
details > summary {
  cursor: pointer;
  padding: 0.3em 0;
  line-height: 1.5;
  list-style: disclosure-closed;
}
details[open] > summary {
  list-style: disclosure-open;
  margin-bottom: 0.6em;
}
details > summary:hover {
  color: #0969da;
}
details p, details li {
  line-height: 1.65;
  margin: 0.7em 0;
}
details details {
  margin-top: 0.8em;
  border-left: 2px solid #c0cad4;
  background: transparent;
}
h1, h2 {
  margin-top: 1.8em;
}
table {
  border-collapse: collapse;
  width: 100%;
  margin: 1em 0;
}
th, td {
  border: 1px solid #d0d7de;
  padding: 0.5em 0.75em;
  vertical-align: top;
}
th {
  background: #f0f4f8;
}
</style>


<h1>EHMI Testspecifications</h1>

<p>Testing is performed in the ITB testtool and with a testprotocol</p>

<p>Corners are defined from this illustration (ehmi core --> ### Layers)</p>

<details> 
<summary>End User Application (EUA)</summary>

<p>As End User Application the system must be able to send and/or receive the messages and display the relevant content to the users of the application. Test of the standards containing the clinical content is not defined on this page, but can be found.... </p>

<p>In regards to communication on the EHMI infrastructure, the relevant tests for a sending and receiving application is shown. </p>


<details> 
<summary>Sending EUA (corner 1)</summary>


<p>Request data from EAS <br> </p>

<p>Registrations sent to EDS <br> </p>

</details>

<details> 
<summary>Receiving EUA (corner 4)</summary>


<p>Registrations sent to EDS</p>

</details>

## MSH 

### Sending MSH (corner 1)

#### Registrations sent to EDS
All applications must comply to the test suite "EHMI Shared ...

#### ehmiSBDH and ehmiSBDHAcknowledgement

### Receiving MSH (corner 4)

#### Registrations sent to EDS

#### ehmiSBDH and ehmiSBDHAcknowledgement


### Receiving EMR MSH (corner 4)

#### Registrations sent to EDS

#### ehmiSBDH and ehmiSBDHAcknowledgement


## AP

### Sending AP (corner 2)
#### Registrations sent to EDS

### Receiving AP (corner 3)
#### Registrations sent to EDS

### Receiving EMR AP (corner 3)
#### Registrations sent to EDS

## Other services

### EAS

### EDS component

## EER
