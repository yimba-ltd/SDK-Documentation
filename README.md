---
title: Yimba SDK Documentation
author: Jamie Williams - CTO - Yimba Ltd

---

<h1 id="yimba-sdk-documentation">Yimba SDK Documentation</h1>
<h2 id="introduction">Introduction</h2>
<p>This document describes the use and integration of the Yimba SDK into your application. The Yimba SDK provides quick and simple integration to new or existing applications allowing you to build a digital mobile wallet with only 5 lines of code! The Yimba SDK returns prebuilt components to your UI within a single line of code.</p>
<h2 id="sdk-installation">SDK Installation</h2>
<p>The SDK can be installed via NPM using standard methods.</p>
<p><strong>Using NPM</strong></p>
<pre><code>$ npm i yimba-sdk
</code></pre>
<p><strong>Using Yarn</strong></p>
<pre><code>$ yarn add yimba-sdk
</code></pre>
<h2 id="available-components">Available Components</h2>

<table>
<thead>
<tr>
<th>Component Name</th>
<th>Function</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>YimbaHeader</strong></td>
<td>Displays a configurable header component allowing you to customise the Title, Iconography and Function of buttons.</td>
</tr>
<tr>
<td><strong>YimbaCard</strong></td>
<td>Displays a Payment Card Preview with any currently applied Card Customisation.</td>
</tr>
<tr>
<td><strong>YimbaDesigns</strong></td>
<td>Displays all available card customisation options available to your card program. This component contains the Yimba Card Component that will dynamically re-render allowing new card art to be previewed before being applied</td>
</tr>
<tr>
<td><strong>YimbaDesignHistory</strong></td>
<td>Displays all previously set card art designs for a given payment card.</td>
</tr>
</tbody>
</table><h2 id="sdk-overview">SDK Overview</h2>
<p>In order to use the Yimba SDK, you will need to have been issued your unique <strong>Authentication Identification, Client Identification and Passkey</strong>. You <strong>will not</strong> be able to make use of the Yimba SDK without these elements being issued by Yimba. The below diagram gives you a basic overview of the process when utilising the SDK.</p>
<h3 id="basic-sdk-overview">Basic SDK Overview</h3>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-3Zgw3TO995mXhfZY" width="100%" style="max-width: 738.58984375px;" viewBox="0 0 738.58984375 460.9078063964844"><g transform="translate(-12, -12)"><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath" style="opacity: 1;"><path class="path" d="M335.03515625,56.10029735098521L86.4296875,104L124.88473360655738,142" marker-end="url(#arrowhead122)" style="fill:none"></path><defs><marker id="arrowhead122" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M171.43557889344262,142L209.890625,104L335.03515625,64.4745464474243" marker-end="url(#arrowhead123)" style="fill:none"></path><defs><marker id="arrowhead123" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M380.2880379098361,66L342.71875,104L380.2880379098361,142" marker-end="url(#arrowhead124)" style="fill:none"></path><defs><marker id="arrowhead124" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M435.12660092213116,142L488.16015625,104L435.12660092213116,66" marker-end="url(#arrowhead125)" style="fill:none"></path><defs><marker id="arrowhead125" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M403.02734375,188L403.02734375,213L475.5187067157478,274.0516088360102" marker-end="url(#arrowhead126)" style="fill:none"></path><defs><marker id="arrowhead126" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M471.01953125,62.28309905197777L618.11328125,104L618.11328125,165L618.11328125,213L546.6219215994067,274.0516060476488" marker-end="url(#arrowhead127)" style="fill:none"></path><defs><marker id="arrowhead127" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M511.07031250000006,369.4078094482426L510.5703125,393.9078063964844L542.986083984375,418.9078063964844" marker-end="url(#arrowhead128)" style="fill:none"></path><defs><marker id="arrowhead128" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M654.162109375,418.9078063964844L742.58984375,393.9078063964844L742.58984375,303.4539031982422L742.58984375,213L742.58984375,165L742.58984375,104L471.01953125,55.214315295416895" marker-end="url(#arrowhead129)" style="fill:none"></path><defs><marker id="arrowhead129" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="translate(86.4296875,104)" style="opacity: 1;"><g transform="translate(-66.4296875,-13)" class="label"><foreignObject width="132.859375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">ClientID &amp; Passkey</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(209.890625,104)" style="opacity: 1;"><g transform="translate(-37.03125,-13)" class="label"><foreignObject width="74.0625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">AuthToken</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(342.71875,104)" style="opacity: 1;"><g transform="translate(-75.796875,-13)" class="label"><foreignObject width="151.59375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">ClientID &amp; AuthToken</span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(488.16015625,104)" style="opacity: 1;"><g transform="translate(-24.8203125,-13)" class="label"><foreignObject width="49.640625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">CardID</span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(618.11328125,165)" style="opacity: 1;"><g transform="translate(-104.4765625,-13)" class="label"><foreignObject width="208.953125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">AuthToken, ClientID &amp; CardID</span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g></g><g class="nodes"><g class="node" id="App" transform="translate(403.02734375,43)" style="opacity: 1;"><rect rx="0" ry="0" x="-67.9921875" y="-23" width="135.984375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-57.9921875,-13)"><foreignObject width="115.984375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Your Application</div></foreignObject></g></g></g><g class="node" id="Auth0" transform="translate(148.16015625,165)" style="opacity: 1;"><rect rx="0" ry="0" x="-114.015625" y="-23" width="228.03125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-104.015625,-13)"><foreignObject width="208.03125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Yimba Authentication Service</div></foreignObject></g></g></g><g class="node" id="SDK" transform="translate(510.5703125,303.4539031982422)" style="opacity: 1;"><polygon points="65.45390625,0 130.9078125,-65.45390625 65.45390625,-130.9078125 0,-65.45390625" rx="5" ry="5" transform="translate(-65.45390625,65.45390625)"></polygon><g class="label" transform="translate(0,0)"><g transform="translate(-39.7265625,-13)"><foreignObject width="79.453125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Yimba SDK</div></foreignObject></g></g></g><g class="node" id="NewCard" transform="translate(403.02734375,165)" style="opacity: 1;"><rect rx="5" ry="5" x="-75.609375" y="-23" width="151.21875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-65.609375,-13)"><foreignObject width="131.21875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Register New Card</div></foreignObject></g></g></g><g class="node" id="Comp" transform="translate(572.80859375,441.9078063964844)" style="opacity: 1;"><rect rx="5" ry="5" x="-87.015625" y="-23" width="174.03125" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-77.015625,-13)"><foreignObject width="154.03125" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Rendered Component</div></foreignObject></g></g></g></g></g></g></svg></div>
<h3 id="process-overview">Process Overview</h3>
<p>Your application must first call the Yimba Authentication Service passing both your <strong>AuthenticationID</strong> and <strong>PassKey</strong> with the request. The authentication service will issue a bearer token that will be valid for 24 hours. The Token Request method (<strong>requestToken</strong>)  will return a promise holding the token data for you to manage within your application.</p>
<p><strong>Obtain Auth Token</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">
    <span class="token keyword">import</span> <span class="token punctuation">{</span> requestToken <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'yimba-sdk'</span><span class="token punctuation">;</span>
    
    <span class="token function">_yourFunctionName</span><span class="token punctuation">(</span>authenticationID<span class="token punctuation">,</span> clientSecret<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token function">requestToken</span><span class="token punctuation">(</span>authenticationID<span class="token punctuation">,</span> clientSecret<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span><span class="token punctuation">(</span>authToken<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
    	    <span class="token comment">// handle the response as required within your app. For example, </span>
    	    <span class="token comment">// call a dispatch to Redux to store the token</span>
    	    <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span><span class="token function">setAPIToken</span><span class="token punctuation">(</span>authToken<span class="token punctuation">)</span><span class="token punctuation">;</span>
    	<span class="token punctuation">}</span><span class="token punctuation">)</span>
    <span class="token punctuation">}</span>

