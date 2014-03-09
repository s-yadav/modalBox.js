modalBox.js
===========

Modal window has become a very popular way of showing information in detail, and getting needed input while blocking the main application flow. There are large numbers of attractive plugin available over the internet with lot of options. But the question is do we need that all?

Fact is we only use 30 to 40 % of that plugin and for that 30 to 40 % we compromise to use a large size plugin. In internet world size matters a lot. Least the size of your page greater the loading speed.

So why not use a plugin which is much smaller and have options which we need the most. modalBox.js is a very light weight plugin packed with only most used features Its overall size is around 5.3 kb ( 2.5 kb minified).

Demo : <a href="http://ignitersworld.com/lab/modalBox.html#demo">http://ignitersworld.com/lab/modalBox.html#demo</a>
Examples
========

<strong>A simplest one</strong><br />
<pre>
<code>
$('.modalBox').modalBox();
//or
$('.modalBox').modalBox('open');
</code>
</pre>
<br />
<strong>Modal box with defined width and height</strong><br />
<pre>
<code>
$('.modalBox').modalBox({
'width':'500px',
'height':'500px'
});
</code>
</pre>
<strong><br />
Modal box with defined top and left</strong><br />
<pre>
<code>
$('.modalBox').modalBox({
'top':'100px',
'left':'100px'
});
</code>
</pre>
<br />
<strong>Modal box with all close options enable</strong><br />
<pre>
<code>
$('.modalBox').modalBox({
  	iconImg:'images/x.png',
		iconClose:true,
		keyClose:true,
		bodyClose:true
});
</code>
</pre>

<br />
<strong>Modal box with all and global close button</strong><br />
<pre>
<code>
$('.modalBox').modalBox({
		iconImg:'images/x.png',
		keyClose:true,
		iconClose:true,
		bodyClose:true
});
</code>
</pre>
<br />
<strong>Modal box with all callback functions</strong><br />
<pre>
<code>
$('.modalBox').modalBox({
		onOpen:function(){
			alert('successfully open');
			},
		onClose:function(){
			alert('successfully close');
			}
});
</code>
</pre>
<br />
<strong>Mutiple modal box functions</strong><br />
<pre>
<code>
$('.modalBox').modalBox({
        width:300,
        height:300,
        top:100,
        left:100,
        iconImg:'images/x.png',
        iconClose:true,
});

$('.modalBox2').modalBox({
        width:300,
        height:300,
        top:100,
        left:500,
        iconImg:'images/x.png',
        iconClose:true,
});
</code>
</pre>

Options
=======
<table width="100%" border="1">
  <thead>
  <tr>
    <td>Options</td>
    <td>Default</td>
    <td>Allowed</td>
    <td>Description</td>
  </tr>
  </thead>
  <tr>
    <td>width</td>
    <td>'auto' </td>
    <td>Width in any unit(px,%,em)</td>
    <td>Change the width of modal box. (Plugin will not do any calculation for width if defined.)</td>
  </tr>
  <tr>
    <td>height</td>
    <td>'auto'</td>
    <td>Height in any unit(px,%,em)</td>
    <td>Change the width of modal box. (Plugin will not do any calculation for height if defined.)</td>
  </tr>
  <tr>
    <td>top</td>
    <td>'auto' (50%)</td>
    <td>Top in any unit(px,%,em)</td>
    <td>Change the top position of modal box. (Plugin will not do any calculation for margin top if top is defined.)</td>
  </tr>
  <tr>
    <td>left</td>
    <td>'auto' (50%)</td>
    <td>Left in any unit(px,%,em)</td>
    <td>Change the left position of modal box. (Plugin will not do any calculation for margin left if left is defined.)</td>
  </tr>
  <tr>
    <td>overlay</td>
    <td>true</td>
    <td>true,false</td>
    <td>Overlay the body if overlay is true.(have class iw-modalOverlay)</td>
  </tr>
  <tr>
    <td>iconClose</td>
    <td>false</td>
    <td>true,false</td>
    <td>Show a close icon on top right corner to close modal box.</td>
  </tr>
  <tr>
    <td>keyClose</td>
    <td>true</td>
    <td>true,false</td>
    <td>Activate closing of modal box by pressing esc key while modal box is open.</td>
  </tr>
  <tr>
    <td>bodyClose</td>
    <td>true</td>
    <td>true,false</td>
    <td>Activate closing of modal box by clicking outside of modal box.</td>
  </tr>
  <tr>
    <td>iconImg</td>
    <td>''</td>
    <td>Image source</td>
    <td>Source of icon image to display. (have class iw-closeImg)</td>
  </tr>
</table>

Callback functions
==================
<table width="100%" border="1">
  <thead>
  <tr>
    <td>Function</td>
    <td>Description</td>
  </tr>
</thead>

  <tr>
    <td>onOpen</td>
    <td>This callback function will be fired just after modal box is successfully open.</td>
  </tr>
  <tr>
    <td>onClose</td>
    <td>This callback function will be fired just after modal box is successfully close.</td>
  </tr>
</table>

Methods
=======
  1. Plugin Method : Passed as first argument of plugin(If need to define).<br />
  ex: $('.modalBox').modalBox('close');
  <br />
</p>
<table width="100%" border="1">
    <thead>

  <tr>
    <td>Method</td>
    <td>Description</td>
  </tr>
  </thead>

  <tr>
    <td>open</td>
    <td>Method to open modal box. It is a default method ,so if no method is defined open will be called.</td>
  </tr>
  <tr>
    <td>close</td>
    <td>Method to close modal box(hide the modal box). Remove all events and element associated with modal box(except modal box itself.)</td>
  </tr>
</table>
<p>  2. Global Method: <br />
  ex: $.modalBox.close();<br />
</p>
<table width="100%" border="1">
  <thead>

  <tr>
    <td>Method</td>
    <td>Description</td>
  </tr>
  </thead>

  <tr>
    <td>close</td>
    <td>Close all currently opened modal box. Called by $.modalBox.close().</td>
  </tr>
</table>

Styling
=======
We have three classes related to modal box.<br />
<ol>
<li><span class="highlight">iw-modalBox</span> for modal box.</li>
<li><span class="highlight">iw-modalOverlay</span> for overlay.</li>
<li><span class="highlight">iw-closeImg</span> for close icon.</li>
</ol>
Example
<pre><code>
.iw-modalBox{
	padding:5px;
	border:1px solid #CCC;
}

.iw-modalOverlay{
	background: #000;
	opacity:.6;
}
</code>
</pre>
