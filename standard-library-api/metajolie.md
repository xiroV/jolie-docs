# Include library: metajolie.iol

Inclusion code: <code>include "metajolie.iol"</code>

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
      <td>MetaJolie</td>
      <td>-</td>
      <td>-</td>
      <td><a href="#MetaJolieInterface">MetaJolieInterface</a></td>
    </tr>
  </tbody>
</table>

<h3>List of Available Interfaces</h3>

<h3 id="MetaJolieInterface">MetaJolieInterface</h3>

Interface documentation: 
WARNING: the API of this service is experimental. Use it at your own risk.


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
      <td><a href="#getInputPortMetaData">getInputPortMetaData</a></td>
      <td><a href="#GetInputPortMetaDataRequest">GetInputPortMetaDataRequest</a></td>
      <td><a href="#GetInputPortMetaDataResponse">GetInputPortMetaDataResponse</a></td>
      <td>
        ParserException( <a href="#ParserExceptionType">ParserExceptionType</a> ) <br> 
        InputPortMetaDataFault( undefined ) <br> 
        SemanticException( <a href="#SemanticExceptionType">SemanticExceptionType</a> )
      </td>
    </tr>
    <tr>
      <td><a href="#parseRoles">parseRoles</a></td>
      <td><a href="#ParseRoleRequest">ParseRoleRequest</a></td>
      <td><a href="#Role">Role</a></td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#getMetaData">getMetaData</a></td>
      <td><a href="#GetMetaDataRequest">GetMetaDataRequest</a></td>
      <td><a href="#GetMetaDataResponse">GetMetaDataResponse</a></td>
      <td>
        ParserException( <a href="#ParserExceptionType">ParserExceptionType</a> ) <br> 
        SemanticException( <a href="#SemanticExceptionType">SemanticExceptionType</a> )
      </td>
    </tr>
    <tr>
      <td><a href="#messageTypeCast">messageTypeCast</a></td>
      <td><a href="#MessageTypeCastRequest">MessageTypeCastRequest</a></td>
      <td><a href="#MessageTypeCastResponse">MessageTypeCastResponse</a></td>
      <td>
        TypeMismatch( undefined )
      </td>
    </tr>
    <tr>
      <td><a href="#checkNativeType">checkNativeType</a></td>
      <td><a href="#CheckNativeTypeRequest">CheckNativeTypeRequest</a></td>
      <td><a href="#CheckNativeTypeResponse">CheckNativeTypeResponse</a></td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

### Operation Description


<a id="getInputPortMetaData"></a>
#### getInputPortMetaData


Invocation template: <code>getInputPortMetaData@MetaJolie( request )( response )</code>

**Request type**
<a id="GetInputPortMetaDataRequest"></a>
Type documentation: no documentation provided 
<pre>type GetInputPortMetaDataRequest: void {
	.filename: string
	.name: Name
}</pre>


**Response type**
<a id="GetInputPortMetaDataResponse"></a>
Type documentation: no documentation provided 
<pre>type GetInputPortMetaDataResponse: void {
	.input*: Participant
}</pre>


**Possible faults thrown**


Fault <code>ParserException</code> with type <code>ParserExceptionType</code>

Fault-handling install template: <code>install ( ParserException => /* error-handling code */ )</code>
<pre>type ParserExceptionType: void {
	.line: int
	.sourceName: string
	.message: string
}</pre>


Fault <code>InputPortMetaDataFault</code> with type <code>undefined</code>

Fault-handling install template: <code>install ( InputPortMetaDataFault => /* error-handling code */ )</code>



Fault <code>SemanticException</code> with type <code>SemanticExceptionType</code>

Fault-handling install template: <code>install ( SemanticException => /* error-handling code */ )</code>
<pre>type SemanticExceptionType: void {
	.error*: void {
		.line: int
		.sourceName: string
		.message: string
	}
}</pre>

---

<a id="parseRoles"></a>
#### parseRoles


Invocation template: <code>parseRoles@MetaJolie( request )( response )</code>

**Request type**
<a id="ParseRoleRequest"></a>
Type documentation: no documentation provided 
<pre>type ParseRoleRequest: void {
	.filename: string
	.rolename: Name
}</pre>


**Response type**
<a id="Role"></a>
Type documentation: no documentation provided 
<pre>type Role: void {
	.output?: Participant
	.input: Participant
	.name: Name
	.conversation*: Conversation
}</pre>




---

<a id="getMetaData"></a>
#### getMetaData


Invocation template: <code>getMetaData@MetaJolie( request )( response )</code>

**Request type**
<a id="GetMetaDataRequest"></a>
Type documentation: no documentation provided 
<pre>type GetMetaDataRequest: void {
	.filename: string
	.name: Name
}</pre>


**Response type**
<a id="GetMetaDataResponse"></a>
Type documentation: no documentation provided 
<pre>type GetMetaDataResponse: void {
	.output*: Participant
	.input*: Participant
	.interfaces*: Interface
	.types*: Type
	.service: Service
	.embeddedServices*: void {
		.servicepath: string
		.type: string
		.portId: string
	}
}</pre>


**Possible faults thrown**


Fault <code>ParserException</code> with type <code>ParserExceptionType</code>

Fault-handling install template: <code>install ( ParserException => /* error-handling code */ )</code>
<pre>type ParserExceptionType: void {
	.line: int
	.sourceName: string
	.message: string
}</pre>


Fault <code>SemanticException</code> with type <code>SemanticExceptionType</code>

Fault-handling install template: <code>install ( SemanticException => /* error-handling code */ )</code>
<pre>type SemanticExceptionType: void {
	.error*: void {
		.line: int
		.sourceName: string
		.message: string
	}
}</pre>

---

<a id="messageTypeCast"></a>
#### messageTypeCast


Invocation template: <code>messageTypeCast@MetaJolie( request )( response )</code>

**Request type**
<a id="MessageTypeCastRequest"></a>
Type documentation: no documentation provided 
<pre>type MessageTypeCastRequest: void {
	.types: void {
		.types*: Type
		.messageTypeName: Name
	}
	.message: undefined
}</pre>


**Response type**
<a id="MessageTypeCastResponse"></a>
Type documentation: no documentation provided 
<pre>type MessageTypeCastResponse: void {
	.message: undefined
}</pre>


**Possible faults thrown**


Fault <code>TypeMismatch</code> with type <code>undefined</code>

Fault-handling install template: <code>install ( TypeMismatch => /* error-handling code */ )</code>


---

<a id="checkNativeType"></a>
#### checkNativeType


Invocation template: <code>checkNativeType@MetaJolie( request )( response )</code>

**Request type**
<a id="CheckNativeTypeRequest"></a>
Type documentation: no documentation provided 
<pre>type CheckNativeTypeRequest: void {
	.type_name: string
}</pre>


**Response type**
<a id="CheckNativeTypeResponse"></a>
Type documentation: no documentation provided 
<pre>type CheckNativeTypeResponse: void {
	.result: bool
}</pre>




---