</code></pre>
<h2 id="section"></h2>
<p>If you are making a call to a Yimba Component and have not yet obtained a valid CardID, then you will need to request for a new card to be registered. When making this call, the Yimba SDK will return an identifier for the card registration. The Registration method requires both your issued <strong>ClientID</strong> and <strong>AuthToken</strong> as well as the Bin Range for the card. You can pass an optional JSON array for the <strong>DefaultCardImage</strong> to display the preset default card image prior to customisation. The <strong>DefaultCardImage</strong> array has the following available properties:-</p>

<table>
<thead>
<tr>
<th>PropName</th>
<th>PropType</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ImageName</strong></td>
<td>string</td>
<td>e.g ‘My Default Image’</td>
</tr>
<tr>
<td><strong>ImageType</strong></td>
<td>DefaultImageType</td>
<td>one of the available values from <strong>DefaultImageTypes</strong> within the Yimba SDK, e.g. ‘URL’ or ‘BASE64’</td>
</tr>
<tr>
<td><strong>ImageData</strong></td>
<td>string</td>
<td>Image data as a string. Either the given image URL or its BASE64 encoded data</td>
</tr>
</tbody>
</table><p><strong>Example Default Image Array</strong></p>
<p><em>Passing Image as URL</em></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token punctuation">[</span>
	<span class="token punctuation">{</span>
		<span class="token string">"ImageName"</span><span class="token punctuation">:</span> <span class="token string">"My Default Image"</span><span class="token punctuation">,</span>
		<span class="token string">"ImageType"</span><span class="token punctuation">:</span> <span class="token string">"URL"</span><span class="token punctuation">,</span>
		<span class="token string">"ImageData"</span><span class="token punctuation">:</span> <span class="token string">"https://pbs.twimg.com/profile_images/735509975649378305/B81JwLT7.jpg"</span>
	<span class="token punctuation">}</span><span class="token punctuation">,</span>
