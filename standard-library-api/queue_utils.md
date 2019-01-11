# Include library: queue_utils.iol

Inclusion code: <code>include "queue_utils.iol"</code>

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
      <td>QueueUtils</td>
      <td>-</td>
      <td>-</td>
      <td><a href="#QueueUtilsInterface">QueueUtilsInterface</a></td>
    </tr>
  </tbody>
</table>

<h3>List of Available Interfaces</h3>

<h3 id="QueueUtilsInterface">QueueUtilsInterface</h3>

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
      <td><a href="#size">size</a></td>
      <td>string</td>
      <td>int</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#poll">poll</a></td>
      <td>string</td>
      <td>undefined</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#new_queue">new_queue</a></td>
      <td>string</td>
      <td>bool</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#delete_queue">delete_queue</a></td>
      <td>string</td>
      <td>bool</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#push">push</a></td>
      <td><a href="#QueueRequest">QueueRequest</a></td>
      <td>bool</td>
      <td>
      </td>
    </tr>
    <tr>
      <td><a href="#peek">peek</a></td>
      <td>string</td>
      <td>undefined</td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

### Operation Description


<a id="size"></a>
#### size


Invocation template: <code>size@QueueUtils( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---

<a id="poll"></a>
#### poll


Invocation template: <code>poll@QueueUtils( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---

<a id="new_queue"></a>
#### new_queue


Invocation template: <code>new_queue@QueueUtils( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---

<a id="delete_queue"></a>
#### delete_queue


Invocation template: <code>delete_queue@QueueUtils( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---

<a id="push"></a>
#### push


Invocation template: <code>push@QueueUtils( request )( response )</code>

**Request type**
<a id="QueueRequest"></a>
Type documentation: no documentation provided 
<pre>type QueueRequest: void {
	.queue_name: string
	.element: undefined
}</pre>


**Response type**

Type documentation: no documentation provided 





---

<a id="peek"></a>
#### peek


Invocation template: <code>peek@QueueUtils( request )( response )</code>

**Request type**

Type documentation: no documentation provided 



**Response type**

Type documentation: no documentation provided 





---




