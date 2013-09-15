# tinytooltip
tinytooltip (900 bytes minified) is an extremely tiny, easy to use tooltip plugin for jQuery

Kailash Nadh, October 2011

License:	MIT License

Documentation and Demo: http://kailashnadh.name/code/tinytooltip

## Example

### HTML - Setup
<pre>
&lt;head&gt;
	&lt;script type="text/javascript" src="lib/jquery.min.js"&gt;&lt;/script&gt;

	&lt;link rel="stylesheet" type="text/css" href="src/jquery.tinytooltip.css"/&gt;
	&lt;script type="text/javascript" src="src/jquery.tinytooltip.min.js"&gt;&lt;/script&gt;
&lt;/head&gt;
</pre>

### Usage
<pre>
// == hover tooltip with static text
$('.example').tinytooltip({message: &quot;This is an example tooltip!&quot;});


// == on click tool tip with dynamic text
$('.example').tinytooltip({
	message: function(tip) {
		return $(this).val();
	},
	hover: false
});

$('.example').click(function() {
	$(this).trigger('showtooltip');	// show the tooltip
}).blur(function() {
	$(this).trigger('hidetooltip');	// hide the tooltip
});

</pre>

To show tooltips at will, set the 'hover' option to false while initializing the tooltip on an element. 
Then, to show the tooltip, use .trigger('showtooltip') and to hide, .trigger('hidetooltip')

## Options
<table border="1">
	<tbody>
		<tr>
			<td>message</td>
			<td>
				Tooltip message. Can be a string or a function()
			</td>
		</tr>
		<tr>
			<td>hover</td>
			<td>
				<strong><em>true</em> (default) or <em>false</em></strong><br />
				Standard tooltip behaviour. Show tooltip on mouseover and hideon mouseout
			</td>
		</tr>
		<tr>
			<td>classes</td>
			<td>
				Addition classes (separated by space) to be added to the tooltip div
			</td>
		</tr>
	</tbody>
</table>
	