<span class="token punctuation">]</span>
</code></pre>
<p><em>Passing Image as BASE64 Encoded Data</em></p>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token punctuation">[</span>
	<span class="token punctuation">{</span>
		<span class="token string">"ImageName"</span><span class="token punctuation">:</span> <span class="token string">"My Default Image"</span><span class="token punctuation">,</span>
		<span class="token string">"ImageType"</span><span class="token punctuation">:</span> <span class="token string">"BASE64"</span><span class="token punctuation">,</span>
		<span class="token string">"ImageData"</span><span class="token punctuation">:</span> <span class="token string">"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"</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">]</span>
</code></pre>
<p><strong>IMPORTANT NOTE:</strong> <em>The returned CardID is valid for the entire lifetime of the card and does not expire. You do not need to call this method unless you do not have a valid CardID to pass to the Yimba SDK</em>.</p>
<p><strong>Register a New Card</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">
    <span class="token keyword">import</span> <span class="token punctuation">{</span> registerCard <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'yimba-sdk'</span><span class="token punctuation">;</span>
    
    <span class="token function">_yourFunctionName</span><span class="token punctuation">(</span>bearerToken<span class="token punctuation">,</span> clientId<span class="token punctuation">,</span> DefaultCardImageURL<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    	<span class="token function">registerCard</span><span class="token punctuation">(</span>bearerToken<span class="token punctuation">,</span> clientId<span class="token punctuation">,</span> <span class="token string">'BIN Number'</span><span class="token punctuation">,</span> DefaultCardImageURL<span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">then</span><span class="token punctuation">(</span><span class="token punctuation">(</span>newCardToken<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
    		<span class="token comment">// handle the response as required within your app. For example, </span>
    	    <span class="token comment">// call a dispatch to Redux to store the card token</span>
    		<span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span><span class="token function">setCardID</span><span class="token punctuation">(</span>newCardToken<span class="token punctuation">)</span><span class="token punctuation">;</span>
    	<span class="token punctuation">}</span><span class="token punctuation">)</span>
    <span class="token punctuation">}</span>

</code></pre>
<h2 id="using-yimba-sdk-components">Using Yimba SDK Components</h2>
<p>This section details the usage of the individual components available within the SDK.</p>
<h3 id="yimbaheader">YimbaHeader</h3>
<p>The <strong>YimbaHeader</strong> component is an optional component that can assist you in creating a common header display for each page within your app. The component displays a configurable header allowing you to customise the Title, Iconography and Function of buttons.  The <strong>YimbaHeader</strong> component takes optional parameters <strong>headerIcon</strong>, <strong>headerTitle</strong>, <strong>hasLeftButton</strong>, <strong>leftAction</strong>. The <strong>leftAction</strong> property allows you to pass a function to the header to set the action of the Header Button. For Example, the action this.props.navigation.goBack() is passed in the code below to push the navigation stack backwards.</p>
<p><strong>Basic Usage</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaHeader <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'yimba-sdk'</span>
    
    <span class="token operator">&lt;</span>YimbaHeader headerTitle<span class="token operator">=</span><span class="token string">'Your Page Name'</span>  <span class="token operator">/</span><span class="token operator">&gt;</span>
</code></pre>
<p><strong>Example Basic Output</strong><br>
<img src="https://s3.eu-west-2.amazonaws.com/yimba.images/SDKDocs/BasicHeader.png" alt="enter image description here"></p>
<p><strong>Advanced Usage</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaHeader <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'yimba-sdk'</span>
    
    <span class="token operator">&lt;</span>YimbaHeader headerTitle<span class="token operator">=</span><span class="token string">'Your Page Name'</span> 
	    hasLeftButton<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
	    headerIcon<span class="token operator">=</span><span class="token string">'arrow-back'</span>
	    leftAction<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span>  <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>navigation<span class="token punctuation">.</span><span class="token function">goBack</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">}</span>
	<span class="token operator">/</span><span class="token operator">&gt;</span>
</code></pre>
<p><strong>Example Advanced Output</strong><br>
<img src="https://s3.eu-west-2.amazonaws.com/yimba.images/SDKDocs/AdvancedHeader.png" alt="enter image description here"></p>
<h3 id="yimbacard">YimbaCard</h3>
<p>The <strong>YimbaCard</strong> component displays a Payment Card Preview with any currently applied Card Customisation. This includes pre-rendered overlays for the Card Issuer and Program as shown below. In order to make use of the <strong>YimbaCard</strong> component, you will need to pass a valid <strong>AuthenticationToken, ClientID &amp; CardID.</strong></p>
<p><strong>Required Component</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaCard <span class="token punctuation">}</span> <span class="token keyword">from</span>  <span class="token string">'yimba-sdk'</span>
    
    <span class="token operator">&lt;</span>YimbaCard bearerToken<span class="token operator">=</span><span class="token punctuation">{</span>apiToken<span class="token punctuation">}</span> clientId<span class="token operator">=</span><span class="token punctuation">{</span>clientId<span class="token punctuation">}</span> cardIdentifier<span class="token operator">=</span><span class="token punctuation">{</span>cardId<span class="token punctuation">}</span>  <span class="token operator">/</span><span class="token operator">&gt;</span>
