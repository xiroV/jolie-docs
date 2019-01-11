# Include library: converter.iol

Inclusion code: <code>include "converter.iol"</code>

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
      <td>Converter</td>
      <td>-</td>
      <td>-</td>
      <td><a href="#ConverterInterface">ConverterInterface</a></td>
    </tr>
  </tbody>
</table>

<h3>List of Available Interfaces</h3>

<h3 id="ConverterInterface">ConverterInterface</h3>

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
      <td><a href="#stringToRaw">stringToRaw</a></td>
      <td><a href="#StringToRawRequest">StringToRawRequest</a></td>
      <td>raw</td>
      <td>
        IOException( <a href="#IOExceptionType">IOExceptionType</a> )
      </td>
    </tr>
    <tr>
      <td><a href="#base64ToRaw">base64ToRaw</a></td>
      <td>string</td>
      <td>raw</td>
      <td>
        IOException( <a href="#IOExceptionType">IOExceptionType</a> )
      </td>
    </tr>
    <tr>
      <td><a href="#rawToBase64">rawToBase64</a></td>
      <td>raw</td>
      <td>string</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#rawToString">rawToString</a></td>
      <td><a href="#RawToStringRequest">RawToStringRequest</a></td>
      <td>string</td>
      <td>
        IOException( <a href="#IOExceptionType">IOExceptionType</a> )
      </td>
    </tr>
  </tbody>
</table>

### Operation Description


<a id="stringToRaw"></a>
#### stringToRaw


Invocation template: <code>stringToRaw@Converter( request )( response )</code>

**Request type**
<a id="StringToRawRequest"></a>
Type documentation: no documentation provided 
<pre>type StringToRawRequest: string {
	.charset?: string
}</pre>


**Response type**

Type documentation: no documentation provided 



**Possible faults thrown**


Fault <code>IOException</code> with type <code>IOExceptionType</code>

Fault-handling install template: <code>install ( IOException => /* error-handling code */ )</code>
<pre>type IOExceptionType: JavaExceptionType</pre>

---

<a id="base64ToRaw"></a>
#### base64ToRaw


Invocation template: <code>base64ToRaw@Converter( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 



**Possible faults thrown**


Fault <code>IOException</code> with type <code>IOExceptionType</code>

Fault-handling install template: <code>install ( IOException => /* error-handling code */ )</code>
<pre>type IOExceptionType: JavaExceptionType</pre>

---

<a id="rawToBase64"></a>
#### rawToBase64


Invocation template: <code>rawToBase64@Converter( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---

<a id="rawToString"></a>
#### rawToString


Invocation template: <code>rawToString@Converter( request )( response )</code>

**Request type**
<a id="RawToStringRequest"></a>
Type documentation: no documentation provided 
<pre>type RawToStringRequest: raw {
	.charset?: string
}</pre>


**Response type**

Type documentation: no documentation provided 



**Possible faults thrown**


Fault <code>IOException</code> with type <code>IOExceptionType</code>

Fault-handling install template: <code>install ( IOException => /* error-handling code */ )</code>
<pre>type IOExceptionType: JavaExceptionType</pre>

---


<h4>Subtypes</h4>


<a id="IOExceptionType"></a>
IOExceptionType

<pre>type IOExceptionType: JavaExceptionType</pre>



