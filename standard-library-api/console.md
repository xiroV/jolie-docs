# Include library: console.iol

Inclusion code: <code>include "console.iol"</code>

<table>
  <caption>Service Deployment</caption>
  <thead>
    <tr>
      <th>Port Name</th>
      <th>Location</th>
      <th>Protocol</th>
      <th>Interfaces</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ConsoleInputPort</td>
      <td>local</td>
      <td>-</td>
      <td><a href="#ConsoleInputInterface">ConsoleInputInterface</a></td>
    </tr>
    <tr>
      <td>Console</td>
      <td>-</td>
      <td>-</td>
      <td><a href="#ConsoleInterface">ConsoleInterface</a></td>
    </tr>
  </tbody>
</table>

<h3>List of Available Interfaces</h3>

<h3 id="ConsoleInputInterface">ConsoleInputInterface</h3>

<table>
  <thead>
    <tr>
      <th>Operation Name</th>
      <th>Input Type</th>
      <th>Output Type</th>
      <th>Faults</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="#in">in</a></td>
      <td><a href="#InRequest">InRequest</a></td>
      <td> - </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

### Operation Description


<a id="in"></a>
#### in


Invocation template: <code>in( request )</code>

**Request type**
<a id="InRequest"></a>
Type documentation: no documentation provided 
<pre>type InRequest: string {
	.token?: string
}</pre>





---





<h3 id="ConsoleInterface">ConsoleInterface</h3>

<table>
  <thead>
    <tr>
      <th>Operation Name</th>
      <th>Input Type</th>
      <th>Output Type</th>
      <th>Faults</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="#print">print</a></td>
      <td>undefined</a></td>
      <td>void</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#println">println</a></td>
      <td>undefined</a></td>
      <td>void</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#registerForInput">registerForInput</a></td>
      <td><a href="#RegisterForInputRequest">RegisterForInputRequest</a></td>
      <td>void</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#unsubscribeSessionListener">unsubscribeSessionListener</a></td>
      <td><a href="#UnsubscribeSessionListener">UnsubscribeSessionListener</a></td>
      <td>void</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#subscribeSessionListener">subscribeSessionListener</a></td>
      <td><a href="#SubscribeSessionListener">SubscribeSessionListener</a></td>
      <td>void</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#enableTimestamp">enableTimestamp</a></td>
      <td><a href="#EnableTimestampRequest">EnableTimestampRequest</a></td>
      <td>void</td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

### Operation Description


<a id="print"></a>
#### print


Invocation template: <code>print@Console( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---

<a id="println"></a>
#### println


Invocation template: <code>println@Console( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---

<a id="registerForInput"></a>
#### registerForInput
Operation documentation: 
	  it enables the console for input listening
	  parameter enableSessionListener enables console input listening for more than one service session (default=false)
	

Invocation template: <code>registerForInput@Console( request )( response )</code>

**Request type**
<a id="RegisterForInputRequest"></a>
Type documentation: no documentation provided 
<pre>type RegisterForInputRequest: void {
	.enableSessionListener?: bool
}</pre>


**Response type**

Type documentation: no documentation provided 





---

<a id="unsubscribeSessionListener"></a>
#### unsubscribeSessionListener
Operation documentation: 
	 it disables a session to receive inputs from the console, previously registered with subscribeSessionListener operation
	

Invocation template: <code>unsubscribeSessionListener@Console( request )( response )</code>

**Request type**
<a id="UnsubscribeSessionListener"></a>
Type documentation: no documentation provided 
<pre>type UnsubscribeSessionListener: void {
	.token: string
}</pre>


**Response type**

Type documentation: no documentation provided 





---

<a id="subscribeSessionListener"></a>
#### subscribeSessionListener
Operation documentation: 
	 it receives a token string which identifies a service session.
	 it enables the session to receive inputs from the console
	

Invocation template: <code>subscribeSessionListener@Console( request )( response )</code>

**Request type**
<a id="SubscribeSessionListener"></a>
Type documentation: no documentation provided 
<pre>type SubscribeSessionListener: void {
	.token: string
}</pre>


**Response type**

Type documentation: no documentation provided 





---

<a id="enableTimestamp"></a>
#### enableTimestamp
Operation documentation: 
		It enables timestamp inline printing for each console output operation call: print, println
		Parameter format allows to specifiy the timestamp output format. Bad Format will be printed out if format value is not allowed.
	

Invocation template: <code>enableTimestamp@Console( request )( response )</code>

**Request type**
<a id="EnableTimestampRequest"></a>
Type documentation: no documentation provided 
<pre>type EnableTimestampRequest: bool {
	.format?: string
}</pre>


**Response type**

Type documentation: no documentation provided 





---