</code></pre>
<p><strong>Example Usage in Basic View</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span>  React<span class="token punctuation">,</span> <span class="token punctuation">{</span> Component <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'react'</span>
    <span class="token keyword">import</span> <span class="token punctuation">{</span> View <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'react-native'</span>
    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaCard <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'yimba-sdk'</span>
    
    <span class="token keyword">class</span> <span class="token class-name">ExampleScreen</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
    <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    		<span class="token keyword">return</span> <span class="token punctuation">(</span>
    			<span class="token operator">&lt;</span>View<span class="token operator">&gt;</span>
					<span class="token operator">&lt;</span>YimbaCard bearerToken<span class="token operator">=</span><span class="token punctuation">{</span>apiToken<span class="token punctuation">}</span> clientId<span class="token operator">=</span><span class="token punctuation">{</span>clientId<span class="token punctuation">}</span> cardIdentifier<span class="token operator">=</span><span class="token punctuation">{</span>cardId<span class="token punctuation">}</span> <span class="token operator">/</span><span class="token operator">&gt;</span>
    			<span class="token operator">&lt;</span><span class="token operator">/</span>View <span class="token operator">&gt;</span>
    		<span class="token punctuation">)</span>
    	<span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
    
    <span class="token keyword">export</span> <span class="token keyword">default</span> ExampleScreen<span class="token punctuation">;</span>
</code></pre>
<p><strong>Example YimbaCard Output</strong></p>
<p><img src="https://s3.eu-west-2.amazonaws.com/yimba.images/SDKDocs/WalletOverview.png" alt="enter image description here"></p>
<h3 id="yimbadesignhistory">YimbaDesignHistory</h3>
<p>The <strong>YimbaDesignHistory</strong> component displays all of the previous applied designs to the card as specified by the <strong>CardID</strong> to allow previous designs to be re-selected and applied to the card easily. In order to make use of the <strong>YimbaDesignHistory</strong> component, you will need to pass a valid <strong>AuthenticationToken, ClientID &amp; CardID.</strong></p>
<p><strong>Required Component</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaDesignHistory <span class="token punctuation">}</span> <span class="token keyword">from</span>  <span class="token string">'yimba-sdk'</span>
    
    <span class="token operator">&lt;</span>YimbaDesignHistory bearerToken<span class="token operator">=</span><span class="token punctuation">{</span>apiToken<span class="token punctuation">}</span> clientId<span class="token operator">=</span><span class="token punctuation">{</span>clientId<span class="token punctuation">}</span> cardIdentifier<span class="token operator">=</span><span class="token punctuation">{</span>cardId<span class="token punctuation">}</span>  <span class="token operator">/</span><span class="token operator">&gt;</span>
</code></pre>
<p><strong>Example Usage in Basic View</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span>  React<span class="token punctuation">,</span> <span class="token punctuation">{</span> Component <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'react'</span>
    <span class="token keyword">import</span> <span class="token punctuation">{</span> View <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'react-native'</span>
    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaDesignHistory <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'yimba-sdk'</span>
    
    <span class="token keyword">class</span> <span class="token class-name">ExampleScreen</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
    <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    		<span class="token keyword">return</span> <span class="token punctuation">(</span>
    			<span class="token operator">&lt;</span>View<span class="token operator">&gt;</span>
					<span class="token operator">&lt;</span>YimbaCard bearerToken<span class="token operator">=</span><span class="token punctuation">{</span>apiToken<span class="token punctuation">}</span> clientId<span class="token operator">=</span><span class="token punctuation">{</span>clientId<span class="token punctuation">}</span> cardIdentifier<span class="token operator">=</span><span class="token punctuation">{</span>cardId<span class="token punctuation">}</span> <span class="token operator">/</span><span class="token operator">&gt;</span>
					<span class="token operator">&lt;</span>YimbaDesignHistory bearerToken<span class="token operator">=</span><span class="token punctuation">{</span>apiToken<span class="token punctuation">}</span> clientId<span class="token operator">=</span><span class="token punctuation">{</span>clientId<span class="token punctuation">}</span> cardIdentifier<span class="token operator">=</span><span class="token punctuation">{</span>cardId<span class="token punctuation">}</span><span class="token operator">/</span><span class="token operator">&gt;</span>
    			<span class="token operator">&lt;</span><span class="token operator">/</span>View <span class="token operator">&gt;</span>
    		<span class="token punctuation">)</span>
    	<span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
    
    <span class="token keyword">export</span> <span class="token keyword">default</span> ExampleScreen<span class="token punctuation">;</span>
</code></pre>
<p><strong>Example YimbaDesignHistory Output</strong></p>
<p><img src="https://s3.eu-west-2.amazonaws.com/yimba.images/SDKDocs/DesignHistory.png" alt="enter image description here"></p>
<h3 id="yimbadesigns">YimbaDesigns</h3>
<p>The <strong>YimbaDesigns</strong> component displays all available card customisation options available to your card program. This component contains the Yimba Card Component that will dynamically re-render allowing new card art to be previewed before being applied. In order to make use of the <strong>YimbaDesigns</strong> component, you will need to pass a valid <strong>AuthenticationToken, ClientID &amp; CardID.</strong></p>
<p><strong>Required Component</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaDesigns <span class="token punctuation">}</span> <span class="token keyword">from</span>  <span class="token string">'yimba-sdk'</span>
    
    <span class="token operator">&lt;</span>YimbaDesigns bearerToken<span class="token operator">=</span><span class="token punctuation">{</span>apiToken<span class="token punctuation">}</span> clientId<span class="token operator">=</span><span class="token punctuation">{</span>clientId<span class="token punctuation">}</span> cardIdentifier<span class="token operator">=</span><span class="token punctuation">{</span>cardId<span class="token punctuation">}</span>  <span class="token operator">/</span><span class="token operator">&gt;</span>
</code></pre>
<p><strong>Example Usage in Basic View</strong></p>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token keyword">import</span>  React<span class="token punctuation">,</span> <span class="token punctuation">{</span> Component <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'react'</span>
    <span class="token keyword">import</span> <span class="token punctuation">{</span> View <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'react-native'</span>
    <span class="token keyword">import</span> <span class="token punctuation">{</span> YimbaDesigns <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">'yimba-sdk'</span>
    
    <span class="token keyword">class</span> <span class="token class-name">ExampleScreen</span> <span class="token keyword">extends</span> <span class="token class-name">Component</span> <span class="token punctuation">{</span>
    <span class="token function">render</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    		<span class="token keyword">return</span> <span class="token punctuation">(</span>
    			<span class="token operator">&lt;</span>View<span class="token operator">&gt;</span>
					<span class="token operator">&lt;</span>YimbaDesigns bearerToken<span class="token operator">=</span><span class="token punctuation">{</span>apiToken<span class="token punctuation">}</span> clientId<span class="token operator">=</span><span class="token punctuation">{</span>clientId<span class="token punctuation">}</span> cardIdentifier<span class="token operator">=</span><span class="token punctuation">{</span>cardId<span class="token punctuation">}</span> <span class="token operator">/</span><span class="token operator">&gt;</span>
    			<span class="token operator">&lt;</span><span class="token operator">/</span>View <span class="token operator">&gt;</span>
    		<span class="token punctuation">)</span>
    	<span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
    
    <span class="token keyword">export</span> <span class="token keyword">default</span> ExampleScreen<span class="token punctuation">;</span>
</code></pre>
<p><strong>Example YimbaDesigns Output</strong></p>
<p><img src="https://s3.eu-west-2.amazonaws.com/yimba.images/SDKDocs/Designs.png" alt="enter image description here">    <img src="https://s3.eu-west-2.amazonaws.com/yimba.images/SDKDocs/ApplyDesign.png" alt="enter image description here"></p>

