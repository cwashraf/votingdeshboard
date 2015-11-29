<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
<head>
<title>redux-client</title>
<!-- 2015-11-29 Sun 04:16 -->
<meta  http-equiv="Content-Type" content="text/html;charset=utf-8" />
<meta  name="generator" content="Org-mode" />
<meta  name="author" content="root" />
<style type="text/css">
 <!--/*--><![CDATA[/*><!--*/
  .title  { text-align: center; }
  .todo   { font-family: monospace; color: red; }
  .done   { color: green; }
  .tag    { background-color: #eee; font-family: monospace;
            padding: 2px; font-size: 80%; font-weight: normal; }
  .timestamp { color: #bebebe; }
  .timestamp-kwd { color: #5f9ea0; }
  .right  { margin-left: auto; margin-right: 0px;  text-align: right; }
  .left   { margin-left: 0px;  margin-right: auto; text-align: left; }
  .center { margin-left: auto; margin-right: auto; text-align: center; }
  .underline { text-decoration: underline; }
  #postamble p, #preamble p { font-size: 90%; margin: .2em; }
  p.verse { margin-left: 3%; }
  pre {
    border: 1px solid #ccc;
    box-shadow: 3px 3px 3px #eee;
    padding: 8pt;
    font-family: monospace;
    overflow: auto;
    margin: 1.2em;
  }
  pre.src {
    position: relative;
    overflow: visible;
    padding-top: 1.2em;
  }
  pre.src:before {
    display: none;
    position: absolute;
    background-color: white;
    top: -10px;
    right: 10px;
    padding: 3px;
    border: 1px solid black;
  }
  pre.src:hover:before { display: inline;}
  pre.src-sh:before    { content: 'sh'; }
  pre.src-bash:before  { content: 'sh'; }
  pre.src-emacs-lisp:before { content: 'Emacs Lisp'; }
  pre.src-R:before     { content: 'R'; }
  pre.src-perl:before  { content: 'Perl'; }
  pre.src-java:before  { content: 'Java'; }
  pre.src-sql:before   { content: 'SQL'; }

  table { border-collapse:collapse; }
  caption.t-above { caption-side: top; }
  caption.t-bottom { caption-side: bottom; }
  td, th { vertical-align:top;  }
  th.right  { text-align: center;  }
  th.left   { text-align: center;   }
  th.center { text-align: center; }
  td.right  { text-align: right;  }
  td.left   { text-align: left;   }
  td.center { text-align: center; }
  dt { font-weight: bold; }
  .footpara:nth-child(2) { display: inline; }
  .footpara { display: block; }
  .footdef  { margin-bottom: 1em; }
  .figure { padding: 1em; }
  .figure p { text-align: center; }
  .inlinetask {
    padding: 10px;
    border: 2px solid gray;
    margin: 10px;
    background: #ffffcc;
  }
  #org-div-home-and-up
   { text-align: right; font-size: 70%; white-space: nowrap; }
  textarea { overflow-x: auto; }
  .linenr { font-size: smaller }
  .code-highlighted { background-color: #ffff00; }
  .org-info-js_info-navigation { border-style: none; }
  #org-info-js_console-label
    { font-size: 10px; font-weight: bold; white-space: nowrap; }
  .org-info-js_search-highlight
    { background-color: #ffff00; color: #000000; font-weight: bold; }
  /*]]>*/-->
</style>
<script type="text/javascript">
/*
@licstart  The following is the entire license notice for the
JavaScript code in this tag.

Copyright (C) 2012-2013 Free Software Foundation, Inc.

The JavaScript code in this tag is free software: you can
redistribute it and/or modify it under the terms of the GNU
General Public License (GNU GPL) as published by the Free Software
Foundation, either version 3 of the License, or (at your option)
any later version.  The code is distributed WITHOUT ANY WARRANTY;
without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE.  See the GNU GPL for more details.

As additional permission under GNU GPL version 3 section 7, you
may distribute non-source (e.g., minimized or compacted) forms of
that code without the copy of the GNU GPL normally required by
section 4, provided you include this license notice and a URL
through which recipients can access the Corresponding Source.


@licend  The above is the entire license notice
for the JavaScript code in this tag.
*/
<!--/*--><![CDATA[/*><!--*/
 function CodeHighlightOn(elem, id)
 {
   var target = document.getElementById(id);
   if(null != target) {
     elem.cacheClassElem = elem.className;
     elem.cacheClassTarget = target.className;
     target.className = "code-highlighted";
     elem.className   = "code-highlighted";
   }
 }
 function CodeHighlightOff(elem, id)
 {
   var target = document.getElementById(id);
   if(elem.cacheClassElem)
     elem.className = elem.cacheClassElem;
   if(elem.cacheClassTarget)
     target.className = elem.cacheClassTarget;
 }
/*]]>*///-->
</script>
</head>
<body>
<div id="content">
<h1 class="title">redux-client</h1>
<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. <span class="done DONE">DONE</span> What You Will Need</a>
<ul>
<li><a href="#sec-1-1">1.1. </a></li>
<li><a href="#sec-1-2">1.2. Install following packages</a>
<ul>
<li><a href="#sec-1-2-1">1.2.1. <span class="done DONE">DONE</span> Node</a></li>
<li><a href="#sec-1-2-2">1.2.2. <span class="done DONE">DONE</span> ES6</a></li>
<li><a href="#sec-1-2-3">1.2.3. React</a></li>
<li><a href="#sec-1-2-4">1.2.4. Webpack</a></li>
<li><a href="#sec-1-2-5">1.2.5. and Babel</a></li>
</ul>
</li>
<li><a href="#sec-1-3">1.3. <span class="todo TOMORROW">TOMORROW</span> For good introduction we need to take a look at SurviveJS</a></li>
</ul>
</li>
<li><a href="#sec-2">2. The App</a>
<ul>
<li><a href="#sec-2-1">2.1. We'll be developing an application for organizing live votes</a>
<ul>
<li><a href="#sec-2-1-1">2.1.1. for parties, conferences, meetings, and other gatherings of people.</a></li>
</ul>
</li>
<li><a href="#sec-2-2">2.2. For example, here's how a vote on the best Danny Boyle film</a></li>
<li><a href="#sec-2-3">2.3. The app will have two separate user interfaces: The voting UI</a></li>
</ul>
</li>
<li><a href="#sec-3">3. The Architecture</a>
<ul>
<li><a href="#sec-3-1">3.1. The system will technically consist of two applications:</a></li>
<li><a href="#sec-3-2">3.2. We're going to use Redux to organize the application code</a></li>
<li><a href="#sec-3-3">3.3. Even though there'll be a lot of similarity between the</a></li>
</ul>
</li>
<li><a href="#sec-4">4. The Server Application</a>
<ul>
<li><a href="#sec-4-1">4.1. Description</a>
<ul>
<li><a href="#sec-4-1-1">4.1.1. We're going to write the Node application first and the React application after that. This will let us concentrate on the core logic before we start thinking about the UI.</a></li>
<li><a href="#sec-4-1-2">4.1.2. As we create the server app, we'll get acquainted with Redux and Immutable, and will see how an application built with them holds together. Redux is most often associated with React applications, but it really isn't limited to that use case. Part of what we're going to learn is how useful Redux can be in other contexts as well!</a></li>
</ul>
</li>
<li><a href="#sec-4-2">4.2. Designing The Application State Tree</a>
<ul>
<li><a href="#sec-4-2-1">4.2.1. Designing a Redux app often begins by thinking about the application state data structure. This is what describes what's going on in your application at any given time.</a></li>
<li><a href="#sec-4-2-2">4.2.2. All kinds of frameworks and architectures have state.</a></li>
</ul>
</li>
<li><a href="#sec-4-3">4.3. Project Setup</a>
<ul>
<li><a href="#sec-4-3-1">4.3.1. <span class="done DONE">DONE</span> This results in a directory with the single file "package.json" in it.</a></li>
<li><a href="#sec-4-3-2">4.3.2. <span class="done DONE">DONE</span> tests with mocha command</a></li>
<li><a href="#sec-4-3-3">4.3.3. <span class="done DONE">DONE</span> Place the command in package.json</a></li>
<li><a href="#sec-4-3-4">4.3.4. <span class="done DONE">DONE</span> Another thing we need to do is enable Babel's ES6/ES2015 language support. It's</a></li>
<li><a href="#sec-4-3-5">4.3.5. <span class="done DONE">DONE</span> test npm</a></li>
<li><a href="#sec-4-3-6">4.3.6. <span class="done DONE">DONE</span> Add immutability</a></li>
<li><a href="#sec-4-3-7">4.3.7. We need to let plug in chai-immutable before any tests are run.</a></li>
</ul>
</li>
<li><a href="#sec-4-4">4.4. Getting Comfortable With Immutable&#xa0;&#xa0;&#xa0;<span class="tag"><span class="IMMUTABLE">IMMUTABLE</span></span></a>
<ul>
<li><a href="#sec-4-4-1">4.4.1. The state is not just a tree, but it is in fact an immutable tree.</a></li>
<li><a href="#sec-4-4-2">4.4.2. the next state is another state tree that reflects the current changes</a></li>
<li><a href="#sec-4-4-3">4.4.3. Two successive states of the application are stored in two separate and independent trees.</a></li>
<li><a href="#sec-4-4-4">4.4.4. How you get from one to the next is by applying a function that takes the current state and returns a new state.</a></li>
<li><a href="#sec-4-4-5">4.4.5. Immutability Helpful for debuging</a></li>
<li><a href="#sec-4-4-6">4.4.6. Data in, data out , pure function</a></li>
<li><a href="#sec-4-4-7">4.4.7. Immutable data structures are the material we'll build our application's state</a></li>
<li><a href="#sec-4-4-8">4.4.8. Unit Testing Immutable Counter</a></li>
</ul>
</li>
<li><a href="#sec-4-5">4.5. Writing The Application Logic With Pure Functions</a>
<ul>
<li><a href="#sec-4-5-1">4.5.1. Loading Entries</a></li>
<li><a href="#sec-4-5-2">4.5.2. Starting The Vote Second state</a></li>
<li><a href="#sec-4-5-3">4.5.3. Voting</a></li>
<li><a href="#sec-4-5-4">4.5.4. Moving to The Next Pair</a></li>
<li><a href="#sec-4-5-5">4.5.5. Ending The Vote</a></li>
</ul>
</li>
<li><a href="#sec-4-6">4.6. Introducing Actions and Reducers</a></li>
<li><a href="#sec-4-7">4.7. A Taste of Reducer Composition</a></li>
<li><a href="#sec-4-8">4.8. Introducing The Redux Store</a></li>
<li><a href="#sec-4-9">4.9. Setting Up a Socket.io Server</a></li>
<li><a href="#sec-4-10">4.10. Broadcasting State from A Redux Listener</a></li>
<li><a href="#sec-4-11">4.11. Receiving Remote Redux Actions</a></li>
</ul>
</li>
<li><a href="#sec-5">5. The Client Application</a>
<ul>
<li><a href="#sec-5-1">5.1. Introduction</a></li>
<li><a href="#sec-5-2">5.2. <span class="done DONE">DONE</span> Client Project Setup</a>
<ul>
<li><a href="#sec-5-2-1">5.2.1. Introduction</a></li>
<li><a href="#sec-5-2-2">5.2.2. Unit Testing support</a></li>
<li><a href="#sec-5-2-3">5.2.3. React and react-hot-loader</a></li>
<li><a href="#sec-5-2-4">5.2.4. Writing The UI for The Voting Screen</a></li>
</ul>
</li>
<li><a href="#sec-5-3">5.3. <span class="done DONE">DONE</span> Immutable Data And Pure Rendering</a>
<ul>
<li><a href="#sec-5-3-1">5.3.1. Introduction</a></li>
<li><a href="#sec-5-3-2">5.3.2. Testing PureRenderMixin</a></li>
</ul>
</li>
<li><a href="#sec-5-4">5.4. <span class="done DONE">DONE</span> Writing The UI for The Results Screen And Handling Routing</a>
<ul>
<li><a href="#sec-5-4-1">5.4.1. Voting Screen</a></li>
<li><a href="#sec-5-4-2">5.4.2. Result Screen</a></li>
<li><a href="#sec-5-4-3">5.4.3. Router</a></li>
<li><a href="#sec-5-4-4">5.4.4. Implemantation of results screen</a></li>
</ul>
</li>
<li><a href="#sec-5-5">5.5. <span class="done DONE">DONE</span> Introducing A Client-Side Redux Store</a>
<ul>
<li><a href="#sec-5-5-1">5.5.1. <span class="done DONE">DONE</span> Introduction</a></li>
<li><a href="#sec-5-5-2">5.5.2. <span class="done DONE">DONE</span> State</a></li>
<li><a href="#sec-5-5-3">5.5.3. <span class="done DONE">DONE</span> Implemantation Details</a></li>
</ul>
</li>
<li><a href="#sec-5-6">5.6. <span class="done DONE">DONE</span> Getting Data In from Redux to React</a>
<ul>
<li><a href="#sec-5-6-1">5.6.1. Introduction</a></li>
<li><a href="#sec-5-6-2">5.6.2. Init</a></li>
<li><a href="#sec-5-6-3">5.6.3. react-redux provider</a></li>
</ul>
</li>
<li><a href="#sec-5-7">5.7. <span class="done DONE">DONE</span> Setting Up The Socket.io Client</a></li>
<li><a href="#sec-5-8">5.8. <span class="done DONE">DONE</span> Receiving Actions From The Server</a></li>
<li><a href="#sec-5-9">5.9. <span class="todo TODAY">TODAY</span> Dispatching Actions From React Components</a>
<ul>
<li><a href="#sec-5-9-1">5.9.1. Introduction</a></li>
<li><a href="#sec-5-9-2">5.9.2. <span class="todo TODAY">TODAY</span> Dispatching voting buttons</a></li>
<li><a href="#sec-5-9-3">5.9.3. <span class="done DONE">DONE</span> Action Createtor</a></li>
</ul>
</li>
<li><a href="#sec-5-10">5.10. <span class="todo TODAY">TODAY</span> Sending Actions To The Server Using Redux Middleware</a>
<ul>
<li><a href="#sec-5-10-1">5.10.1. A VOTE action is created and dispatched to the client-side Redux Store when the user votes.</a></li>
<li><a href="#sec-5-10-2">5.10.2. VOTE actions are handled by the client-side reducer by setting the hasVoted state.</a></li>
<li><a href="#sec-5-10-3">5.10.3. The server is ready to receive actions from clients via the action Socket.io event. It dispatches</a></li>
<li><a href="#sec-5-10-4">5.10.4. VOTE actions are handled by the serverside reducer by registering the vote and updating the tally.</a></li>
<li><a href="#sec-5-10-5">5.10.5. Middleware</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#sec-6">6. Exercises</a>
<ul>
<li><a href="#sec-6-1">6.1. 1. Invalid Vote Prevention</a></li>
<li><a href="#sec-6-2">6.2. 2. Improved Vote State Reset</a></li>
<li><a href="#sec-6-3">6.3. 3. Duplicate Vote Prevention</a></li>
<li><a href="#sec-6-4">6.4. 4. Restarting The Vote</a></li>
<li><a href="#sec-6-5">6.5. 5. Indicating Socket Connection State</a></li>
<li><a href="#sec-6-6">6.6. Bonus Challenge: Going Peer to Peer</a>
<ul>
<li><a href="#sec-6-6-1">6.6.1. Loading Entries</a></li>
<li><a href="#sec-6-6-2">6.6.2. Starting The Vote</a></li>
<li><a href="#sec-6-6-3">6.6.3. Voting</a></li>
<li><a href="#sec-6-6-4">6.6.4. Moving to The Next Pair</a></li>
<li><a href="#sec-6-6-5">6.6.5. Ending The Vote</a></li>
</ul>
</li>
<li><a href="#sec-6-7">6.7. Introducing Actions and Reducers</a></li>
<li><a href="#sec-6-8">6.8. A Taste of Reducer Composition</a></li>
<li><a href="#sec-6-9">6.9. Introducing The Redux Store</a></li>
<li><a href="#sec-6-10">6.10. Setting Up a Socket.io Server</a></li>
<li><a href="#sec-6-11">6.11. Broadcasting State from A Redux Listener</a></li>
<li><a href="#sec-6-12">6.12. Receiving Remote Redux Actions</a></li>
</ul>
</li>
</ul>
</div>
</div>
<div id="outline-container-sec-1" class="outline-2">
<h2 id="sec-1"><span class="section-number-2">1</span> <span class="done DONE">DONE</span> What You Will Need</h2>
<div class="outline-text-2" id="text-1">
<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
<caption class="t-above"><span class="table-number">Table 1:</span> Clock summary at <span class="timestamp-wrapper"><span class="timestamp">[2015-11-24 মঙ্গল 21:33]</span></span></caption>

<colgroup>
<col  class="left" />

<col  class="left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">Headline</th>
<th scope="col" class="left">Time</th>
</tr>
</thead>
<tbody>
<tr>
<td class="left"><b>Total time</b></td>
<td class="left"><b>0:22</b></td>
</tr>
</tbody>
<tbody>
<tr>
<td class="left">TODAY What You Will Need</td>
<td class="left">0:22</td>
</tr>
</tbody>
</table>
</div>
<div id="outline-container-sec-1-1" class="outline-3">
<h3 id="sec-1-1"><span class="section-number-3">1.1</span> <a href="http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html">http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html</a></h3>
</div>
<div id="outline-container-sec-1-2" class="outline-3">
<h3 id="sec-1-2"><span class="section-number-3">1.2</span> Install following packages</h3>
<div class="outline-text-3" id="text-1-2">
</div><div id="outline-container-sec-1-2-1" class="outline-4">
<h4 id="sec-1-2-1"><span class="section-number-4">1.2.1</span> <span class="done DONE">DONE</span> Node</h4>
<div class="outline-text-4" id="text-1-2-1">
<div class="org-src-container">

<pre class="src src-sh">node -v
</pre>
</div>
</div>
</div>
<div id="outline-container-sec-1-2-2" class="outline-4">
<h4 id="sec-1-2-2"><span class="section-number-4">1.2.2</span> <span class="done DONE">DONE</span> ES6</h4>
</div>
<div id="outline-container-sec-1-2-3" class="outline-4">
<h4 id="sec-1-2-3"><span class="section-number-4">1.2.3</span> React</h4>
</div>
<div id="outline-container-sec-1-2-4" class="outline-4">
<h4 id="sec-1-2-4"><span class="section-number-4">1.2.4</span> Webpack</h4>
</div>
<div id="outline-container-sec-1-2-5" class="outline-4">
<h4 id="sec-1-2-5"><span class="section-number-4">1.2.5</span> and Babel</h4>
</div>
</div>
<div id="outline-container-sec-1-3" class="outline-3">
<h3 id="sec-1-3"><span class="section-number-3">1.3</span> <span class="todo TOMORROW">TOMORROW</span> For good introduction we need to take a look at <a href="http://survivejs.com/">SurviveJS</a></h3>
</div>
</div>
<div id="outline-container-sec-2" class="outline-2">
<h2 id="sec-2"><span class="section-number-2">2</span> The App</h2>
<div class="outline-text-2" id="text-2">
</div><div id="outline-container-sec-2-1" class="outline-3">
<h3 id="sec-2-1"><span class="section-number-3">2.1</span> We'll be developing an application for organizing live votes</h3>
<div class="outline-text-3" id="text-2-1">
</div><div id="outline-container-sec-2-1-1" class="outline-4">
<h4 id="sec-2-1-1"><span class="section-number-4">2.1.1</span> for parties, conferences, meetings, and other gatherings of people.</h4>
</div>
</div>
<div id="outline-container-sec-2-2" class="outline-3">
<h3 id="sec-2-2"><span class="section-number-3">2.2</span> For example, here's how a vote on the best Danny Boyle film</h3>
<div class="outline-text-3" id="text-2-2">
<p>
could go:
The app puts entries against each other in pairs, until a winner is found. 
</p>
</div>
</div>

<div id="outline-container-sec-2-3" class="outline-3">
<h3 id="sec-2-3"><span class="section-number-3">2.3</span> The app will have two separate user interfaces: The voting UI</h3>
<div class="outline-text-3" id="text-2-3">
<p>
can be used on a mobile device, or anything else that has a
web browser. The results UI is designed to be beamed on a
projector or some other large screen. It'll show the results
of the running vote in real time.
</p>
</div>
</div>
</div>

<div id="outline-container-sec-3" class="outline-2">
<h2 id="sec-3"><span class="section-number-2">3</span> The Architecture</h2>
<div class="outline-text-2" id="text-3">
</div><div id="outline-container-sec-3-1" class="outline-3">
<h3 id="sec-3-1"><span class="section-number-3">3.1</span> The system will technically consist of two applications:</h3>
<div class="outline-text-3" id="text-3-1">
<p>
There's a browser app we'll make with React that provides
both the user interfaces, and a server app we'll make for
Node that handles the voting logic. Communication between the
two will be done using WebSockets.
</p>
</div>
</div>
<div id="outline-container-sec-3-2" class="outline-3">
<h3 id="sec-3-2"><span class="section-number-3">3.2</span> We're going to use Redux to organize the application code</h3>
<div class="outline-text-3" id="text-3-2">
<p>
both on the client and on the server. For holding the state
we'll use Immutable data structures.
</p>
</div>
</div>

<div id="outline-container-sec-3-3" class="outline-3">
<h3 id="sec-3-3"><span class="section-number-3">3.3</span> Even though there'll be a lot of similarity between the</h3>
<div class="outline-text-3" id="text-3-3">
<p>
client and server - both will use Redux, for example - this
isn't really a universal/isomorphic application and the two
won't actually share any code. 
</p>
</div>
</div>
</div>

<div id="outline-container-sec-4" class="outline-2">
<h2 id="sec-4"><span class="section-number-2">4</span> The Server Application</h2>
<div class="outline-text-2" id="text-4">
</div><div id="outline-container-sec-4-1" class="outline-3">
<h3 id="sec-4-1"><span class="section-number-3">4.1</span> Description</h3>
<div class="outline-text-3" id="text-4-1">
</div><div id="outline-container-sec-4-1-1" class="outline-4">
<h4 id="sec-4-1-1"><span class="section-number-4">4.1.1</span> We're going to write the Node application first and the React application after that. This will let us concentrate on the core logic before we start thinking about the UI.</h4>
</div>
<div id="outline-container-sec-4-1-2" class="outline-4">
<h4 id="sec-4-1-2"><span class="section-number-4">4.1.2</span> As we create the server app, we'll get acquainted with Redux and Immutable, and will see how an application built with them holds together. Redux is most often associated with React applications, but it really isn't limited to that use case. Part of what we're going to learn is how useful Redux can be in other contexts as well!</h4>
</div>
</div>
<div id="outline-container-sec-4-2" class="outline-3">
<h3 id="sec-4-2"><span class="section-number-3">4.2</span> Designing The Application State Tree</h3>
<div class="outline-text-3" id="text-4-2">
</div><div id="outline-container-sec-4-2-1" class="outline-4">
<h4 id="sec-4-2-1"><span class="section-number-4">4.2.1</span> Designing a Redux app often begins by thinking about the application state data structure. This is what describes what's going on in your application at any given time.</h4>
</div>
<div id="outline-container-sec-4-2-2" class="outline-4">
<h4 id="sec-4-2-2"><span class="section-number-4">4.2.2</span> All kinds of frameworks and architectures have state.</h4>
<div class="outline-text-4" id="text-4-2-2">
</div><ol class="org-ol"><li><a id="sec-4-2-2-1" name="sec-4-2-2-1"></a>In Ember apps and Backbone apps, state is in Models.<br  /></li>
<li><a id="sec-4-2-2-2" name="sec-4-2-2-2"></a>In Angular apps, state is often in Factories and Services.<br  /></li>
<li><a id="sec-4-2-2-3" name="sec-4-2-2-3"></a>In most Flux implementations, it is in Stores.<br  /></li>
<li><a id="sec-4-2-2-4" name="sec-4-2-2-4"></a>How does Redux differ from these<br  /><ol class="org-ol"><li><a id="sec-4-2-2-4-1" name="sec-4-2-2-4-1"></a>The main difference is that in Redux.<br  /></li>
<li><a id="sec-4-2-2-4-2" name="sec-4-2-2-4-2"></a>the application state is all stored in one single tree structure. In other words, everything there is to know<br  /><div class="outline-text-6" id="text-4-2-2-4-2">
<p>
about your application's state is stored in one data structure formed out
of maps and arrays.
</p>
</div>
</li></ol>
</li></ol>
</div>
</div>

<div id="outline-container-sec-4-3" class="outline-3">
<h3 id="sec-4-3"><span class="section-number-3">4.3</span> Project Setup</h3>
<div class="outline-text-3" id="text-4-3">
</div><div id="outline-container-sec-4-3-1" class="outline-4">
<h4 id="sec-4-3-1"><span class="section-number-4">4.3.1</span> <span class="done DONE">DONE</span> This results in a directory with the single file "package.json" in it.</h4>
<div class="outline-text-4" id="text-4-3-1">
<div class="org-src-container">

<pre class="src src-sh">npm init -y
</pre>
</div>
<p>
<b>*</b> DONE Install ES6, Mocha, Cha 
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save-dev babel-core babel-cli babel-preset-es2015
npm install --save-dev mocha chai
</pre>
</div>
</div>
</div>
<div id="outline-container-sec-4-3-2" class="outline-4">
<h4 id="sec-4-3-2"><span class="section-number-4">4.3.2</span> <span class="done DONE">DONE</span> tests with mocha command</h4>
<div class="outline-text-4" id="text-4-3-2">
<div class="org-src-container">

<pre class="src src-sh">mkdir test
./node_modules/mocha/bin/mocha --compilers js:babel-core/register --recursive
</pre>
</div>
</div>
</div>
<div id="outline-container-sec-4-3-3" class="outline-4">
<h4 id="sec-4-3-3"><span class="section-number-4">4.3.3</span> <span class="done DONE">DONE</span> Place the command in package.json</h4>
<div class="outline-text-4" id="text-4-3-3">
<p>
package.json
"scripts": {
  "test": "mocha &#x2013;compilers js:babel-core/register &#x2013;recursive"
},
</p>
</div>
</div>
<div id="outline-container-sec-4-3-4" class="outline-4">
<h4 id="sec-4-3-4"><span class="section-number-4">4.3.4</span> <span class="done DONE">DONE</span> Another thing we need to do is enable Babel's ES6/ES2015 language support. It's</h4>
<div class="outline-text-4" id="text-4-3-4">
<p>
done by activating the babel-preset-es2015 package that we already installed.
We just need to add a "babel" section to package.json:
</p>

<p>
package.json
"babel": {
  "presets": ["es2015"]
}
</p>
</div>
</div>
<div id="outline-container-sec-4-3-5" class="outline-4">
<h4 id="sec-4-3-5"><span class="section-number-4">4.3.5</span> <span class="done DONE">DONE</span> test npm</h4>
<div class="outline-text-4" id="text-4-3-5">
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</div>

<div id="outline-container-sec-4-3-6" class="outline-4">
<h4 id="sec-4-3-6"><span class="section-number-4">4.3.6</span> <span class="done DONE">DONE</span> Add immutability</h4>
<div class="outline-text-4" id="text-4-3-6">
<p>
One of the first libraries we're going to be using is Facebook's Immutable,
which provides a number of data structures for us to use. We're going to start
discussing Immutable in the next section, but for now let's just add it to the
project, along with the chai-immutable library that extends Chai to add support
for comparing Immutable data structures:
</p>

<div class="org-src-container">

<pre class="src src-sh">npm install --save immutable
npm install --save-dev chai-immutable
</pre>
</div>
</div>
</div>
<div id="outline-container-sec-4-3-7" class="outline-4">
<h4 id="sec-4-3-7"><span class="section-number-4">4.3.7</span> We need to let plug in chai-immutable before any tests are run.</h4>
<div class="outline-text-4" id="text-4-3-7">
</div><ol class="org-ol"><li><a id="sec-4-3-7-1" name="sec-4-3-7-1"></a><span class="done DONE">DONE</span> Add test/test<sub>helper</sub>.js<br  /><div class="outline-text-5" id="text-4-3-7-1">
<div class="org-src-container">

<pre class="src src-js">import chai from 'chai';
import chaiImmutable from 'chai-immutable';

chai.use(chaiImmutable);
</pre>
</div>
</div>
</li>
<li><a id="sec-4-3-7-2" name="sec-4-3-7-2"></a>Modify package.json<br  /><div class="outline-text-5" id="text-4-3-7-2">
<p>
"scripts": {
  "test": "mocha &#x2013;compilers js:babel-core/register &#x2013;require ./test/test<sub>helper</sub>.js  &#x2013;recursive",
  "test:watch": "npm run test &#x2013; &#x2013;watch"
},
</p>
</div>
</li></ol>
</div>
</div>

<div id="outline-container-sec-4-4" class="outline-3">
<h3 id="sec-4-4"><span class="section-number-3">4.4</span> Getting Comfortable With Immutable&#xa0;&#xa0;&#xa0;<span class="tag"><span class="IMMUTABLE">IMMUTABLE</span></span></h3>
<div class="outline-text-3" id="text-4-4">
<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
<caption class="t-above"><span class="table-number">Table 2:</span> Clock summary at <span class="timestamp-wrapper"><span class="timestamp">[2015-11-24 মঙ্গল 21:34]</span></span></caption>

<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="right" />

<col  class="left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">Headline</th>
<th scope="col" class="left">Time</th>
<th scope="col" class="right">&#xa0;</th>
<th scope="col" class="left">&#xa0;</th>
</tr>
</thead>
<tbody>
<tr>
<td class="left"><b>Total time</b></td>
<td class="left"><b>2:27</b></td>
<td class="right">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>
</tbody>
<tbody>
<tr>
<td class="left">&emsp; Getting Comfortable With Immutable</td>
<td class="left">&#xa0;</td>
<td class="right">2:27</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&emsp;&emsp; Immutable data structures are the&#x2026;</td>
<td class="left">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="left">1:00</td>
</tr>
</tbody>
</table>

<p>
The second important point about the Redux architecture is that the state is
not just a tree, but it is in fact an immutable tree.
</p>
</div>
<div id="outline-container-sec-4-4-1" class="outline-4">
<h4 id="sec-4-4-1"><span class="section-number-4">4.4.1</span> The state is not just a tree, but it is in fact an immutable tree.</h4>
<div class="outline-text-4" id="text-4-4-1">
<p>
Looking at the trees in the previous section, it might at first seem like a
reasonable idea to have code that changes the state of the application by just
making updates in the tree: Replacing things in maps, removing things from
arrays, etc. However, this is not how things are done in Redux.
</p>
</div>
</div>
<div id="outline-container-sec-4-4-2" class="outline-4">
<h4 id="sec-4-4-2"><span class="section-number-4">4.4.2</span> the next state is another state tree that reflects the current changes</h4>
<div class="outline-text-4" id="text-4-4-2">
<p>
A Redux application's state tree is an immutable data structure. That means
that once you have a state tree, it will never change as long as it exists. It
will keep holding the same state forever. How you then go to the next state is
by producing another state tree that reflects the changes you wanted to make.
</p>
</div>
</div>
<div id="outline-container-sec-4-4-3" class="outline-4">
<h4 id="sec-4-4-3"><span class="section-number-4">4.4.3</span> Two successive states of the application are stored in two separate and independent trees.</h4>
<div class="outline-text-4" id="text-4-4-3">
<p>
This means any two successive states of the application are stored in two
separate and independent trees. How you get from one to the next is by applying
a function that takes the current state and returns a new state.
</p>
</div>
</div>
<div id="outline-container-sec-4-4-4" class="outline-4">
<h4 id="sec-4-4-4"><span class="section-number-4">4.4.4</span> How you get from one to the next is by applying a function that takes the current state and returns a new state.</h4>
</div>
<div id="outline-container-sec-4-4-5" class="outline-4">
<h4 id="sec-4-4-5"><span class="section-number-4">4.4.5</span> Immutability Helpful for debuging</h4>
<div class="outline-text-4" id="text-4-4-5">
</div><ol class="org-ol"><li><a id="sec-4-4-5-1" name="sec-4-4-5-1"></a>Can hold on to the history of your application<br  /></li>
<li><a id="sec-4-4-5-2" name="sec-4-4-5-2"></a>You can then do things like undo/redo for "free"<br  /></li>
<li><a id="sec-4-4-5-3" name="sec-4-4-5-3"></a>serialize the history<br  /><div class="outline-text-5" id="text-4-4-5-3">
<p>
just setthe current application state to the previous or next tree in the history. 
You can also serialize the history and save it for later, or send it to some
storage so that you can replay it later, which can be hugely helpful when
debugging.
</p>
</div>
</li></ol>
</div>
<div id="outline-container-sec-4-4-6" class="outline-4">
<h4 id="sec-4-4-6"><span class="section-number-4">4.4.6</span> Data in, data out , pure function</h4>
<div class="outline-text-4" id="text-4-4-6">
<p>
However, I'd say that even beyond these extra features, the most important
thing about immutable data is how it simplifies your code. You get to program
with pure functions: 
</p>
</div>
<ol class="org-ol"><li><a id="sec-4-4-6-1" name="sec-4-4-6-1"></a>pure functions:<br  /><div class="outline-text-5" id="text-4-4-6-1">
<p>
Functions that take data and return data and do nothing
else. These are functions that you can trust to behave predictably. You can
call them as many times as you like and their behavior won't change. Give them
the same arguments, and they'll return the same results. They're not going to
change the state of the world. Testing becomes trivial, as you don't need to
set up stubs or other fakes to "prepare the universe" before you call
something. It's just data in, data out.
</p>
</div>
</li></ol>
</div>
<div id="outline-container-sec-4-4-7" class="outline-4">
<h4 id="sec-4-4-7"><span class="section-number-4">4.4.7</span> Immutable data structures are the material we'll build our application's state</h4>
<div class="outline-text-4" id="text-4-4-7">
<p>
Immutable data structures are the material we'll build our application's state
from, so let's spend some time getting comfortable with it by writing some unit
tests that illustrate how it all works.
</p>
</div>
</div>
<div id="outline-container-sec-4-4-8" class="outline-4">
<h4 id="sec-4-4-8"><span class="section-number-4">4.4.8</span> Unit Testing Immutable Counter</h4>
<div class="outline-text-4" id="text-4-4-8">
<p>
If you're already comfortable with immutable data and the Immutable library,
feel free to skip to the next section. 
</p>
</div>
<ol class="org-ol"><li><a id="sec-4-4-8-1" name="sec-4-4-8-1"></a>To get acquainted with the idea of immutability<br  /><div class="outline-text-5" id="text-4-4-8-1">
<p>
it may be helpful to first talk about the simplest possible data structure: What if you had a "counter"
application whose state was nothing but a single number? The state would go
from 0 to 1 to 2 to 3, etc.
</p>
</div>
</li>
<li><a id="sec-4-4-8-2" name="sec-4-4-8-2"></a>We are already used to thinking of numbers as immutable data.<br  /><div class="outline-text-5" id="text-4-4-8-2">
<p>
When the counter increments, we don't mutate a number. It would in fact be 
impossible as there are no "setters" on numbers. You can't say 42.setValue(43).
</p>
</div>
</li>
<li><a id="sec-4-4-8-3" name="sec-4-4-8-3"></a>What happens instead is we get another number<br  /><div class="outline-text-5" id="text-4-4-8-3">
<p>
Which is the result of adding 1 to the previous number. 
That we can do with a pure function. Its argument is the current state and 
its return value will be used as the next state. When it is called, 
it does not change the current state. Here is such a function and a
unit test for it:
</p>

<div class="org-src-container">

<pre class="src src-js">import {expect} from 'chai'
describe('a number', () =&gt; {
  function increment(currentState) {
    return currentState + 1;
  }
  it('is immutable', () =&gt; {
    let state = 42;
    let nextState = increment(state);
    expect(nextState).to.equal(43);
    expect(state).to.equal(42);
  });
});
</pre>
</div>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-4-4-8-4" name="sec-4-4-8-4"></a>The fact that state doesn't change when increment is called should be obvious.<br  /><div class="outline-text-5" id="text-4-4-8-4">
<p>
How could it? Numbers are immutable!
</p>
</div>
</li>
<li><a id="sec-4-4-8-5" name="sec-4-4-8-5"></a>You may have noticed that this test really has nothing to do with our<br  /><div class="outline-text-5" id="text-4-4-8-5">
<p>
application - we don't even have any application code yet! 
</p>
</div>
</li>
<li><a id="sec-4-4-8-6" name="sec-4-4-8-6"></a>The test is just a learning tool for us.<br  /><div class="outline-text-5" id="text-4-4-8-6">
<p>
I often find it useful to explore a new API or technique by writing unit tests 
that exercise the relevant ideas, which is what we're doing here. Kent Beck calls 
these kinds of tests "Learning Tests" in his original TDD book. 
</p>

<p>
What we're going to do next is extend this same idea of immutability to all
kinds of data structures, not just numbers.
</p>
</div>
</li>

<li><a id="sec-4-4-8-7" name="sec-4-4-8-7"></a>Immutable's Lists<br  /><div class="outline-text-5" id="text-4-4-8-7">
<p>
     we can, for example, have an application whose state is
     a list of movies. An operation that adds a movie produces a new list that is
     the old list and the new movie combined. Crucially, the old state remains
     unchanged after the operation:
Head:     dad130b master immutable list tested
</p>
<div class="org-src-container">

<pre class="src src-js">imporot {expect} from 'chai';
import {List} from 'immutable';

describe('immutability', () =&gt; {
  describe('a number', () =&gt; {
    function increment(currentState) {
      return currentState + 1;
    }
    it('is immutable', () =&gt; {
      let state = 42;
      let nextState = increment(state);
      expect(nextState).to.equal(43);
      expect(state).to.equal(42);
    });
  });

  describe('A List', () =&gt; {
    function addMovie(currentState, movie){
      return currentState.push(movie);
    }

    it('is immutable', () =&gt; {
      let state = List.of('Trainspotting', '28 Days Later');
      let nextState = addMovie(state, 'Sunshine');

      expect(nextState).to.equal(List.of(
	'Trainspotting',
	'28 Days Later',
	'Sunshine'
      ));
      expect(state).to.equal(List.of(
	'Trainspotting',
	'28 Days Later'
      ));

    });
  });
});
</pre>
</div>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
<p>
&gt; voting-server@1.0.0  test  /usr/local/src/jstutorials/voting-server
&gt; mocha &#x2013;compilers  js:babel-core/register &#x2013;require ./test/test<sub>helper</sub>.js &#x2013;recursive 
</p>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />
</colgroup>
<tbody>
<tr>
<td class="left">immutability</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">a</td>
<td class="left">number</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
</tr>

<tr>
<td class="left">A</td>
<td class="left">List</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">2</td>
<td class="left">passing</td>
<td class="left">(28ms)</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>
</tbody>
</table>

<p>
The old state would not have remained unchanged if we'd pushed into a regular
array! Since we're using an Immutable List instead, we have the same semantics
as we had with the number example.
</p>

<p>
The idea extends to full state trees as well. A state tree is just a nested
data structure of Lists, Maps, and possibly other kinds of collections.
Applying an operation to it involves producing a new state tree, leaving the
previous one untouched. If the state tree is a Map with a key 'movies' that
contains a List of movies, 
</p>
</div>
</li>
<li><a id="sec-4-4-8-8" name="sec-4-4-8-8"></a>adding a movie means we need to create a new Map where the movies key points to a new List<br  /><div class="outline-text-5" id="text-4-4-8-8">
<div class="org-src-container">

<pre class="src src-js">imporot {expect} from 'chai';
import {List, Map} from 'immutable';

describe('immutability', () =&gt; {
  describe('a number', () =&gt; {
    function increment(currentState) {
      return currentState + 1;
    }
    it('is immutable', () =&gt; {
      let state = 42;
      let nextState = increment(state);
      expect(nextState).to.equal(43);
      expect(state).to.equal(42);
    });
  });

  describe('A List', () =&gt; {
    function addMovie(currentState, movie){
      return currentState.push(movie);
    }

    it('is immutable', () =&gt; {
      let state = List.of('Trainspotting', '28 Days Later');
      let nextState = addMovie(state, 'Sunshine');

      expect(nextState).to.equal(List.of(
	'Trainspotting',
	'28 Days Later',
	'Sunshine'
      ));
      expect(state).to.equal(List.of(
	'Trainspotting',
	'28 Days Later'
      ));

    });
  });

  describe('a tree' , () =&gt; {
    function addMovie(currentState, movie ) {
      return currentState.set(
	'movies',
	currentState.get('movies').push(movie)
      );
    }

    it('is immatable', () =&gt; {
      let state = Map({
	movies: List.of('Trainspotting', '28 Days Later')
      });
      let nextState = addMovie(state, 'Sunshine');

      expect(nextState).to.equal(Map({
	movies: List.of(
	  'Trainspotting',
	  '28 Days Later',
	  'Sunshine'
	)
      }));
    });
  });
});
</pre>
</div>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
<p>
Head:     19afc7b master new Map where the movies key points to a new List
</p>

<p>
&gt; voting-server@1.0.0 test /usr/local/src/jstutorials/voting-server
&gt; mocha &#x2013;compilers  js:babel-core/register  &#x2013;require ./test/test<sub>helper</sub>.js &#x2013;recursive 
</p>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />
</colgroup>
<tbody>
<tr>
<td class="left">immutability</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">a</td>
<td class="left">number</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
</tr>

<tr>
<td class="left">A</td>
<td class="left">List</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
</tr>

<tr>
<td class="left">a</td>
<td class="left">tree</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immatable</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">3</td>
<td class="left">passing</td>
<td class="left">(30ms)</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>
</tbody>
</table>

<p>
This is exactly the same behavior as before, just extended to show that it
works with nested data structures too. The same idea holds to all shapes and
sizes of data.
</p>

<p>
For operations on nested data structures such as this one, Immutable provides
several helper functions that make it easier to "reach into" the nested data to
produce an updated value. We can use one called update in this case to make the
code more concise:
</p>
<div class="org-src-container">

<pre class="src src-patch">-    function addMovie(currentState, movie ) {
-      return currentState.set(
-       'movies',
-       currentState.get('movies').push(movie)
-      );
+    function addMovie(currentState, movie) {
+      return currentState.update('movies', movies =&gt; movies.push(movie));
</pre>
</div>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
<p>
Head:     b23ffbc master helper functions that make it easier to reach into
</p>
<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />
</colgroup>
<tbody>
<tr>
<td class="left">&gt;  voting-server@1.0.0  test  /usr/local/src/jstutorials/voting-server</td>
</tr>

<tr>
<td class="left">&gt;  mocha  &#x2013;compilers  js:babel-core/register  &#x2013;require  ./test/test<sub>helper</sub>.js  &#x2013;recursive</td>
</tr>
</tbody>
</table>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />
</colgroup>
<tbody>
<tr>
<td class="left">immutability</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">a</td>
<td class="left">number</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
</tr>

<tr>
<td class="left">A</td>
<td class="left">List</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
</tr>

<tr>
<td class="left">a</td>
<td class="left">tree</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immatable</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">3</td>
<td class="left">passing</td>
<td class="left">(33ms)</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>
</tbody>
</table>
</div>
</li>
<li><a id="sec-4-4-8-9" name="sec-4-4-8-9"></a>Reasons for using IMMUTABLE library<br  /><ol class="org-ol"><li><a id="sec-4-4-8-9-1" name="sec-4-4-8-9-1"></a>Immutable's data structures are designed from the ground up to be used<br  /><div class="outline-text-6" id="text-4-4-8-9-1">
<p>
immutably and thus provide an API that makes immutable operations convenient. 
</p>
</div>
</li>
<li><a id="sec-4-4-8-9-2" name="sec-4-4-8-9-2"></a>I'm partial to Rich Hickey's view that there is no such as thing as<br  /><div class="outline-text-6" id="text-4-4-8-9-2">
<p>
immutability by convention. If you use data structures that allow mutations,
sooner or later you or someone else is bound to make a mistake and mutate
them. This is especially true when you're just getting started. Things like
Object.freeze() may help with this. 
</p>
</div>
</li>
<li><a id="sec-4-4-8-9-3" name="sec-4-4-8-9-3"></a>Immutable's data structures are persistent, meaning that they are internally<br  /><div class="outline-text-6" id="text-4-4-8-9-3">
<p>
structured so that producing new versions is efficient both in terms of time
and memory, even for large state trees. Using plain objects and arrays may
result in excessive amounts of copying, which hurts performance. 
</p>
</div>
</li></ol>
</li></ol>
</div>
</div>

<div id="outline-container-sec-4-5" class="outline-3">
<h3 id="sec-4-5"><span class="section-number-3">4.5</span> Writing The Application Logic With Pure Functions</h3>
<div class="outline-text-3" id="text-4-5">
<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
<caption class="t-above"><span class="table-number">Table 3:</span> Clock summary at <span class="timestamp-wrapper"><span class="timestamp">[2015-11-24 মঙ্গল 21:36]</span></span></caption>

<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="right" />

<col  class="right" />

<col  class="right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">Headline</th>
<th scope="col" class="left">Time</th>
<th scope="col" class="right">&#xa0;</th>
<th scope="col" class="right">&#xa0;</th>
<th scope="col" class="right">&#xa0;</th>
</tr>
</thead>
<tbody>
<tr>
<td class="left"><b>Total time</b></td>
<td class="left"><b>5:09</b></td>
<td class="right">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">&#xa0;</td>
</tr>
</tbody>
<tbody>
<tr>
<td class="left">&emsp; Writing The Application Logic With&#x2026;</td>
<td class="left">&#xa0;</td>
<td class="right">5:09</td>
<td class="right">&#xa0;</td>
<td class="right">&#xa0;</td>
</tr>

<tr>
<td class="left">&emsp;&emsp; Loading Entries</td>
<td class="left">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">1:03</td>
<td class="right">&#xa0;</td>
</tr>

<tr>
<td class="left">&emsp;&emsp;&emsp; Test Case for Entries and Source Code</td>
<td class="left">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">1:03</td>
</tr>

<tr>
<td class="left">&emsp;&emsp; Starting The Vote Second state</td>
<td class="left">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">0:30</td>
<td class="right">&#xa0;</td>
</tr>

<tr>
<td class="left">&emsp;&emsp; Voting</td>
<td class="left">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">1:12</td>
<td class="right">&#xa0;</td>
</tr>

<tr>
<td class="left">&emsp;&emsp; Moving to The Next Pair</td>
<td class="left">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">0:50</td>
<td class="right">&#xa0;</td>
</tr>

<tr>
<td class="left">&emsp;&emsp; Ending The Vote</td>
<td class="left">&#xa0;</td>
<td class="right">&#xa0;</td>
<td class="right">0:33</td>
<td class="right">&#xa0;</td>
</tr>
</tbody>
</table>

<p>
Armed with an understanding of immutable state trees and the functions that
operate on them, we can turn our attention to the logic of our voting
application itself. The core of the app will be formed from the pieces that we
have been discussing: A tree structure and a set of functions that produce new
versions of that tree structure.
</p>
</div>

<div id="outline-container-sec-4-5-1" class="outline-4">
<h4 id="sec-4-5-1"><span class="section-number-4">4.5.1</span> Loading Entries</h4>
<div class="outline-text-4" id="text-4-5-1">
</div><ol class="org-ol"><li><a id="sec-4-5-1-1" name="sec-4-5-1-1"></a>Test Case for Entries and Source Code<br  /><div class="outline-text-5" id="text-4-5-1-1">
<p>
the application allows "loading in" a collection of entries that will be voted on. 
We could have a function called setEntries that takes a previous state and 
a collection of entries and produces a state where the entries are included. 
</p>
<div class="org-src-container">

<pre class="src src-js">import {List, Map} from 'immutable';
import {expect} from 'chai';
import {setEntries} from '../src/core';

describe('application logic', () =&gt; {
  describe('setEntries', () =&gt; {
    it('adds the entries to the state', ()=&gt; {
      const state = Map();
      const entries = List.of('Trainspotting', '28 Days Later');
      const nextState = setEntries(state, entries);
      expect(nextState).to.equal(Map({
	entries: List.of('Trainspotting', '28 Days Later')
      }));
    });
  });
});
</pre>
</div>

<div class="org-src-container">

<pre class="src src-js">export function setEntries(state,entries){
  return state.set('entries', entries);
}
</pre>
</div>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
<ol class="org-ol"><li><a id="sec-4-5-1-1-1" name="sec-4-5-1-1-1"></a>Array to Immutable List<br  /><div class="outline-text-6" id="text-4-5-1-1-1">
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>

<div class="org-src-container">

<pre class="src src-patch">@@ -1,4 +1,4 @@
-
+import {List} from 'immutable';
 export function setEntries(state,entries){
-  return state.set('entries', entries);
+  return state.set('entries', List(entries));
 }
</pre>
</div>

<div class="org-src-container">

<pre class="src src-test/core_spec.js">@@ -6,9 +6,9 @@ import {setEntries} from '../src/core';
 describe('application logic', () =&gt; {
   describe('setEntries', () =&gt; {
     it('adds the entries to the state', ()=&gt; {
       const state = Map();
-      const entries = List.of('Trainspotting', '28 Days Later');
+      const entries = ['Trainspotting', '28 Days Later'];
       const nextState = setEntries(state, entries);
       expect(nextState).to.equal(Map({
	 entries: List.of('Trainspotting', '28 Days Later')
       }));
</pre>
</div>
</div>
</li></ol>
</li></ol>
</div>

<div id="outline-container-sec-4-5-2" class="outline-4">
<h4 id="sec-4-5-2"><span class="section-number-4">4.5.2</span> Starting The Vote Second state</h4>
<div class="outline-text-4" id="text-4-5-2">
<p>
    We can begin the voting by calling a function called next on a state that
already has entries set. That means, going from the first to the second of the
state trees we designed.
</p>

<p>
The function takes no additional arguments. It should create a vote Map on the
state, where the two first entries are included under the key pair. The entries
under vote should no longer be in the entries List:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
<ol class="org-ol"><li><a id="sec-4-5-2-1" name="sec-4-5-2-1"></a>Head:     9e91d63 master prepare 2 canditate for voting.<br  /><div class="outline-text-5" id="text-4-5-2-1">
<pre class="example">
modified   src/core.js
@@ -1,4 +1,12 @@
-import {List} from 'immutable';
+import {List, Map} from 'immutable';
 export function setEntries(state,entries){
   return state.set('entries', List(entries));
 }
+
+export function next(state){
+  const entries = state.get('entries');
+  return state.merge({
+    vote: Map({pair: entries.take(2)}),
+    entries: entries.skip(2)
+  });
+}
modified   test/core_spec.js
@@ -1,7 +1,7 @@
 
 import {List, Map} from 'immutable';
 import {expect} from 'chai';
-import {setEntries} from '../src/core';
+import {setEntries, next} from '../src/core';
 
 describe('application logic', () =&gt; {
   describe('setEntries', () =&gt; {
@@ -14,4 +14,18 @@ describe('application logic', () =&gt; {
       }));
     });
   });
+  describe('next',() =&gt; {
+    it('takes the next two entries under vote', () =&gt; {
+      const state = Map({
+	entries: List.of('Trainspotting', '28 Days Later', 'Sunshine')
+      });
+      const nextState = next(state);
+      expect(nextState).to.equal(Map({
+	vote: Map({
+	  pair: List.of('Trainspotting', '28 Days Later')
+	}),
+	entries: List.of('Sunshine')
+      }));
+    });
+  });
 });
</pre>
</div>
</li></ol>
</div>
<div id="outline-container-sec-4-5-3" class="outline-4">
<h4 id="sec-4-5-3"><span class="section-number-4">4.5.3</span> Voting</h4>
<div class="outline-text-4" id="text-4-5-3">

<p>
When a vote is ongoing, it should be possible for people to vote on entries.
When a new vote is cast for an entry, a "tally" for it should appear in the
vote. If there already is a tally for the entry, it should be incremented:
</p>

<p>
tag: 40d673bc12d521250ff4418e09105ac270f92c4d
Parent:     d17fe11 diff code insertion
</p>

<pre class="example">
modified   src/core.js
@@ -10,3 +10,11 @@ export function next(state){
     entries: entries.skip(2)
   });
 }
+
+export function vote(state, entry){
+  return state.updateIn(
+    ['vote', 'tally', entry ],
+    0,
+    tally =&gt; tally + 1
+  );
+}
modified   test/core_spec.js
@@ -1,7 +1,7 @@
 
 import {List, Map} from 'immutable';
 import {expect} from 'chai';
-import {setEntries, next} from '../src/core';
+import {setEntries, next, vote} from '../src/core';
 
 describe('application logic', () =&gt; {
   describe('setEntries', () =&gt; {
@@ -28,4 +28,47 @@ describe('application logic', () =&gt; {
       }));
     });
   });
+  describe('vote', () =&gt; {
+    it('creates a tally for the voted entry', () =&gt; {
+      const state = Map({
+	vote: Map({
+	  pair: List.of('Trainspotting', '28 Days Later')
+	}),
+	entries: List()
+      });
+      const nextState = vote(state, 'Trainspotting' );
+      expect(nextState).to.equal(Map({
+	vote: Map({
+	  pair: List.of('Trainspotting', '28 Days Later'),
+	  tally: Map({
+	    'Trainspotting': 1
+	  })
+	}),
+	entries: List()
+      }));
+    });
+    it('adds to existing tally for the voted entry', () =&gt; {
+      const state = Map({
+	vote: Map({
+	  pair: List.of('Trainspotting', '28 Days Later'),
+	  tally: Map({
+	    'Trainspotting': 3,
+	    '28 Days Later': 2
+	  }),
+	}),
+	entries: List()
+      });
+      const nextState = vote(state, 'Trainspotting');
+      expect(nextState).to.equal(Map({
+	vote: Map({
+	  pair: List.of('Trainspotting', '28 Days Later'),
+	  tally: Map({
+	    'Trainspotting': 4,
+	    '28 Days Later': 2
+	  }),
+	}),
+	entries: List()
+      }));
+    });
+  });
 });
</pre>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
<p>
Using updateIn makes this pleasingly succinct. What the code expresses is
"reach into the nested data structure path ['vote', 'tally', 'Trainspotting'],
and apply this function there. If there are keys missing along the path, create
new Maps in their place. If the value at the end is missing, initialize it with
0".
</p>

<p>
It packs a lot of punch, but this is exactly the kind of code that makes
working with immutable data structures pleasant, so it's worth spending a bit
of time getting comfortable with it.
</p>

<p>
You could build all these nested Maps and Lists more concisely using the fromJS
function from Immutable. 
</p>
</div>
</div>

<div id="outline-container-sec-4-5-4" class="outline-4">
<h4 id="sec-4-5-4"><span class="section-number-4">4.5.4</span> Moving to The Next Pair</h4>
<div class="outline-text-4" id="text-4-5-4">
<p>
Once the vote for a given pair is over, we should proceed to the next one. The
winning entry from the current vote should be kept, and added back to the end
of the entries, so that it will later be paired with something else. The losing
entry is thrown away. If there is a tie, both entries are kept.
Head:     c5b0f2d master send winner[s] back to entries
tag: c5b0f2dff360b81b73e5d422b211f0d8bae60c13
</p>
<pre class="example">
 @@ -3,8 +3,19 @@ export function setEntries(state,entries){
   return state.set('entries', List(entries));
 }
 
+function getWinners(vote) {
+  if (!vote) return [];
+  const [a,b] = vote.get('pair');
+  const aVotes = vote.getIn(['tally', a ] , 0);
+  const bVotes = vote.getIn(['tally', b ] , 0);
+  if ( aVotes &gt; bVotes )    return [a];
+  if ( aVotes &lt; bVotes )    return [b];
+  return [a, b];
+}
+
 export function next(state){
-  const entries = state.get('entries');
+  const entries = state.get('entries')
+                       .concat(getWinners(state.get('vote')));
   return state.merge({
     vote: Map({pair: entries.take(2)}),
     entries: entries.skip(2)
modified   test/core_spec.js
@@ -27,7 +27,47 @@ describe('application logic', () =&gt; {
 	entries: List.of('Sunshine')
       }));
     });
+    it('puts winner of current vote back to entries', () =&gt; {
+      const state = Map({
+	vote: Map({
+	  pair: List.of('Trainspotting', '28 Days Later'),
+          tally: Map({
+            'Trainspotting': 4,
+            '28 Days Later': 2
+          })
+	}),
+	entries: List.of('Sunshine', 'Millions', '127 Hours')
+      });
+      const nextState = next(state);
+      expect(nextState).to.equal(Map({
+	vote: Map({
+          pair: List.of('Sunshine', 'Millions')
+	}),
+	entries: List.of('127 Hours', 'Trainspotting')
+      }));
+    });
+
+    it('puts both from tied vote back to entries', () =&gt; {
+      const state = Map({
+	vote: Map({
+          pair: List.of('Trainspotting', '28 Days Later'),
+          tally: Map({
+            'Trainspotting': 3,
+            '28 Days Later': 3
+          })
+	}),
+	entries: List.of('Sunshine', 'Millions', '127 Hours')
+      });
+      const nextState = next(state);
+      expect(nextState).to.equal(Map({
+	vote: Map({
+          pair: List.of('Sunshine', 'Millions')
+	}),
+	entries: List.of('127 Hours', 'Trainspotting', '28 Days Later')
+      }));
+    });
   });
+  
   describe('vote', () =&gt; {
     it('creates a tally for the voted entry', () =&gt; {
       const state = Map({
</pre>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</div>

<div id="outline-container-sec-4-5-5" class="outline-4">
<h4 id="sec-4-5-5"><span class="section-number-4">4.5.5</span> Ending The Vote</h4>
<div class="outline-text-4" id="text-4-5-5">
<p>
At some point there's just going to be one entry left when a vote ends. At that
point we have a winning entry. What we should do is, instead of trying to form
a next vote, just set the winner in the state explicitly. The vote is over.
</p>

<p>
    In the implementation of next we should have a special case for the situation
    where the entries has a size of 1 after we've processed the current vote:
Head:     c37c165 master get winner ending&#x2026;
tag: c37c165998a38553e195d7b644491c23f683b731
</p>
<pre class="example">
modified   src/core.js
@@ -15,7 +15,11 @@ function getWinners(vote) {
 
 export function next(state){
   const entries = state.get('entries')
-                       .concat(getWinners(state.get('vote')));
+    .concat(getWinners(state.get('vote')));
+  if (entries.size === 1 )
+    return state.remove('vote')
+                .remove('entries')
+                .set('winner', entries.first()); 
   return state.merge({
     vote: Map({pair: entries.take(2)}),
     entries: entries.skip(2)
modified   test/core_spec.js
@@ -66,6 +66,22 @@ describe('application logic', () =&gt; {
 	entries: List.of('127 Hours', 'Trainspotting', '28 Days Later')
       }));
     });
+    it('marks winner when just one entry left', () =&gt; {
+      const state = Map({
+	vote: Map({
+          pair: List.of('Trainspotting', '28 Days Later'),
+          tally: Map({
+            'Trainspotting': 4,
+            '28 Days Later': 2
+          })
+	}),
+	entries: List()
+      });
+      const nextState = next(state);
+      expect(nextState).to.equal(Map({
+	winner: 'Trainspotting'
+      }));
+    });
   });
   
   describe('vote', () =&gt; {
</pre>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>

<p>
We could have just returned Map({winner: entries.first()}) here. But instead we
still take the old state as the starting point and explicitly remove 'vote' and
'entries' keys from it. The reason for this is future-proofing: At some point
we might have some unrelated data in the state, and it should pass through this
function unchanged. It is generally a good idea in these state transformation
functions to always morph the old state into the new one instead of building
the new state completely from scratch.
</p>

<p>
Here we have an acceptable version of the core logic of our app, expressed as a
few functions. We also have unit tests for them, and writing those tests has
been relatively easy: No setup, no mocks, no stubs. That's the beauty of pure
functions. We can just call them and inspect the return values.
</p>

<p>
Note that we haven't even installed Redux yet. We've been able to focus totally
on the logic of the app itself, without bringing the "framework" in. There's
something very pleasing about that.
</p>
</div>
</div>
</div>

<div id="outline-container-sec-4-6" class="outline-3">
<h3 id="sec-4-6"><span class="section-number-3">4.6</span> Introducing Actions and Reducers</h3>
<div class="outline-text-3" id="text-4-6">

<p>
We have the core functions of our app, but in Redux you don't actually call
those functions directly. There is a layer of indirection between the functions
and the outside world: Actions.
</p>

<p>
An action is a simple data structure that describes a change that should occur
in your app state. It's basically a description of a function call packaged
into a little object. By convention, every action has a type attribute that
describes which operation the action is for. Each action may also carry
additional attributes. Here are a few example actions that match the core
functions we have just written:
</p>

<p>
{type: 'SET<sub>ENTRIES'</sub>, entries: ['Trainspotting', '28 Days Later']}
</p>

<p>
{type: 'NEXT'}
</p>

<p>
{type: 'VOTE', entry: 'Trainspotting'}
</p>

<p>
If actions are expressed like this, we also need a way to turn them into the
actual core function calls. For example, given the VOTE action, the following
call should be made:
</p>

<p>
// This action
let voteAction = {type: 'VOTE', entry: 'Trainspotting'}
// should cause this to happen
return vote(state, voteAction.entry);
</p>

<p>
What we're going to write is a generic function that takes any kind of action -
along with the current state - and invokes the core function that matches the
action. This function is called a reducer:
</p>
<div class="org-src-container">

<pre class="src src-js">export default function reducer(state, action) {
// Figure out which function to call and call it
}
</pre>
</div>

<p>
We should test that the reducer can indeed handle each of our three actions:
</p>

<div class="org-src-container">

<pre class="src src-js">import {Map, fromJS} from 'immutable'
import {expect} from 'chai';
import reducer from '../src/reducer';

  it('handles SET_ENTRIES', () =&gt; {
    const initialState = Map();
    const action = { type: 'SET_ENTRIES', entries: ['Trainspotting'] };
    const nextState = reducer(initialState, action );
    expect(nextState).to.equal(fromJS({
      entries: ['Trainspotting']
    }));
  });

  it('handles NEXT', () =&gt; {
    const initialState = fromJS({
      entries: ['Trainspotting', '28 Days Later']
    });
    const action = {type: 'NEXT'};
    const nextState = reducer(initialState, action);

    expect(nextState).to.equal(fromJS({
      vote: {
	pair: ['Trainspotting', '28 Days Later'],
	tally: {Transformation: 1}
      },
      entries: []
    }));
  });

  it('handles VOTE', () =&gt; { 
    const initialState = fromJS({
      vote: {
	pair: ['Trainspotting', '28 Days Later']
      },
      entries: []
    });
    const action = {type: 'VOTE', entry: 'Trainspotting'};
    const nextState = reducer(initialState, action);

    expect(nextState).to.equal(fromJS({
      vote: {
	pair: ['Trainspotting', '28 Days Later'],
	tally: {Transformation: 1}
      },
      entries: []
    }));
  });
});
</pre>
</div>
<p>
Our reducer should delegate to one of the core functions based on the type of
the action. It also knows how to unpack the additional arguments of each
function from the action object:
</p>

<pre class="example">
import {setEntries, next, vote} from './core';

export default function reducer(state, action) {
  switch (action.type) {
    case 'SET_ENTRIES':
      return setEntries(state, action.entries);
    case 'NEXT':
      return next(state);
    case 'VOTE':
      return vote(state, action.entry)
  }
  return state;
}
</pre>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>

<p>
&gt; voting-server@1.0.0 test /usr/local/src/jstutorials/voting-server
&gt; mocha &#x2013;compilers  js:babel-core/register  &#x2013;require  ./test/test<sub>helper</sub>.js  &#x2013;recursive 
</p>

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />

<col  class="left" />
</colgroup>
<tbody>
<tr>
<td class="left">application</td>
<td class="left">logic</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">setEntries</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">adds</td>
<td class="left">the</td>
<td class="left">entries</td>
<td class="left">to</td>
<td class="left">the</td>
<td class="left">state</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">next</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">takes</td>
<td class="left">the</td>
<td class="left">next</td>
<td class="left">two</td>
<td class="left">entries</td>
<td class="left">under</td>
<td class="left">vote</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">puts</td>
<td class="left">winner</td>
<td class="left">of</td>
<td class="left">current</td>
<td class="left">vote</td>
<td class="left">back</td>
<td class="left">to</td>
<td class="left">entries</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">puts</td>
<td class="left">both</td>
<td class="left">from</td>
<td class="left">tied</td>
<td class="left">vote</td>
<td class="left">back</td>
<td class="left">to</td>
<td class="left">entries</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">marks</td>
<td class="left">winner</td>
<td class="left">when</td>
<td class="left">just</td>
<td class="left">one</td>
<td class="left">entry</td>
<td class="left">left</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">vote</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">creates</td>
<td class="left">a</td>
<td class="left">tally</td>
<td class="left">for</td>
<td class="left">the</td>
<td class="left">voted</td>
<td class="left">entry</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">adds</td>
<td class="left">to</td>
<td class="left">existing</td>
<td class="left">tally</td>
<td class="left">for</td>
<td class="left">the</td>
<td class="left">voted</td>
<td class="left">entry</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">immutability</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">a</td>
<td class="left">number</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">A</td>
<td class="left">List</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immutable</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">a</td>
<td class="left">tree</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">is</td>
<td class="left">immatable</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">Reducer</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">handles</td>
<td class="left">SET<sub>ENTRIES</sub></td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">handles</td>
<td class="left">NEXT</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">✓</td>
<td class="left">handles</td>
<td class="left">VOTE</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">13</td>
<td class="left">passing</td>
<td class="left">(98ms)</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>

<tr>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
<td class="left">&#xa0;</td>
</tr>
</tbody>
</table>

<p>
test/reducer<sub>spec</sub>.js
describe('reducer', () =&gt; {
</p>

<p>
// &#x2026;
</p>

<p>
it('has an initial state', () =&gt; {
  const action = {type: 'SET<sub>ENTRIES'</sub>, entries: ['Trainspotting']};
  const nextState = reducer(undefined, action);
  expect(nextState).to.equal(fromJS({
    entries: ['Trainspotting']
  }));
});
</p>

<p>
});
</p>

<p>
Since our application's logic is in core.js, it makes sense to introduce the
initial state there:
</p>

<p>
src/core.js
export const INITIAL<sub>STATE</sub> = Map();
</p>

<p>
In the reducer we'll import it and use it as the default value of the state
argument:
</p>

<p>
src/reducer.js
import {setEntries, next, vote, INITIAL<sub>STATE</sub>} from './core';
</p>

<p>
export default function reducer(state = INITIAL<sub>STATE</sub>, action) {
  switch (action.type) {
  case 'SET<sub>ENTRIES'</sub>:
    return setEntries(state, action.entries);
  case 'NEXT':
    return next(state);
  case 'VOTE':
    return vote(state, action.entry)
  }
  return state;
}
</p>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
<p>
This ability to batch and/or replay a collection of actions is a major benefit
of the action/reducer model of state transitions, when compared to calling the
core functions directly. For example, given that actions are just objects that
you can also serialize to JSON, you could easily send them over to a Web Worker
and run your reducer logic there. Or you can even send them over the network,
as we're going to do later!
</p>

<p>
Note that we are using plain objects as actions instead of Immutable data
structures. This is something Redux actually requires us to do. 
</p>
</div>
</div>

<div id="outline-container-sec-4-7" class="outline-3">
<h3 id="sec-4-7"><span class="section-number-3">4.7</span> A Taste of Reducer Composition</h3>
<div class="outline-text-3" id="text-4-7">
<p>
Our core functionality is currently defined so that each function takes the
whole state of the application and returns the whole, next state of the
application.
</p>

<p>
It is easy to see how keeping to this pattern may not be a good idea in large
applications. If each and every operation in the application needs to be aware
of the structure of the whole state, things can easily get brittle. If you
wanted to change the shape of the state, it would require a whole lot of
changes.
</p>

<p>
It is a much better idea to, whenever you can, make operations work on the
smallest piece (or subtree) of the state possible. What we're talking about is
modularization: Have the functionality that deals with a given piece of data
deal with only that part of the data, as if the rest didn't exist.
</p>

<p>
Our application is so tiny that we don't have a problem of this kind yet, but
we do already have one opportunity to improve on this: There is no reason for
the vote function to receive the whole app state, since it only works on the
'vote' part of it. That's the only thing it should know about. We can modify
the existing unit tests for vote to reflect this idea:
</p>

<p>
test/core<sub>spec</sub>.js
describe('vote', () =&gt; {
</p>

<p>
it('creates a tally for the voted entry', () =&gt; {
  const state = Map({
    pair: List.of('Trainspotting', '28 Days Later')
  });
  const nextState = vote(state, 'Trainspotting')
  expect(nextState).to.equal(Map({
    pair: List.of('Trainspotting', '28 Days Later'),
    tally: Map({
      'Trainspotting': 1
    })
  }));
});
</p>

<p>
it('adds to existing tally for the voted entry', () =&gt; {
  const state = Map({
    pair: List.of('Trainspotting', '28 Days Later'),
    tally: Map({
      'Trainspotting': 3,
      '28 Days Later': 2
    })
  });
  const nextState = vote(state, 'Trainspotting');
  expect(nextState).to.equal(Map({
    pair: List.of('Trainspotting', '28 Days Later'),
    tally: Map({
      'Trainspotting': 4,
      '28 Days Later': 2
    })
  }));
});
</p>

<p>
});
</p>

<p>
As we see, this also simplifies the test code, which is usually a good sign!
</p>

<p>
The vote implementation should now just take the vote part of the state, and
update its tally:
</p>

<p>
src/core.js
export function vote(voteState, entry) {
  return voteState.updateIn(
    ['tally', entry],
    0,
    tally =&gt; tally + 1
  );
}
</p>

<p>
Now it becomes the job of our reducer to pick apart the state so that it gives
only the relevant part to the vote function:
</p>

<p>
src/reducer.js
export default function reducer(state = INITIAL<sub>STATE</sub>, action) {
  switch (action.type) {
  case 'SET<sub>ENTRIES'</sub>:
    return setEntries(state, action.entries);
  case 'NEXT':
    return next(state);
  case 'VOTE':
    return state.update('vote',
                        voteState =&gt; vote(voteState, action.entry));
  }
  return state;
}
</p>

<p>
This is a small example of the kind of pattern that becomes much more important
the larger an application gets: The main reducer function only hands parts of
the state to lower-level reducer functions. We separate the job of finding the
right location in the state tree from applying the update to that location.
</p>

<p>
The Redux documentation for reducers goes into these patterns of reducer
composition in a lot more detail, and also describes some helper functions that
makes reducer composition easier in many cases.
</p>
</div>
</div>

<div id="outline-container-sec-4-8" class="outline-3">
<h3 id="sec-4-8"><span class="section-number-3">4.8</span> Introducing The Redux Store</h3>
<div class="outline-text-3" id="text-4-8">
<p>
Now that we have a reducer, we can start looking at how this all plugs into
Redux itself.
</p>

<p>
As we just saw, if you had a collection of all the actions that are ever going
to occur in your application, you could just call reduce. Out pops the final
state of your app. Of course, you usually don't have a collection of all those
actions. They will arrive spread out over time, as things happen in the world:
When users interact with the app, when data is received from networks, or when
timeouts trigger.
</p>

<p>
To deal with this reality, we can use a Redux Store. It is an object that, as
the name implies, stores the state of your application over time.
</p>

<p>
A Redux Store is initialized with a reducer function, such as the one we have
just implemented:
</p>

<p>
Now that we have a reducer, we can start looking at how this all plugs into
Redux itself.
</p>

<p>
As we just saw, if you had a collection of all the actions that are ever going
to occur in your application, you could just call reduce. Out pops the final
state of your app. Of course, you usually don't have a collection of all those
actions. They will arrive spread out over time, as things happen in the world:
When users interact with the app, when data is received from networks, or when
timeouts trigger.
</p>

<p>
To deal with this reality, we can use a Redux Store. It is an object that, as
the name implies, stores the state of your application over time.
</p>

<p>
A Redux Store is initialized with a reducer function, such as the one we have
just implemented:
</p>

<p>
import {createStore} from 'redux';
</p>

<p>
const store = createStore(reducer);
</p>

<p>
What you can then do is dispatch actions to that Store. The Store will
internally use your reducer to apply the actions to the current state, and
store the resulting, next state:
</p>

<p>
store.dispatch({type: 'NEXT'});
</p>

<p>
At any point in time, you can obtain the current state from inside the Store:
</p>

<p>
store.getState();
</p>

<p>
We're going to set up and export a Redux Store in a file called store.js. Let's
test it first. We should be able to make a store, read its initial state,
dispatch action, and witness the changed state:
import {createStore} from 'redux';
</p>

<p>
const store = createStore(reducer);
</p>

<p>
What you can then do is dispatch actions to that Store. The Store will
internally use your reducer to apply the actions to the current state, and
store the resulting, next state:
</p>

<p>
store.dispatch({type: 'NEXT'});
</p>

<p>
At any point in time, you can obtain the current state from inside the Store:
</p>

<p>
store.getState();
</p>

<p>
We're going to set up and export a Redux Store in a file called store.js. Let's
test it first. We should be able to make a store, read its initial state,
dispatch action, and witness the changed state:
</p>

<p>
test/store<sub>spec</sub>.js
import {Map, fromJS} from 'immutable';
import {expect} from 'chai';
</p>

<p>
import makeStore from '../src/store';
</p>

<p>
describe('store', () =&gt; {
</p>

<p>
it('is a Redux store configured with the correct reducer', () =&gt; {
  const store = makeStore();
  expect(store.getState()).to.equal(Map());
</p>

<p>
  store.dispatch({
    type: 'SET<sub>ENTRIES'</sub>,
    entries: ['Trainspotting', '28 Days Later']
  });
  expect(store.getState()).to.equal(fromJS({
    entries: ['Trainspotting', '28 Days Later']
  }));
});
</p>

<p>
});
</p>

<p>
Before we can create the Store, we need to add Redux into the project:
</p>

<div class="org-src-container">

<pre class="src src-sh">npm install --save redux
</pre>
</div>

<p>
Then we can create store.js, where we simply call createStore with our reducer:
</p>

<p>
src/store.js
import {createStore} from 'redux';
import reducer from './reducer';
</p>

<p>
export default function makeStore() {
  return createStore(reducer);
}
</p>

<p>
So, the Redux store ties things together into something we'll be able to use as
the central point of our application: It holds the current state, and over time
can receive actions that evolve the state from one version to the next, using
the core application logic we have written and exposed through the reducer.
Question: How many variables do you need in a Redux application?
Answer: One. The one inside the store. 
</p>

<p>
This notion may sound ludicrous at first - at least if you haven't done much
functional programming. How can you do anything useful with just one variable? 
</p>

<p>
But the fact is we don't need any more variables than that. The current state
tree is the only thing that varies over time in our core application. The rest
is all constants and immutable values. 
</p>

<p>
It is quite remarkable just how small the integration surface area between our
application code and Redux actually is. Because we have a generic reducer
function, that's the only thing we need to let Redux know about. The rest is
all in our own, non-framework-specific, highly portable and purely functional
code!
</p>

<p>
If we now create the index.js entry point for the application, we can have it
create and export a store:
</p>

<p>
index.js
import makeStore from './src/store';
</p>

<p>
export const store = makeStore();
</p>

<p>
Since we also export the store, you could now fire up a Node REPL (with e.g.
babel-node), require the index.js file and interact with the application using
the store.
</p>
</div>
</div>

<div id="outline-container-sec-4-9" class="outline-3">
<h3 id="sec-4-9"><span class="section-number-3">4.9</span> Setting Up a Socket.io Server</h3>
<div class="outline-text-3" id="text-4-9">
<div class="org-src-container">

<pre class="src src-sh">npm install --save socket.io
</pre>
</div>
<p>
This creates a Socket.io server, as well as a regular HTTP server bound to port
</p>
<ol class="org-ol">
<li>The choice of port is arbitrary, but it needs to match the port we'll
</li>
</ol>
<p>
later use to connect from clients.
</p>

<p>
We can then have index.js call this function, so that a server is started when
the app starts:
</p>

<p>
index.js
import makeStore from './src/store';
import startServer from './src/server';
</p>

<p>
export const store = makeStore();
startServer();
</p>

<p>
If we now add a start command to our package.json, we'll make startup a bit
simpler:
</p>

<p>
package.json
"scripts": {
  "start": "babel-node index.js",
  "test": "mocha &#x2013;compilers js:babel-core/register  &#x2013;require ./test/test<sub>helper</sub>.js  &#x2013;recursive",
  "test:watch": "npm run test &#x2013; &#x2013;watch"
},
</p>

<p>
Now we can simply start the server (and create the Redux store) by typing:
</p>

<p>
npm run start
</p>

<p>
The babel-node command comes from the babel-cli package that we installed
earlier. It allows us to easily run Node code with Babel transpiling support
enabled. It adds some performance overhead so it isn't generally recommended
for production use, but it works well for the purposes of our tutorial. 
</p>
</div>
</div>

<div id="outline-container-sec-4-10" class="outline-3">
<h3 id="sec-4-10"><span class="section-number-3">4.10</span> Broadcasting State from A Redux Listener</h3>
<div class="outline-text-3" id="text-4-10">
<p>
We have a Socket.io server and we have a Redux state container but they aren't
yet integrated in any way. The next thing we'll do is change that.
</p>

<p>
Our server should be able to let clients know about the current state of the
application (i.e. "what is being voted on?", "What is the current tally of
votes?", "Is there a winner yet?"). It can do so by emitting a Socket.io event
to all connected clients whenever something changes.
</p>

<p>
And how can we know when something has changed? Well, Redux provides something
for exactly this purpose: You can subscribe to a Redux store. You do that by
providing a function that the store will call after every action it applies,
when the state has potentially changed. It is essentially a callback to state
changes within the store.
</p>

<p>
We'll do this in startServer, so let's give it the Redux store first:
</p>

<p>
index.js
import makeStore from './src/store';
import {startServer} from './src/server';
</p>

<p>
export const store = makeStore();
startServer(store);
</p>

<p>
What we'll do is subscribe a listener to the store that reads the current
state, turns it into a plain JavaScript object, and emits it as a state event
on the Socket.io server. The result will be that a JSON-serialized snapshot of
the state is sent over all active Socket.io connections.
</p>

<p>
src/server.js
import Server from 'socket.io';
</p>

<p>
export function startServer(store) {
  const io = new Server().attach(8090);
</p>

<p>
  store.subscribe(
    () =&gt; io.emit('state', store.getState().toJS())
  );
}
</p>

<p>
We are now publishing the whole state to everyone whenever any changes occur.
This may end up causing a lot of data transfer. One could think of various ways
of optimizing this (e.g. just sending the relevant subset, sending diffs
instead of snapshots&#x2026;), but this implementation has the benefit of being easy
to write, so we'll just use it for our example app. 
</p>

<p>
In addition to sending a state snapshot whenever state changes, it will be
useful for clients to immediately receive the current state when they connect
to the application. That lets them sync their client-side state to the latest
server state right away.
</p>

<p>
We can listen to 'connection' events on our Socket.io server. We get one each
time a client connects. In the event listener we can emit the current state
right away:
</p>

<p>
src/server.js
import Server from 'socket.io';
</p>

<p>
export function startServer(store) {
  const io = new Server().attach(8090);
</p>

<p>
store.subscribe(
  () =&gt; io.emit('state', store.getState().toJS())
);
</p>

<p>
io.on('connection', (socket) =&gt; {
  socket.emit('state', store.getState().toJS());
});
</p>

<p>
}
</p>
</div>
</div>

<div id="outline-container-sec-4-11" class="outline-3">
<h3 id="sec-4-11"><span class="section-number-3">4.11</span> Receiving Remote Redux Actions</h3>
<div class="outline-text-3" id="text-4-11">
<p>
In addition to emitting the application state out to clients, we should also be
able to receive updates from them: Voters will be assigning votes, and the vote
organizer will be moving the contest forward using the NEXT action.
</p>

<p>
The solution we'll use for this is actually quite simple. What we can do is
simply have our clients emit 'action' events that we feed directly into our
Redux store:
</p>

<p>
src/server.js
import Server from 'socket.io';
</p>

<p>
export function startServer(store) {
  const io = new Server().attach(8090);
</p>

<p>
store.subscribe(
() =&gt; io.emit('state', store.getState().toJS())
);
</p>

<p>
io.on('connection', (socket) =&gt; {
  socket.emit('state', store.getState().toJS());
  socket.on('action', store.dispatch.bind(store));
});
</p>

<p>
}
</p>

<p>
This is where we start to go beyond "regular Redux", since we are now
essentially accepting remote actions into our store. However, the Redux
architecture makes it remarkably easy to do: Since actions are just JavaScript
objects, and JavaScript objects can easily be sent over the network, we
immediately got a system with which any number of clients can participate in
voting. That's no small feat!
</p>

<p>
There are some obvious security considerations here. We're allowing any
connected Socket.io client to dispatch any action into the Redux store. 
</p>

<p>
In most real-world cases, there should be some kind of firewall here, probably
not dissimilar to the one in the Vert.x Event Bus Bridge. Apps that have an
authentication mechanism should also plug it in here. 
</p>

<p>
Our server now operates essentially like this:
</p>

<p>
1 A client sends an action to the server. 
2 The server hands the action to the Redux Store. 
3 The Store calls the reducer and the reducer executes the logic related to the
  action. 
4 The Store updates its state based on the return value of the reducer. 
5 The Store executes the listener function subscribed by the server. 
6 The server emits a 'state' event. 
7 All connected clients - including the one that initiated the original action -
  receive the new state. 
</p>

<p>
Before we're done with the server, let's have it load up a set of test entries
for us to play with, so that we have something to look at once we have the
whole system going. We can add an entries.json file that lists the contest
entries. For example, the list of Danny Boyle's feature films to date - feel
free to substitute your favorite subject matter though!
</p>

<p>
entries.json
[
  "Shallow Grave",
  "Trainspotting",
  "A Life Less Ordinary",
  "The Beach",
  "28 Days Later",
  "Millions",
  "Sunshine",
  "Slumdog Millionaire",
  "127 Hours",
  "Trance",
  "Steve Jobs"
]
</p>

<p>
We can just load this in into index.js and then kick off the vote by
dispatching a NEXT action:
</p>

<p>
index.js
import makeStore from './src/store';
import {startServer} from './src/server';
</p>

<p>
export const store = makeStore();
startServer(store);
</p>

<p>
store.dispatch({
  type: 'SET<sub>ENTRIES'</sub>,
  entries: require('./entries.json')
});
store.dispatch({type: 'NEXT'});
</p>

<p>
And with that, we're ready to switch our focus to the client application.
</p>
</div>
</div>
</div>

<div id="outline-container-sec-5" class="outline-2">
<h2 id="sec-5"><span class="section-number-2">5</span> The Client Application</h2>
<div class="outline-text-2" id="text-5">
</div><div id="outline-container-sec-5-1" class="outline-3">
<h3 id="sec-5-1"><span class="section-number-3">5.1</span> Introduction</h3>
<div class="outline-text-3" id="text-5-1">
<p>
During the remainder of this tutorial we'll be writing a React application that
connects to the server we now have and makes the voting system come alive to
users.
</p>

<p>
We're going to use Redux again on the client. This is arguably the most common
use case for Redux: As the underlying engine of a React application. We've
already seen how Redux itself works, and soon we'll learn exactly how it fits
together with React and how using it influences the design of React apps.
</p>
</div>
</div>

<div id="outline-container-sec-5-2" class="outline-3">
<h3 id="sec-5-2"><span class="section-number-3">5.2</span> <span class="done DONE">DONE</span> Client Project Setup</h3>
<div class="outline-text-3" id="text-5-2">
</div><div id="outline-container-sec-5-2-1" class="outline-4">
<h4 id="sec-5-2-1"><span class="section-number-4">5.2.1</span> Introduction</h4>
<div class="outline-text-4" id="text-5-2-1">
<p>
The very first thing we're going to do is start a fresh NPM project, just like
we did with the server.
</p>

<p>
mkdir voting-client
cd voting-client
</p>

<div class="org-src-container">

<pre class="src src-sh">npm init -y
</pre>
</div>

<p>
We're going to need an HTML host page for the app. Let's put that in dist/index.html:
</p>

<p>
dist/index.html
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;
  &lt;div id="app"&gt;&lt;/div&gt;
  &lt;script src="bundle.js"&gt;&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</p>

<p>
This document just contains a &lt;div&gt; with id app, into which we'll put our application. It expects
there to be a JavaScript file called bundle.js in the same directory.
</p>

<p>
Let's also create the first JavaScript file for this app. This will be the application's entry point
file. For now we can just put a simple logging statement in it:
</p>

<p>
src/index.js
console.log('I am alive!');
</p>

<p>
To ease our client development workflow, we're going to use Webpack along with its development server,
so let's add both to the project:
</p>

<div class="org-src-container">

<pre class="src src-sh">npm install --save-dev webpack webpack-dev-server
</pre>
</div>

<p>
If you don't have them already, also install the same packages globally so that you'll be able to
conveniently launch them from the command line: npm install -g webpack webpack-dev-server. 
</p>

<p>
Next, let's add a Webpack configuration file at the root of the project, that matches the files and
directories we've created:
</p>

<div class="org-src-container">

<pre class="src src-sh">npm install --save-dev babel-core babel-loader babel-preset-es2015 babel-preset-react
</pre>
</div>


<p>
You should now be able to run Webpack to produce bundle.js:
</p>

<p>
webpack
</p>

<p>
You should also be able to start the dev server, after which the test page (including the logging
statement from index.js) should be accessible in localhost:8080.
</p>

<p>
webpack-dev-server &#x2013;host=ip
</p>

<p>
In this tutorial we won't be spending any time on CSS. If you'd like the app to look nicer, you can of
course add your own styles as you go along. 
</p>

<p>
Alternatively, you can grab some styling from this commit. In addition to a CSS file, it adds Webpack
support for including (and autoprefixing) it, as well as a slightly improved result visualization
component. 
</p>
</div>
</div>

<div id="outline-container-sec-5-2-2" class="outline-4">
<h4 id="sec-5-2-2"><span class="section-number-4">5.2.2</span> Unit Testing support</h4>
<div class="outline-text-4" id="text-5-2-2">
<p>
We'll be writing some unit tests for the client code too. We can use the same unit test libraries that
we used on the server - Mocha and Chai - to test it:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save-dev mocha chai
</pre>
</div>


<p>
We're going to test our React components as well, and that's going to require a DOM. One alternative
would be to run tests in an actual web browser with a library like Karma. However, we don't actually
need to do that because we can get away with using jsdom, a pure JavaScript DOM implementation that
runs in Node:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save-dev jsdom
</pre>
</div>


<p>
The latest versions of jsdom require io.js or Node.js 4.0.0. If you are running an older Node version,
you need to explicitly install an older version: npm install &#x2013;save-dev jsdom@3 
</p>

<p>
We also need a bit of setup code for jsdom before it's ready for React to use. We essentially need to
create jsdom versions of the document and window objects that would normally be provided by the web
browser. Then we need to put them on the global object, so that they will be discovered by React when
it accesses document or window. We can set up a test helper file for this kind of setup code:
</p>

<p>
test/test<sub>helper</sub>.js
import jsdom from 'jsdom';
</p>

<p>
const doc = jsdom.jsdom('&lt;!doctype html&gt;&lt;html&gt;&lt;body&gt;&lt;/body&gt;&lt;/html&gt;');
const win = doc.defaultView;
</p>

<p>
global.document = doc;
global.window = win;
</p>

<p>
Additionally, we need to take all the properties that the jsdom window object contains, such as
navigator, and hoist them on to the Node.js global object. This is done so that properties provided by
window can be used without the window. prefix, which is what would happen in a browser environment.
Some of the code inside React relies on this:
</p>

<p>
test/test<sub>helper</sub>.js
import jsdom from 'jsdom';
</p>

<p>
const doc = jsdom.jsdom('&lt;!doctype html&gt;&lt;html&gt;&lt;body&gt;&lt;/body&gt;&lt;/html&gt;');
const win = doc.defaultView;
</p>

<p>
global.document = doc;
global.window = win;
</p>

<p>
Object.keys(window).forEach((key) =&gt; {
  if (!(key in global)) {
    global[key] = window[key];
  }
});
</p>

<p>
We're also going to be using Immutable collections, so we need to repeat the same trick we applied on
the server to add Chai expectation support for them. We should install both the immutable and the
chai-immutable package:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save immutable
npm install --save-dev chai-immutable
</pre>
</div>

<p>
Then we should enable it in the test helper file:
</p>

<p>
test/test<sub>helper</sub>.js
import jsdom from 'jsdom';
import chai from 'chai';
import chaiImmutable from 'chai-immutable';
</p>

<p>
const doc = jsdom.jsdom('&lt;!doctype html&gt;&lt;html&gt;&lt;body&gt;&lt;/body&gt;&lt;/html&gt;');
const win = doc.defaultView;
</p>

<p>
global.document = doc;
global.window = win;
</p>

<p>
Object.keys(window).forEach((key) =&gt; {
  if (!(key in global)) {
    global[key] = window[key];
  }
});
</p>

<p>
chai.use(chaiImmutable);
</p>

<p>
The final step before we can run tests is to come up with the command that will run them, and put it
in our package.json. Here it is:
</p>

<p>
package.json
"scripts": {
  "test": "mocha &#x2013;compilers js:babel-core/register &#x2013;require ./test/test<sub>helper</sub>.js 'test/**/*.@(js|jsx)'"
},
</p>

<p>
This is almost the same command that we used in the server's package.json. There only difference is in
the test file specification: On the server we just used &#x2013;recursive, but that option won't find .jsx
files. We need to use a glob that will find all .js and .jsx test files.
</p>

<p>
It will be useful to continuously run tests whenever code changes occur. We can add a test:watch
command for this. It is identical to the one for the server:
</p>

<p>
package.json
"scripts": {
  "test": "mocha &#x2013;compilers js:babel-core/register &#x2013;require ./test/test<sub>helper</sub>.js 'test/**/*.@(js|jsx)'",
  "test:watch": "npm run test &#x2013; &#x2013;watch"
},
</p>
</div>
</div>

<div id="outline-container-sec-5-2-3" class="outline-4">
<h4 id="sec-5-2-3"><span class="section-number-4">5.2.3</span> React and react-hot-loader</h4>
<div class="outline-text-4" id="text-5-2-3">
<p>
With the Webpack and Babel infrastructure in place, let's talk about React!
</p>

<p>
What's really cool about the way React applications get built with Redux and Immutable is that we can
write everything as so-called Pure Components (also sometimes called "Dumb Components"). As a concept,
this is similar to pure functions, in that there are a couple of rules to follow:
</p>

<p>
1 A pure component receives all its data as props, like a function receives all its data as arguments.
  It should have no side effects, including reading data from anywhere else, initiating network
  requests, etc. 
2 A pure component generally has no internal state. What it renders is fully driven by its input
  props. Rendering the same pure component twice with the same props should result in the same UI.
  There's no hidden state inside the component that would cause the UI to differ between the two
  renders. 
</p>

<p>
This has a similar simplifying effect as using pure functions does: We can figure out what a component
does by looking at what it receives as inputs and what it renders. There's nothing else we need to
know about the component. We can also test it really easily - almost as easily as we were able to test
our pure application logic.
</p>

<p>
If components can't have state, where will the state be? In an immutable data structure inside a Redux
store! We've already seen how that works. The big idea is to separate the state from the user
interface code. The React components are just a stateless projection of the state at a given point in
time.
</p>

<p>
But, first things first, let's go ahead and add React to the project:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save react react-dom
</pre>
</div>

<p>
We should also set up react-hot-loader. It will make our development workflow much faster by reloading
code for us without losing the current state of the app.
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save-dev react-hot-loader
</pre>
</div>

<p>
It would be silly of us not to use react-hot-loader, since we'll have an architecture that makes using
it really easy. In fact, the creation of both Redux and react-hot-loader are all part of the same
story! 
</p>

<p>
We need to make several updates to webpack.config.js to enable the hot loader. Here's the updated
version:
</p>

<p>
webpack.config.js
var webpack = require('webpack');
</p>

<p>
module.exports = {
  entry: [
    'webpack-dev-server/client?<a href="http://localhost:8080">http://localhost:8080</a>',
    'webpack/hot/only-dev-server',
    './src/index.js'
  ],
  module: {
    loaders: [{
      test: <i>\.jsx?$</i>,
      exclude: <i>node<sub>modules</sub></i>,
      loader: 'react-hot!babel'
    }]
  },
  resolve: {
    extensions: ['', '.js', '.jsx']
  },
  output: {
    path: _<sub>dirname</sub> + '/dist',
    publicPath: '/',
    filename: 'bundle.js'
  },
  devServer: {
    contentBase: './dist',
    hot: true
  },
  plugins: [
    new webpack.HotModuleReplacementPlugin()
  ]
};
</p>

<p>
In the entry section we include two new things to our app's entry points: The client-side library of
the Webpack dev server and the Webpack hot module loader. These provide the Webpack infrastructure for
hot module replacement. The hot module replacement support isn't loaded by default, so we also need to
load its plugin in the plugins section and enable it in the devServer section.
</p>

<p>
In the loaders section we configure the react-hot loader to be used with our .js and .jsx files, in
addition to Babel.
</p>

<p>
If you now start or restart the development server, you should see a message about Hot Module
Replacement being enabled in the console. We're good to go ahead with writing our first component.
</p>
</div>
</div>

<div id="outline-container-sec-5-2-4" class="outline-4">
<h4 id="sec-5-2-4"><span class="section-number-4">5.2.4</span> Writing The UI for The Voting Screen</h4>
<div class="outline-text-4" id="text-5-2-4">
</div>

<ol class="org-ol"><li><a id="sec-5-2-4-1" name="sec-5-2-4-1"></a>The voting screen<br  /><ol class="org-ol"><li><a id="sec-5-2-4-1-1" name="sec-5-2-4-1-1"></a>Introduction<br  /><div class="outline-text-6" id="text-5-2-4-1-1">
<p>
The application will be quite simple: While voting is ongoing, it'll always
display two buttons - one for each of the entries being voted on. When the vote is over, it'll display
the winner.
</p>

<p>
We've been mainly doing test-first development so far, but for the React components we'll switch our
workflow around: We'll write the components first and the tests second. This is because Webpack and
react-hot-loader provide an even tighter feedback loop for development than unit tests do. Also,
there's no better feedback when writing a UI than to actually see it in action!
</p>

<p>
Let's just assume we're going to have a Voting component and render it in the application entry point.
We can mount it into the #app div that we added to index.html earlier. We should also rename index.js
to index.jsx since it'll now contain some JSX markup:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Voting from './components/Voting';
</p>

<p>
const pair = ['Trainspotting', '28 Days Later'];
</p>

<p>
ReactDOM.render(
  &lt;Voting pair={pair} /&gt;,
  document.getElementById('app')
);
</p>
</div>

<ol class="org-ol"><li><a id="sec-5-2-4-1-1-1" name="sec-5-2-4-1-1-1"></a>changle entrypoint<br  /><div class="outline-text-7" id="text-5-2-4-1-1-1">
<p>
The entrypoint filename must also be changed in webpack.config.js:
</p>

<p>
webpack.config.js
entry: [
  'webpack-dev-server/client?<a href="http://localhost:8080">http://localhost:8080</a>',
  'webpack/hot/only-dev-server',
  './src/index.jsx'
],
</p>

<p>
If you start (or restart) webpack-dev-server now, you'll see it complain about the missing Voting
component. Let's fix that by writing our first version of it:
   
</p>
</div>
</li></ol>
</li></ol>
</li>

<li><a id="sec-5-2-4-2" name="sec-5-2-4-2"></a>The Voting component<br  /><div class="outline-text-5" id="text-5-2-4-2">
<p>
takes the current pair of entries as props. For now we can just hardcode that
pair, and later we'll substitute it with real data. The component itself is pure and doesn't care
where the data comes from.
</p>


<p>
src/components/Voting.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  getPair: function() {
    return this.props.pair || [];
  },
  render: function() {
    return &lt;div className="voting"&gt;
      {this.getPair().map(entry =&gt;
        &lt;button key={entry}&gt;
          &lt;h1&gt;{entry}&lt;/h1&gt;
        &lt;/button&gt;
      )}
    &lt;/div&gt;;
  }
});
</p>

<p>
This renders the pair of entries as buttons. You should be able to see them in your web browser. Try
making some changes to the component code and see how they're immediately applied in the browser. No
restarts, no page reloads. Talk about fast feedback!
</p>

<p>
If you don't see what you expect, check the webpack-dev-server output as well as the console log in
your browser's development tools for problems. 
</p>
</div>
</li>

<li><a id="sec-5-2-4-3" name="sec-5-2-4-3"></a>Now we can add our first unit test as well<br  /><ol class="org-ol"><li><a id="sec-5-2-4-3-1" name="sec-5-2-4-3-1"></a>Introduction<br  /><div class="outline-text-6" id="text-5-2-4-3-1">
<p>
for the functionality that we've got. It'll go in a file
called Voting<sub>spec</sub>.jsx:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
import Voting from '../../src/components/Voting';
</p>

<p>
describe('Voting', () =&gt; {
</p>

<p>
});
</p>
</div>
</li>

<li><a id="sec-5-2-4-3-2" name="sec-5-2-4-3-2"></a>renderIntoDocument<br  /><div class="outline-text-6" id="text-5-2-4-3-2">
<p>
To test that the component renders those buttons based on the pair prop, we should render it and see
what the output was. To render a component in a unit test, we can use a helper function called
renderIntoDocument, which will be in react/addons:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
import React from 'react/addons';
import Voting from '../../src/components/Voting';
</p>

<p>
const {renderIntoDocument} = React.addons.TestUtils;
</p>

<p>
describe('Voting', () =&gt; {
</p>

<p>
it('renders a pair of buttons', () =&gt; {
  const component = renderIntoDocument(
    &lt;Voting pair={["Trainspotting", "28 Days Later"]} /&gt;
  );
});
</p>

<p>
});
</p>
</div>
</li>

<li><a id="sec-5-2-4-3-3" name="sec-5-2-4-3-3"></a>scryRenderedDOMComponentsWithTag<br  /><div class="outline-text-6" id="text-5-2-4-3-3">
<p>
Once the component is rendered, we can use another React helper function called
scryRenderedDOMComponentsWithTag to find the button elements we expect there to be. We expect two of
them, and we expect their text contents to be the two entries, respectively:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
import React from 'react/addons';
import Voting from '../../src/components/Voting';
import {expect} from 'chai';
</p>

<p>
const {renderIntoDocument, scryRenderedDOMComponentsWithTag}
  = React.addons.TestUtils;
</p>

<p>
describe('Voting', () =&gt; {
</p>

<p>
it('renders a pair of buttons', () =&gt; {
  const component = renderIntoDocument(
    &lt;Voting pair={["Trainspotting", "28 Days Later"]} /&gt;
  );
  const buttons = scryRenderedDOMComponentsWithTag(component, 'button');
</p>

<p>
  expect(buttons.length).to.equal(2);
  expect(buttons<sup><a id="fnr.1" name="fnr.1" class="footref" href="#fn.1">1</a></sup>.textContent).to.equal('Trainspotting');
  expect(buttons<sup><a id="fnr.2" name="fnr.2" class="footref" href="#fn.2">2</a></sup>.textContent).to.equal('28 Days Later');
});
</p>

<p>
});
</p>

<p>
If you run the test now, you should see it pass:
</p>
</div>
</li>
<li><a id="sec-5-2-4-3-4" name="sec-5-2-4-3-4"></a>Test: renders a pair of buttons<br  /><div class="outline-text-6" id="text-5-2-4-3-4">
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-2-4-3-5" name="sec-5-2-4-3-5"></a>Simulating<br  /><div class="outline-text-6" id="text-5-2-4-3-5">
<p>
the component should invoke a callback function. Like the
entry pair, the callback function should also be given to the component as a prop.
</p>

<p>
Let's go ahead and add a unit test for this too. We can test this by simulating a click using the
Simulate object from React's test utilities:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
import React from 'react/addons';
import Voting from '../../src/components/Voting';
import {expect} from 'chai';
</p>

<p>
const {renderIntoDocument, scryRenderedDOMComponentsWithTag, Simulate}
  = React.addons.TestUtils;
</p>

<p>
describe('Voting', () =&gt; {
</p>

<p>
// &#x2026;
</p>

<p>
it('invokes callback when a button is clicked', () =&gt; {
  let votedWith;
  const vote = (entry) =&gt; votedWith = entry;
</p>

<p>
const component = renderIntoDocument(
  &lt;Voting pair={["Trainspotting", "28 Days Later"]}
          vote={vote}/&gt;
);
const buttons = scryRenderedDOMComponentsWithTag(component, 'button');
Simulate.click(buttons<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup>);
</p>

<p>
  expect(votedWith).to.equal('Trainspotting');
});
</p>

<p>
});
</p>
</div>
</li>

<li><a id="sec-5-2-4-3-6" name="sec-5-2-4-3-6"></a>Onclick handler<br  /><div class="outline-text-6" id="text-5-2-4-3-6">
<p>
Getting this test to pass is simple enough. We just need an onClick handler on the buttons that
invokes vote with the correct entry:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  getPair: function() {
    return this.props.pair || [];
  },
  render: function() {
    return &lt;div className="voting"&gt;
      {this.getPair().map(entry =&gt;
        &lt;button key={entry}
                onClick={() =&gt; this.props.vote(entry)}&gt;
          &lt;h1&gt;{entry}&lt;/h1&gt;
        &lt;/button&gt;
      )}
    &lt;/div&gt;;
  }
});
</p>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>


<p>
This is generally how we'll manage user input and actions with pure components: The components don't
try to do much about those actions themselves. They merely invoke callback props.
</p>

<p>
Here we switched back to test-first development by writing the test first and the functionality
second. I find it's often easier to initially test user input code from tests than through the
browser. 
</p>

<p>
In general, we'll be switching between the test-first and test-last workflows during UI development,
based on whichever feels more useful at each step. 
</p>
</div>
</li></ol>
</li>

<li><a id="sec-5-2-4-4" name="sec-5-2-4-4"></a>Once the user has already voted for a pair<br  /><div class="outline-text-5" id="text-5-2-4-4">
<p>
     we probably shouldn't let them vote again. While we could
handle this internally in the component state, we're really trying to keep our components pure, so we
should try to externalize that logic. The component could just take a hasVoted prop, for which we'll
just hardcode a value for now:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Voting from './components/Voting';
</p>

<p>
const pair = ['Trainspotting', '28 Days Later'];
</p>

<p>
ReactDOM.render(
  &lt;Voting pair={pair} hasVoted="Trainspotting" /&gt;,
  document.getElementById('app')
);
</p>

<p>
 
</p>

<p>
We can make this work quite easily:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  getPair: function() {
    return this.props.pair || [];
  },
  isDisabled: function() {
    return !!this.props.hasVoted;
  },
  render: function() {
    return &lt;div className="voting"&gt;
      {this.getPair().map(entry =&gt;
        &lt;button key={entry}
                disabled={this.isDisabled()}
                onClick={() =&gt; this.props.vote(entry)}&gt;
          &lt;h1&gt;{entry}&lt;/h1&gt;
        &lt;/button&gt;
      )}
    &lt;/div&gt;;
  }
});
</p>
</div>

<ol class="org-ol"><li><a id="sec-5-2-4-4-1" name="sec-5-2-4-4-1"></a>Let's also add a little label to the button<br  /><div class="outline-text-6" id="text-5-2-4-4-1">
<p>
that the user has voted on, so that it is clear to them
what has happened. The label should become visible for the button whose entry matches the hasVoted
prop. We can make a new helper method hasVotedFor to decide whether to render the label or not:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  getPair: function() {
    return this.props.pair || [];
  },
  isDisabled: function() {
    return !!this.props.hasVoted;
  },
  hasVotedFor: function(entry) {
    return this.props.hasVoted <code>=</code> entry;
  },
  render: function() {
    return &lt;div className="voting"&gt;
      {this.getPair().map(entry =&gt;
        &lt;button key={entry}
                disabled={this.isDisabled()}
                onClick={() =&gt; this.props.vote(entry)}&gt;
          &lt;h1&gt;{entry}&lt;/h1&gt;
          {this.hasVotedFor(entry) ?
            &lt;div className="label"&gt;Voted&lt;/div&gt; :
            null}
        &lt;/button&gt;
      )}
    &lt;/div&gt;;
  }
});
</p>
</div>
</li></ol>
</li>

<li><a id="sec-5-2-4-5" name="sec-5-2-4-5"></a>Winners<br  /><ol class="org-ol"><li><a id="sec-5-2-4-5-1" name="sec-5-2-4-5-1"></a>The final requirement<br  /><div class="outline-text-6" id="text-5-2-4-5-1">
<p>
for the voting screen is that once there is a winner, it will show just that,
instead of trying to render any voting buttons. There might another prop for the winner. Again, we can
simply hardcode a value for it temporarily until we have real data to plug in:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Voting from './components/Voting';
</p>

<p>
const pair = ['Trainspotting', '28 Days Later'];
</p>

<p>
ReactDOM.render(
  &lt;Voting pair={pair} winner="Trainspotting" /&gt;,
  document.getElementById('app')
);
</p>

<p>
 
</p>
</div>
</li>

<li><a id="sec-5-2-4-5-2" name="sec-5-2-4-5-2"></a>We could handle this in the component by conditionally rendering a winner div or the buttons:<br  /><div class="outline-text-6" id="text-5-2-4-5-2">
<p>
src/components/Voting.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  getPair: function() {
    return this.props.pair || [];
  },
  isDisabled: function() {
    return !!this.props.hasVoted;
  },
  hasVotedFor: function(entry) {
    return this.props.hasVoted <code>=</code> entry;
  },
  render: function() {
    return &lt;div className="voting"&gt;
      {this.props.winner ?
        &lt;div ref="winner"&gt;Winner is {this.props.winner}!&lt;/div&gt; :
        this.getPair().map(entry =&gt;
          &lt;button key={entry}
                  disabled={this.isDisabled()}
                  onClick={() =&gt; this.props.vote(entry)}&gt;
            &lt;h1&gt;{entry}&lt;/h1&gt;
            {this.hasVotedFor(entry) ?
              &lt;div className="label"&gt;Voted&lt;/div&gt; :
              null}
          &lt;/button&gt;
        )}
    &lt;/div&gt;;
  }
});
</p>
</div>
</li>

<li><a id="sec-5-2-4-5-3" name="sec-5-2-4-5-3"></a>Winner component<br  /><div class="outline-text-6" id="text-5-2-4-5-3">
<p>
This is the functionality that we need, but the rendering code is now slightly messy. It might be
better if we extract some separate components from this, so that the Voting screen component renders
either a Winner component or a Vote component. Starting with the Winner component, it can just render
a div:
</p>

<p>
src/components/Winner.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  render: function() {
    return &lt;div className="winner"&gt;
      Winner is {this.props.winner}!
    &lt;/div&gt;;
  }
});
</p>

<p>
The Vote component will be pretty much exactly like the Voting component was before - just concerned
with the voting buttons:
</p>

<p>
src/components/Vote.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  getPair: function() {
    return this.props.pair || [];
  },
  isDisabled: function() {
    return !!this.props.hasVoted;
  },
  hasVotedFor: function(entry) {
    return this.props.hasVoted <code>=</code> entry;
  },
  render: function() {
    return &lt;div className="voting"&gt;
      {this.getPair().map(entry =&gt;
        &lt;button key={entry}
                disabled={this.isDisabled()}
                onClick={() =&gt; this.props.vote(entry)}&gt;
          &lt;h1&gt;{entry}&lt;/h1&gt;
          {this.hasVotedFor(entry) ?
            &lt;div className="label"&gt;Voted&lt;/div&gt; :
            null}
        &lt;/button&gt;
      )}
    &lt;/div&gt;;
  }
});
</p>

<p>
The Voting component itself now merely makes a decision about which of these two components to render:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
import Winner from './Winner';
import Vote from './Vote';
</p>

<p>
export default React.createClass({
  render: function() {
    return &lt;div&gt;
      {this.props.winner ?
        &lt;Winner ref="winner" winner={this.props.winner} /&gt; :
        &lt;Vote {&#x2026;this.props} /&gt;}
    &lt;/div&gt;;
  }
});
</p>
</div>

<ol class="org-ol"><li><a id="sec-5-2-4-5-3-1" name="sec-5-2-4-5-3-1"></a>Notice that we added a ref for the Winner component.<br  /><div class="outline-text-7" id="text-5-2-4-5-3-1">
<p>
It's something we'll use in unit tests to grab the corresponding DOM node.
</p>

<p>
That's our pure Voting component! Notice how we haven't really implemented any logic yet: There are
buttons but we haven't specified what they do, except invoke a callback. Our components are concerned
with rendering the UI and only that. The application logic will come in later, when we connect the UI
to a Redux store.
</p>

<p>
Before we move on though, time to writes some more unit tests for the new features we've added.
Firstly, the presence of the hasVoted props should cause the voting buttons to become disabled:
</p>
</div>
</li></ol>
</li></ol>
</li>

<li><a id="sec-5-2-4-6" name="sec-5-2-4-6"></a>Testing HasVoted<br  /><div class="outline-text-5" id="text-5-2-4-6">
<p>
test/components/Voting<sub>spec</sub>.jsx
it('disables buttons when user has voted', () =&gt; {
  const component = renderIntoDocument(
    &lt;Voting pair={["Trainspotting", "28 Days Later"]}
            hasVoted="Trainspotting" /&gt;
  );
  const buttons = scryRenderedDOMComponentsWithTag(component, 'button');
</p>

<p>
  expect(buttons.length).to.equal(2);
  expect(buttons<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup>.hasAttribute('disabled')).to.equal(true);
  expect(buttons<sup><a id="fnr.2.100" name="fnr.2.100" class="footref" href="#fn.2">2</a></sup>.hasAttribute('disabled')).to.equal(true);
});
</p>

<p>
A 'Voted' label should be present on the button whose entry matches the value of hasVoted:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
it('adds label to the voted entry', () =&gt; {
  const component = renderIntoDocument(
    &lt;Voting pair={["Trainspotting", "28 Days Later"]}
            hasVoted="Trainspotting" /&gt;
  );
  const buttons = scryRenderedDOMComponentsWithTag(component, 'buttons');
</p>

<p>
  expect(buttons<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup>.textContent).to.contain('Voted');
});
</p>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-2-4-7" name="sec-5-2-4-7"></a>Testing Winner<br  /><div class="outline-text-5" id="text-5-2-4-7">
<p>
When there's a winner, there should be no buttons, but instead an element with the winner ref:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
it('renders just the winner when there is one', () =&gt; {
  const component = renderIntoDocument(
    &lt;Voting winner="Trainspotting" /&gt;
  );
  const buttons = scryRenderedDOMComponentsWithTag(component, 'button');
  expect(buttons.length).to.equal(0);
</p>

<p>
  const winner = React.findDOMNode(component.refs.winner);
  expect(winner).to.be.ok;
  expect(winner.textContent).to.contain('Trainspotting');
});
</p>

<p>
We could also have written unit tests for each component separately, but I find it more appropriate in
this case to treat the Voting screen as the "unit" to test. We test the component's external behavior,
and the fact that it uses smaller components internally is an implementation detail. 
</p>
</div>
</li></ol>
</div>
</div>

<div id="outline-container-sec-5-3" class="outline-3">
<h3 id="sec-5-3"><span class="section-number-3">5.3</span> <span class="done DONE">DONE</span> Immutable Data And Pure Rendering</h3>
<div class="outline-text-3" id="text-5-3">
</div>
<div id="outline-container-sec-5-3-1" class="outline-4">
<h4 id="sec-5-3-1"><span class="section-number-4">5.3.1</span> Introduction</h4>
<div class="outline-text-4" id="text-5-3-1">
<p>
We have discussed the virtues of using immutable data, but there's one additional, very practical
benefit that we get when using it together with React: If we only use immutable data in component
props, and write the component as a pure component, we can have React use a more efficient strategy
for detecting changes in the props.
</p>
</div>
</div>

<div id="outline-container-sec-5-3-2" class="outline-4">
<h4 id="sec-5-3-2"><span class="section-number-4">5.3.2</span> Testing PureRenderMixin</h4>
<div class="outline-text-4" id="text-5-3-2">
</div>

<ol class="org-ol"><li><a id="sec-5-3-2-1" name="sec-5-3-2-1"></a>Introduction<br  /><div class="outline-text-5" id="text-5-3-2-1">
<p>
This is done by applying the PureRenderMixin that is available as an add-on package. When this mixin
is added to a component, it changes the way React checks for changes in the component's props (and
state). Instead of a deep compare it does a shallow compare, which is much, much faster.
</p>

<p>
The reason we can do this is that by definition, there can never be changes within immutable data
structures. If the props of a component are all immutable values, and the props keep pointing to the
same values between renders, there can be no reason to re-render the component, and it can be skipped
completely!
</p>
</div>
</li>

<li><a id="sec-5-3-2-2" name="sec-5-3-2-2"></a>Test for mutable data<br  /><div class="outline-text-5" id="text-5-3-2-2">
<p>
We can concretely see what this is about by writing some unit tests. Our component is supposed to be
pure, so if we did give it a mutable array, and then caused a mutation inside the array, it should not
be re-rendered:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
it('renders as a pure component', () =&gt; {
  const pair = ['Trainspotting', '28 Days Later'];
  const component = renderIntoDocument(
    &lt;Voting pair={pair} /&gt;
  );
</p>

<p>
let firstButton = scryRenderedDOMComponentsWithTag(component, 'button')<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup>;
expect(firstButton.textContent).to.equal('Trainspotting');
</p>

<p>
  pair<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup> = 'Sunshine';
  component.setProps({pair: pair});
  firstButton = scryRenderedDOMComponentsWithTag(component, 'button')<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup>;
  expect(firstButton.textContent).to.equal('Trainspotting');
});
</p>
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-3-2-3" name="sec-5-3-2-3"></a>test case for immutable data pair<br  /><div class="outline-text-5" id="text-5-3-2-3">
<p>
We should have to explicitly set a new immutable list in the props to have the change reflected in the
UI:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
import React from 'react/addons';
import {List} from 'immutable';
import Voting from '../../src/components/Voting';
import {expect} from 'chai';
</p>

<p>
const {renderIntoDocument, scryRenderedDOMComponentsWithTag, Simulate}
  = React.addons.TestUtils;
</p>

<p>
describe('Voting', () =&gt; {
</p>

<p>
// &#x2026;
</p>

<p>
it('does update DOM when prop changes', () =&gt; {
  const pair = List.of('Trainspotting', '28 Days Later');
  const component = renderIntoDocument(
    &lt;Voting pair={pair} /&gt;
  );
</p>

<p>
let firstButton = scryRenderedDOMComponentsWithTag(component, 'button')<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup>;
expect(firstButton.textContent).to.equal('Trainspotting');
</p>

<p>
  const newPair = pair.set(0, 'Sunshine');
  component.setProps({pair: newPair});
  firstButton = scryRenderedDOMComponentsWithTag(component, 'button')<sup><a id="fnr.1.100" name="fnr.1.100" class="footref" href="#fn.1">1</a></sup>;
  expect(firstButton.textContent).to.equal('Sunshine');
});
</p>

<p>
});
</p>

<p>
I wouldn't usually bother writing tests like this one, and would just assume that PureRenderMixin is
being used. In this case the tests just happen to help us understand what exactly is going on. 
</p>

<p>
Running the tests at this point will show how the component is not currently behaving as we expect:
It'll update the UI in both cases, which means it is doing deep checks within the props, 
which is what we wanted to avoid since we're going to be using immutable data.
</p>

<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-3-2-4" name="sec-5-3-2-4"></a>PureRenderMixin in React addons<br  /><div class="outline-text-5" id="text-5-3-2-4">
<p>
Everything falls into place when we enable the pure render mixin in our components. We need to install
its package first:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save react-addons-pure-render-mixin
</pre>
</div>


<p>
If we now mix it into our components, tests start passing and we're done:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
import Winner from './Winner';
import Vote from './Vote';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  // &#x2026;
});
src/components/Vote.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  // &#x2026;
});
src/components/Winner.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  // &#x2026;
});
</p>

<p>
Strictly speaking, the tests would start to pass if we only enabled the pure render mixin for Voting
and didn't bother with the two other components. That's because when React doesn't notice any changes
in the Voting props, it skips re-rendering for the whole component subtree. 
</p>

<p>
However, I find it more appropriate to consistently use the pure render mixin in all my components,
both to make it explicit that the components are pure, and to make sure they will behave as I expect
even after I rearrange them. 
</p>
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li></ol>
</div>
</div>

<div id="outline-container-sec-5-4" class="outline-3">
<h3 id="sec-5-4"><span class="section-number-3">5.4</span> <span class="done DONE">DONE</span> Writing The UI for The Results Screen And Handling Routing</h3>
<div class="outline-text-3" id="text-5-4">
</div>
<div id="outline-container-sec-5-4-1" class="outline-4">
<h4 id="sec-5-4-1"><span class="section-number-4">5.4.1</span> Voting Screen</h4>
<div class="outline-text-4" id="text-5-4-1">
<p>
With that Voting screen all done, let's move on to the other main screen of the app: The one where
results will be shown.
The data displayed here is the same pair of entries as in the voting screen, and the tally of votes
for each. Additionally, there's a little button on the bottom with which the person managing the vote
can move on to the next pair.
</p>
</div>
</div>
<div id="outline-container-sec-5-4-2" class="outline-4">
<h4 id="sec-5-4-2"><span class="section-number-4">5.4.2</span> Result Screen</h4>
<div class="outline-text-4" id="text-5-4-2">
<p>
What we have here are two separate screens, exactly one of which should be shown at any given time. To
choose between the two, using URL paths might be a good idea: We could set the root path #/ to show
the voting screen, and a #/results path to show the results screen.
</p>
</div>
</div>
<div id="outline-container-sec-5-4-3" class="outline-4">
<h4 id="sec-5-4-3"><span class="section-number-4">5.4.3</span> Router</h4>
<div class="outline-text-4" id="text-5-4-3">
</div>

<ol class="org-ol"><li><a id="sec-5-4-3-1" name="sec-5-4-3-1"></a><span class="done DONE">DONE</span> Install<br  /><div class="outline-text-5" id="text-5-4-3-1">
<p>
     That kind of thing can easily be done with the react-router library, with which we can associate
different components to different paths. Let's add it to the project:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save react-router@1.0.0-rc3
</pre>
</div>
</div>
</li>
<li><a id="sec-5-4-3-2" name="sec-5-4-3-2"></a><span class="todo TEST">TEST</span> Adding Voting route<br  /><div class="outline-text-5" id="text-5-4-3-2">
<p>
We can now configure our route paths. The Router comes with a React component called Route, which can
be used to declaratively define a routing table. For now, we'll have just one route:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import {Route} from 'react-router';
import App from './components/App';
import Voting from './components/Voting';
</p>

<p>
const pair = ['Trainspotting', '28 Days Later'];
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/" component={Voting} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Voting pair={pair} /&gt;,
  document.getElementById('app')
);
</p>

<p>
 
</p>

<p>
We have a single route that we have configured to point to the Voting component. The other thing we've
done here is define a component for the root Route in the configuration, which will be shared for all
the concrete routes within. It's pointing to an App component, which we'll soon create.
</p>
</div>
</li>

<li><a id="sec-5-4-3-3" name="sec-5-4-3-3"></a><span class="todo TEST">TEST</span> Root Component<br  /><div class="outline-text-5" id="text-5-4-3-3">
<p>
The purpose of the root route component is to render all the markup that is common across all routes.
Here's what our root component App should look like:
</p>

<p>
src/components/App.jsx
import React from 'react';
import {List} from 'immutable';
</p>

<p>
const pair = List.of('Trainspotting', '28 Days Later');
</p>

<p>
export default React.createClass({
  render: function() {
    return React.cloneElement(this.props.children, {pair: pair});
  }
});
</p>

<p>
 
</p>

<p>
This component does nothing except render its child components, expected to be given in as the
children prop. This is something that the react-router package does for us. It plugs in the component
(s) defined for whatever the current route happens to be. Since we currently just have the one route
for Voting, at the moment this component always renders Voting.
</p>
</div>
</li>
<li><a id="sec-5-4-3-4" name="sec-5-4-3-4"></a><span class="todo TEST">TEST</span> CloneElement API<br  /><div class="outline-text-5" id="text-5-4-3-4">
<p>
Notice that we've moved the placeholder pair data from index.jsx to App.jsx. We use React's
cloneElement API to create a clone of the original components with our custom pair prop attached. This
is just a temporary measure, and we'll be able to remove the cloning call later. 
</p>

<p>
Earlier we discussed how <b>it's generally a good idea to use the pure render mixin across all</b>
<b>components. The App component is an exception to this rule.</b> The reason is that it would cause route
changes not to fire, because of an implementation issue between the router and React itself. This
situation may well change in the near future.
</p>
</div>
</li>
<li><a id="sec-5-4-3-5" name="sec-5-4-3-5"></a><span class="todo TEST">TEST</span> Kickstart the Router<br  /><div class="outline-text-5" id="text-5-4-3-5">
<p>
We can now switch back to index.js where we can kickstart the Router itself, and have it initialize
our application:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import App from './components/App';
import Voting from './components/Voting';
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/" component={Voting} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Router&gt;{routes}&lt;/Router&gt;,
  document.getElementById('app')
);
</p>

<p>
We now supply the Router component from the react-router package as the root component of our
application. We plug our route table into it by passing it in as a child component.
</p>


<p>
With this, we've restored the previous functionality of our app: It just renders the Voting component.
But this time it is done with the React router baked in, which means we can now easily add more
routes.
</p>
</div>
</li></ol>
</div>
<div id="outline-container-sec-5-4-4" class="outline-4">
<h4 id="sec-5-4-4"><span class="section-number-4">5.4.4</span> Implemantation of results screen</h4>
<div class="outline-text-4" id="text-5-4-4">
</div><ol class="org-ol"><li><a id="sec-5-4-4-0-1" name="sec-5-4-4-0-1"></a><span class="todo TEST">TEST</span> Initilization<br  /><div class="outline-text-6" id="text-5-4-4-0-1">
<p>
This will be served by a new component called Results:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import App from './components/App';
import Voting from './components/Voting';
import Results from './components/Results';
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={Results} /&gt;
  &lt;Route path="/" component={Voting} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Router&gt;{routes}&lt;/Router&gt;,
  document.getElementById('app')
);
</p>

<p>
Here we use the &lt;Route&gt; component again to specify that for a path named "/results", the Results
component should be used. Everything else will still be handled by Voting.
</p>
</div>
</li>
<li><a id="sec-5-4-4-0-2" name="sec-5-4-4-0-2"></a><span class="todo TEST">TEST</span> Simple implementation of Results<br  /><div class="outline-text-6" id="text-5-4-4-0-2">

<p>
Let's make a simple implementation of Results so that we can see how the routing works:
</p>

<p>
src/components/Results.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  render: function() {
    return &lt;div&gt;Hello from results!&lt;/div&gt;
  }
});
</p>

<p>
If you now point your browser to <a href="http://localhost:8080/#/results">http://localhost:8080/#/results</a>, you should see the little message
from the Results component. The root path, on the other hand, should show the voting buttons. You can
also use the back and forward buttons to switch between the routes, and the visible component is
switched while the application remains alive. That's the router in action!
</p>

<p>
This is all we're going to do with the React Router in this application. The library is capable of a
lot more though. Take a look at its documentation to find out about all the things you can do with it.
</p>
</div>
</li>
<li><a id="sec-5-4-4-0-3" name="sec-5-4-4-0-3"></a><span class="todo TEST">TEST</span> Implemantation of Results component<br  /><div class="outline-text-6" id="text-5-4-4-0-3">

<p>
Now that we have a placeholder Results component, let's go right ahead and make it do something
useful. It should display the same two entries currently being voted on that the Voting component
does:
</p>

<p>
src/components/Results.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  getPair: function() {
    return this.props.pair || [];
  },
  render: function() {
    return &lt;div className="results"&gt;
      {this.getPair().map(entry <code>&gt;
        &lt;div key={entry} className</code>"entry"&gt;
          &lt;h1&gt;{entry}&lt;/h1&gt;
        &lt;/div&gt;
      )}
    &lt;/div&gt;;
  }
  });
</p>
</div>
</li>
<li><a id="sec-5-4-4-0-4" name="sec-5-4-4-0-4"></a><span class="todo TEST">TEST</span> Add Tally<br  /><div class="outline-text-6" id="text-5-4-4-0-4">

<p>
Since this is the results screen, it should also actually show the tally of votes. That's what people
want to see when they're on this screen. Let's pass in a placeholder tally Map to the component from
our root App component first:
</p>

<p>
src/components/App.jsx
import React from 'react';
import {List, Map} from 'immutable';
</p>

<p>
const pair = List.of('Trainspotting', '28 Days Later');
const tally = Map({'Trainspotting': 5, '28 Days Later': 4});
</p>

<p>
export default React.createClass({
  render: function() {
    return React.cloneElement(this.props.children, {
      pair: pair,
      tally: tally
    });
  }
});
</p>

<p>
Now we can tweak the Results component to show those numbers:
</p>

<p>
src/components/Results.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  getPair: function() {
    return this.props.pair || [];
  },
  getVotes: function(entry) {
    if (this.props.tally &amp;&amp; this.props.tally.has(entry)) {
      return this.props.tally.get(entry);
    }
    return 0;
  },
  render: function() {
    return &lt;div className="results"&gt;
      {this.getPair().map(entry <code>&gt;
        &lt;div key={entry} className</code>"entry"&gt;
          &lt;h1&gt;{entry}&lt;/h1&gt;
          &lt;div className="voteCount"&gt;
            {this.getVotes(entry)}
          &lt;/div&gt;
        &lt;/div&gt;
      )}
    &lt;/div&gt;;
  }
});
</p>

<p>
At this point, let's switch gears and add a unit test for the current behavior of the Results
component to make sure we won't break it later.
</p>
</div>
</li>
<li><a id="sec-5-4-4-1" name="sec-5-4-4-1"></a>UNIT Testing for Voting Result<br  /><div class="outline-text-5" id="text-5-4-4-1">
<p>
We expect the component to render a div for each entry, and display both the entry name and the number
of votes within that div. For entries that have no votes, a vote count of zero should be shown:
</p>

<p>
test/components/Results<sub>spec</sub>.jsx
import React from 'react/addons';
import {List, Map} from 'immutable';
import Results from '../../src/components/Results';
import {expect} from 'chai';
</p>

<p>
const {renderIntoDocument, scryRenderedDOMComponentsWithClass}
  = React.addons.TestUtils;
</p>

<p>
describe('Results', () =&gt; {
</p>

<p>
it('renders entries with vote counts or zero', () =&gt; {
  const pair = List.of('Trainspotting', '28 Days Later');
  const tally = Map({'Trainspotting': 5});
  const component = renderIntoDocument(
    &lt;Results pair={pair} tally={tally} /&gt;
  );
  const entries = scryRenderedDOMComponentsWithClass(component, 'entry');
  const [train, days] = entries.map(e =&gt; e.textContent);
</p>

<p>
  expect(entries.length).to.equal(2);
  expect(train).to.contain('Trainspotting');
  expect(train).to.contain('5');
  expect(days).to.contain('28 Days Later');
  expect(days).to.contain('0');
});
</p>

<p>
});
</p>
</div>
</li>

<li><a id="sec-5-4-4-2" name="sec-5-4-4-2"></a>Next button of the Result<br  /><ol class="org-ol"><li><a id="sec-5-4-4-2-1" name="sec-5-4-4-2-1"></a>Test case<br  /><div class="outline-text-6" id="text-5-4-4-2-1">
<p>
Next, let's talk about the "Next" button, which is used to move the voting to the next entry.
</p>

<p>
From the component's point of view, there should just be a callback function in the props. The
component should invoke that callback when the "Next" button inside it is clicked. We can formulate a
unit test for this, which is quite similar to the ones we made for the voting buttons:
</p>

<p>
test/components/Results<sub>spec</sub>.jsx
import React from 'react/addons';
import {List, Map} from 'immutable';
import Results from '../../src/components/Results';
import {expect} from 'chai';
</p>

<p>
const {renderIntoDocument, scryRenderedDOMComponentsWithClass, Simulate}
  = React.addons.TestUtils;
</p>

<p>
describe('Results', () =&gt; {
</p>

<p>
// &#x2026;
</p>

<p>
it('invokes the next callback when next button is clicked', () =&gt; {
  let nextInvoked = false;
  const next = () =&gt; nextInvoked = true;
</p>

<p>
const pair = List.of('Trainspotting', '28 Days Later');
const component = renderIntoDocument(
  &lt;Results pair={pair}
           tally={Map()}
           next={next}/&gt;
);
Simulate.click(React.findDOMNode(component.refs.next));
</p>

<p>
  expect(nextInvoked).to.equal(true);
});
</p>

<p>
});
</p>
</div>
</li>
<li><a id="sec-5-4-4-2-2" name="sec-5-4-4-2-2"></a>Implemantation<br  /><div class="outline-text-6" id="text-5-4-4-2-2">
<p>
The implementation is also similar to the voting buttons. It is just slightly simpler, as there are no
arguments to pass:
</p>

<p>
src/components/Results.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  getPair: function() {
    return this.props.pair || [];
  },
  getVotes: function(entry) {
    if (this.props.tally &amp;&amp; this.props.tally.has(entry)) {
      return this.props.tally.get(entry);
    }
    return 0;
  },
  render: function() {
    return &lt;div className="results"&gt;
      &lt;div className="tally"&gt;
        {this.getPair().map(entry <code>&gt;
          &lt;div key={entry} className</code>"entry"&gt;
            &lt;h1&gt;{entry}&lt;/h1&gt;
            &lt;div class="voteCount"&gt;
              {this.getVotes(entry)}
            &lt;/div&gt;
          &lt;/div&gt;
        )}
      &lt;/div&gt;
      &lt;div className="management"&gt;
        &lt;button ref="next"
                className="next"
                onClick={this.props.next}&gt;
          Next
        &lt;/button&gt;
      &lt;/div&gt;
    &lt;/div&gt;;
  }
});
</p>
</div>
</li></ol>
</li>
<li><a id="sec-5-4-4-3" name="sec-5-4-4-3"></a>Winner screen in result<br  /><ol class="org-ol"><li><a id="sec-5-4-4-3-1" name="sec-5-4-4-3-1"></a>Unit Test<br  /><div class="outline-text-6" id="text-5-4-4-3-1">
<p>
Finally, just like the Voting screen, the Results screen should display the winner once we have one:
</p>

<p>
test/components/Results<sub>spec</sub>.jsx
it('renders the winner when there is one', () =&gt; {
  const component = renderIntoDocument(
    &lt;Results winner="Trainspotting"
             pair={["Trainspotting", "28 Days Later"]}
             tally={Map()} /&gt;
  );
  const winner = React.findDOMNode(component.refs.winner);
  expect(winner).to.be.ok;
  expect(winner.textContent).to.contain('Trainspotting');
});
</p>
</div>
</li>
<li><a id="sec-5-4-4-3-2" name="sec-5-4-4-3-2"></a>Source<br  /><div class="outline-text-6" id="text-5-4-4-3-2">
<p>
We can implement this by simply reusing the Winner component we already developed for the Voting
screen. If there's a winner, we render it instead of the regular Results screen:
</p>

<p>
src/components/Results.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
import Winner from './Winner';
</p>

<p>
export default React.createClass({
  mixins: [PureRenderMixin],
  getPair: function() {
    return this.props.pair || [];
  },
  getVotes: function(entry) {
    if (this.props.tally &amp;&amp; this.props.tally.has(entry)) {
      return this.props.tally.get(entry);
    }
    return 0;
  },
  render: function() {
    return this.props.winner ?
      &lt;Winner ref="winner" winner={this.props.winner} /&gt; :
      &lt;div className="results"&gt;
        &lt;div className="tally"&gt;
          {this.getPair().map(entry <code>&gt;
            &lt;div key={entry} className</code>"entry"&gt;
              &lt;h1&gt;{entry}&lt;/h1&gt;
              &lt;div className="voteCount"&gt;
                {this.getVotes(entry)}
              &lt;/div&gt;
            &lt;/div&gt;
          )}
        &lt;/div&gt;
        &lt;div className="management"&gt;
          &lt;button ref="next"
                   className="next"
                   onClick={this.props.next}&gt;
            Next
          &lt;/button&gt;
        &lt;/div&gt;
      &lt;/div&gt;;
  }
});
</p>

<p>
This component would also benefit from being broken down into smaller ones. Perhaps a Tally component
for displaying the pair of entries. Go ahead and do the refactoring if you feel like it! 
</p>

<p>
And that's pretty much what our simple application will need in terms of UI! The components we've
written don't yet do anything because they're not connected to any real data or actions. It is
remarkable, however, just how far we're able to get without needing any of that. We have been able to
just inject some simple placeholder data to these components and concentrate on the structure of the
UI.
</p>

<p>
Now that we do have the UI though, let's talk about how to make it come alive by connecting its inputs
and outputs to a Redux store.
</p>
</div>
</li></ol>
</li></ol>
</div>
</div>

<div id="outline-container-sec-5-5" class="outline-3">
<h3 id="sec-5-5"><span class="section-number-3">5.5</span> <span class="done DONE">DONE</span> Introducing A Client-Side Redux Store</h3>
<div class="outline-text-3" id="text-5-5">
</div>
<div id="outline-container-sec-5-5-1" class="outline-4">
<h4 id="sec-5-5-1"><span class="section-number-4">5.5.1</span> <span class="done DONE">DONE</span> Introduction</h4>
<div class="outline-text-4" id="text-5-5-1">
<p>
Redux is really designed to be used as the state container for UI applications, exactly like the one
we are in the process of building. We've only used Redux on the server so far though, and discovered
it's actually pretty useful there too! Now we're ready to look at how Redux works with a React
application, which is arguably where it's most commonly used.
</p>

<p>
Just like on the server, we'll begin by thinking about the state of the application. That state is
going to be quite similar to the one on the server, which is not by accident.
</p>

<p>
We have a UI with two screens. On both of them we display the pair of entries that's being voted on.
It would make sense to have a state which included a vote entry with such a pair:
</p>

<p>
In addition to this, the results screen displays the current tally of votes. That should also be in
the vote state:
</p>
</div>
</div>

<div id="outline-container-sec-5-5-2" class="outline-4">
<h4 id="sec-5-5-2"><span class="section-number-4">5.5.2</span> <span class="done DONE">DONE</span> State</h4>
<div class="outline-text-4" id="text-5-5-2">
</div><ol class="org-ol"><li><a id="sec-5-5-2-1" name="sec-5-5-2-1"></a>Voted<br  /><div class="outline-text-5" id="text-5-5-2-1">
<p>
The Voting component renders differently when the user has already voted in the current pair. This is
something that the state also needs to track:
</p>
</div>
</li>

<li><a id="sec-5-5-2-2" name="sec-5-5-2-2"></a>Winner<br  /><div class="outline-text-5" id="text-5-5-2-2">
<p>
When there is a winner, we need that and only that in the state:
</p>
</div>
</li>

<li><a id="sec-5-5-2-3" name="sec-5-5-2-3"></a>hasVoted client side state<br  /><div class="outline-text-5" id="text-5-5-2-3">
<p>
Notice that everything in here is a subset of the server state, except for the hasVoted entry.
</p>
</div>
</li></ol>
</div>

<div id="outline-container-sec-5-5-3" class="outline-4">
<h4 id="sec-5-5-3"><span class="section-number-4">5.5.3</span> <span class="done DONE">DONE</span> Implemantation Details</h4>
<div class="outline-text-4" id="text-5-5-3">
<p>
This brings us to the implementation of the core logic and the actions and reducers that our Redux
Store will use. What should they be?
</p>
</div>

<ol class="org-ol"><li><a id="sec-5-5-3-1" name="sec-5-5-3-1"></a><span class="done DONE">DONE</span> User Actions<br  /><div class="outline-text-5" id="text-5-5-3-1">
<p>
We can think about this in terms of what can happen while the application is running that could cause
the state to change. One source of state changes are the user's actions. We currently have two
possible user interactions built into the UI:
</p>
</div>

<ol class="org-ol"><li><a id="sec-5-5-3-1-1" name="sec-5-5-3-1-1"></a>The user clicks one of the vote buttons on the voting screen.<br  /></li>
<li><a id="sec-5-5-3-1-2" name="sec-5-5-3-1-2"></a>The user click on the Next button on the results screen.<br  /></li>
<li><a id="sec-5-5-3-1-3" name="sec-5-5-3-1-3"></a>Server send us it's current state<br  /><div class="outline-text-6" id="text-5-5-3-1-3">
<p>
Additionally, we know that our server is set up to send us its current state. We will soon be writing
the code for receiving it. That is a third source of state change.
</p>
</div>
<ol class="org-ol"><li><a id="sec-5-5-3-1-3-1" name="sec-5-5-3-1-3-1"></a>Merge the server state<br  /><div class="outline-text-7" id="text-5-5-3-1-3-1">
<p>
We can begin with the server state update, since that is going to be the most straightforward one to
do. Earlier we set the server up to emit a state event, whose payload is almost exactly the shape of
the client-side state trees that we have drawn. This is no coincidence since that's how we designed
it. From the point of view of our client's reducer, it would make sense to have an action that
receives the state snapshot from the server and just merges it into the client state. The action would
look something like this:
</p>

<p>
{
  type: 'SET<sub>STATE'</sub>,
  state: {
    vote: {&#x2026;}
  }
}
</p>
</div>
</li></ol>
</li></ol>
</li>
<li><a id="sec-5-5-3-2" name="sec-5-5-3-2"></a><span class="done DONE">DONE</span> implemantioan Redux to client<br  /><ol class="org-ol"><li><a id="sec-5-5-3-2-1" name="sec-5-5-3-2-1"></a><span class="done DONE">DONE</span> Test SET<sub>STATE</sub><br  /><div class="outline-text-6" id="text-5-5-3-2-1">
<p>
Let's add some unit tests to see how this might work out. We're expecting to have a reducer that,
given an action like the one above, merges its payload into the current state:
</p>

<p>
test/reducer<sub>spec</sub>.js
import {List, Map, fromJS} from 'immutable';
import {expect} from 'chai';
</p>

<p>
import reducer from '../src/reducer';
</p>

<p>
describe('reducer', () =&gt; {
</p>

<p>
it('handles SET<sub>STATE'</sub>, () =&gt; {
  const initialState = Map();
  const action = {
    type: 'SET<sub>STATE'</sub>,
    state: Map({
      vote: Map({
        pair: List.of('Trainspotting', '28 Days Later'),
        tally: Map({Trainspotting: 1})
      })
    })
  };
  const nextState = reducer(initialState, action);
</p>

<p>
  expect(nextState).to.equal(fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    }
  }));
});
</p>

<p>
});
</p>
</div>
</li>

<li><a id="sec-5-5-3-2-2" name="sec-5-5-3-2-2"></a><span class="done DONE">DONE</span> immutable data structure by the time it is returned as the next value:<br  /><div class="outline-text-6" id="text-5-5-3-2-2">

<p>
The reducers should be able to receive plain JavaScript data structure, as opposed to an Immutable
data structure, since that's what actually get from the socket. It should still be turned into an
immutable data structure by the time it is returned as the next value:
</p>

<p>
test/reducer<sub>spec</sub>.js
it('handles SET<sub>STATE</sub> with plain JS payload', () =&gt; {
  const initialState = Map();
  const action = {
    type: 'SET<sub>STATE'</sub>,
    state: {
      vote: {
        pair: ['Trainspotting', '28 Days Later'],
        tally: {Trainspotting: 1}
      }
    }
  };
  const nextState = reducer(initialState, action);
</p>

<p>
  expect(nextState).to.equal(fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    }
  }));
});
</p>
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-5-3-2-3" name="sec-5-5-3-2-3"></a><span class="done DONE">DONE</span> Handle undifined initial state<br  /><div class="outline-text-6" id="text-5-5-3-2-3">
<p>
As part of the reducer contract, an undefined initial state should also be correctly initialized into
an Immutable data structure by the reducer:
</p>

<p>
test/reducer<sub>spec</sub>.js
it('handles SET<sub>STATE</sub> without initial state', () =&gt; {
  const action = {
    type: 'SET<sub>STATE'</sub>,
    state: {
      vote: {
        pair: ['Trainspotting', '28 Days Later'],
        tally: {Trainspotting: 1}
      }
    }
  };
  const nextState = reducer(undefined, action);
</p>

<p>
  expect(nextState).to.equal(fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    }
  }));
});
</p>
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-5-3-2-4" name="sec-5-5-3-2-4"></a><span class="done DONE">DONE</span> Implemanting client side Reducer<br  /><div class="outline-text-6" id="text-5-5-3-2-4">
<p>
That's our spec. Let's see how to fulfill it. We should have a reducer function exported by the
reducer module:
</p>

<p>
src/reducer.js
import {Map} from 'immutable';
</p>

<p>
export default function(state = Map(), action) {
</p>

<p>
  return state;
}
</p>
</div>
</li>
<li><a id="sec-5-5-3-2-5" name="sec-5-5-3-2-5"></a><span class="done DONE">DONE</span> SET<sub>STATE</sub><br  /><div class="outline-text-6" id="text-5-5-3-2-5">
<p>
The reducer should handle the SET<sub>STATE</sub> action. In its handler function we can actually just merge the
given new state to the old state, using the merge function from Map. That makes our tests pass!
</p>

<p>
src/reducer.js
import {Map} from 'immutable';
</p>

<p>
function setState(state, newState) {
  return state.merge(newState);
}
</p>

<p>
export default function(state = Map(), action) {
  switch (action.type) {
  case 'SET<sub>STATE'</sub>:
    return setState(state, action.state);
  }
  return state;
}
</p>

<p>
Notice that here we are not bothering with a "core" module separated from the reducer module. That's
because the logic in our reducer is so simple that it doesn't really warrant one. We're just doing a
merge, whereas on the server we have our whole voting system's logic in there. It might later be more
appropriate to add some separation of concerns in the client as well, if the need arises. 
</p>

<p>
The two remaining causes for state change are the user actions: Voting and clicking "Next". Since
these are both actions that involve server interaction, we'll return to them a bit later, after we've
got the architecture for server communication in place.
</p>
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-5-3-2-6" name="sec-5-5-3-2-6"></a><span class="done DONE">DONE</span> Installation<br  /><div class="outline-text-6" id="text-5-5-3-2-6">
<p>
Now that we have a reducer though, we can spin up a Redux Store from it. Time to add Redux to the
project:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save redux
</pre>
</div>
</div>
</li>

<li><a id="sec-5-5-3-2-7" name="sec-5-5-3-2-7"></a><span class="done DONE">DONE</span> Initialization<br  /><div class="outline-text-6" id="text-5-5-3-2-7">
<p>
The entry point index.jsx is a good place to set up the Store. Let's also kick it off with some state
by dispatching the SET<sub>STATE</sub> action on it (this is only temporary until we get real data in):
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore} from 'redux';
import reducer from './reducer';
import App from './components/App';
import Voting from './components/Voting';
import Results from './components/Results';
</p>

<p>
const store = createStore(reducer);
store.dispatch({
  type: 'SET<sub>STATE'</sub>,
  state: {
    vote: {
      pair: ['Sunshine', '28 Days Later'],
      tally: {Sunshine: 2}
    }
  }
});
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={Results} /&gt;
  &lt;Route path="/" component={Voting} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Router&gt;{routes}&lt;/Router&gt;,
  document.getElementById('app')
);
</p>

<p>
There's our Store. Now, how do we get the data from the Store into the React components?
</p>
</div>
</li></ol>
</li></ol>
</div>
</div>

<div id="outline-container-sec-5-6" class="outline-3">
<h3 id="sec-5-6"><span class="section-number-3">5.6</span> <span class="done DONE">DONE</span> Getting Data In from Redux to React</h3>
<div class="outline-text-3" id="text-5-6">
</div><div id="outline-container-sec-5-6-1" class="outline-4">
<h4 id="sec-5-6-1"><span class="section-number-4">5.6.1</span> Introduction</h4>
<div class="outline-text-4" id="text-5-6-1">
<p>
We have a Redux Store that holds our immutable application state. We have stateless React components
that take immutable data as inputs. The two would be a great fit: If we can figure out a way to always
get the latest data from the Store to the components, that would be perfect. React would re-render
when the state changes, and the pure render mixin would make sure that the parts of the UI that have
no need to re-render won't be.
</p>
</div>
</div>
<div id="outline-container-sec-5-6-2" class="outline-4">
<h4 id="sec-5-6-2"><span class="section-number-4">5.6.2</span> Init</h4>
<div class="outline-text-4" id="text-5-6-2">
<p>
Rather than writing such synchronization code ourselves, we can make use of the Redux React bindings
that are available in the react-redux package:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save react-redux
</pre>
</div>


<p>
The big idea of react-redux is to take our pure components and wire them up into a Redux Store by
doing two things:
</p>
</div>

<ol class="org-ol"><li><a id="sec-5-6-2-1" name="sec-5-6-2-1"></a>Mapping the Store state into component input props.<br  /></li>
<li><a id="sec-5-6-2-2" name="sec-5-6-2-2"></a>Mapping actions into component output callback props.<br  /></li></ol>
</div>
<div id="outline-container-sec-5-6-3" class="outline-4">
<h4 id="sec-5-6-3"><span class="section-number-4">5.6.3</span> react-redux provider</h4>
<div class="outline-text-4" id="text-5-6-3">
</div>
<ol class="org-ol"><li><a id="sec-5-6-3-1" name="sec-5-6-3-1"></a><span class="done DONE">DONE</span> Init<br  /><div class="outline-text-5" id="text-5-6-3-1">
<p>
Before any of this is possible, we need to wrap our top-level application component inside a
react-redux Provider component. This connects our component tree to a Redux store, enabling us to make
the mappings for individual components later.
</p>

<p>
We'll put in the Provider around the Router component. That'll cause the Provider to be an ancestor to
all of our application components:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore} from 'redux';
import {Provider} from 'react-redux';
import reducer from './reducer';
import App from './components/App';
import {VotingContainer} from './components/Voting';
import Results from './components/Results';
</p>

<p>
const store = createStore(reducer);
store.dispatch({
  type: 'SET<sub>STATE'</sub>,
  state: {
    vote: {
      pair: ['Sunshine', '28 Days Later'],
      tally: {Sunshine: 2}
    }
  }
});
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={Results} /&gt;
  &lt;Route path="/" component={VotingContainer} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Provider store={store}&gt;
    &lt;Router&gt;{routes}&lt;/Router&gt;
  &lt;/Provider&gt;,
  document.getElementById('app')
);
</p>

<p>
});
</p>

<p>
 
</p>

<p>
Next, we should think about which of our components need to be "wired up" so that all the data will
come from the Store. We have five component, which we can divide in three categories:
</p>
</div>
</li>

<li><a id="sec-5-6-3-2" name="sec-5-6-3-2"></a><span class="done DONE">DONE</span> The root component App doesn't really need anything since it doesn't use any data.<br  /></li>
<li><a id="sec-5-6-3-3" name="sec-5-6-3-3"></a>Vote and Winner are only used by parent components that give them all the props they need.<br  /><div class="outline-text-5" id="text-5-6-3-3">
<p>
They don't need wiring up either. 
</p>
</div>
</li>
<li><a id="sec-5-6-3-4" name="sec-5-6-3-4"></a>What's left are the components we use in routes: Voting and Results.<br  /><div class="outline-text-5" id="text-5-6-3-4">
<p>
They are currently getting data
in as hardcoded placeholder props from App. These are the components that need to be wired up to the
Store. 
</p>

<p>
Let's begin with the Voting component. With react-redux we get a function called connect that can do
the wiring-up of a component. It takes a mapping function as an argument and returns another function
that takes a React component class:
</p>

<p>
connect(mapStateToProps)(SomeComponent);
</p>
</div>
</li>
<li><a id="sec-5-6-3-5" name="sec-5-6-3-5"></a><span class="todo TEST">TEST</span> Connect Voting Containter to store<br  /><div class="outline-text-5" id="text-5-6-3-5">
<p>
The role of the mapping function is to map the state from the Redux Store into an object of props.
Those props will then be merged into the props of the component that's being connected. In the case of
Voting, we just need to map the pair and winner from the state:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin'
import {connect} from 'react-redux';
import Winner from './Winner';
import Vote from './Vote';
</p>

<p>
const Voting = React.createClass({
  mixins: [PureRenderMixin],
  render: function() {
    return &lt;div&gt;
      {this.props.winner ?
        &lt;Winner ref="winner" winner={this.props.winner} /&gt; :
        &lt;Vote {&#x2026;this.props} /&gt;}
    &lt;/div&gt;;
  }
});
</p>

<p>
function mapStateToProps(state) {
  return {
    pair: state.getIn(['vote', 'pair']),
    winner: state.get('winner')
  };
}
</p>

<p>
connect(mapStateToProps)(Voting);
</p>

<p>
export default Voting;
</p>
</div>
</li>
<li><a id="sec-5-6-3-6" name="sec-5-6-3-6"></a><span class="todo TEST">TEST</span> Export the VotingContainer<br  /><div class="outline-text-5" id="text-5-6-3-6">
<p>
This isn't quite right though. True to functional style, the connect function doesn't actually go and
mutate the Voting component. Voting remains a pure, unconnected component. Instead, connect returns a
connected version of Voting. That means our current code isn't really doing anything. We need to grab
that return value, which we'll call VotingContainer:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
import {connect} from 'react-redux';
import Winner from './Winner';
import Vote from './Vote';
</p>

<p>
export const Voting = React.createClass({
  mixins: [PureRenderMixin],
  render: function() {
    return &lt;div&gt;
      {this.props.winner ?
        &lt;Winner ref="winner" winner={this.props.winner} /&gt; :
        &lt;Vote {&#x2026;this.props} /&gt;}
    &lt;/div&gt;;
  }
});
</p>

<p>
function mapStateToProps(state) {
  return {
    pair: state.getIn(['vote', 'pair']),
    winner: state.get('winner')
  };
}
</p>

<p>
export const VotingContainer = connect(mapStateToProps)(Voting);
</p>

<p>
The module now exports two components: The pure component Voting and the connected component
VotingContainer. The react-redux documentation calls the former a "dumb" component and the latter a
"smart" component. I prefer "pure" and "connected". Call them what you will, understanding the
difference is key:
</p>
</div>
</li>

<li><a id="sec-5-6-3-7" name="sec-5-6-3-7"></a>The pure/dumb component is fully driven by the props it is given.<br  /><div class="outline-text-5" id="text-5-6-3-7">
<p>
It is the component equivalent of a pure function. 
</p>
</div>
</li>
<li><a id="sec-5-6-3-8" name="sec-5-6-3-8"></a><span class="todo TODAY">TODAY</span> The connected/smart component.<br  /><div class="outline-text-5" id="text-5-6-3-8">
<p>
on the other hand, wraps the pure version with some logic that will
keep it in sync with the changing state of the Redux Store. That logic is provided by react-redux. 
</p>
</div>
</li>
<li><a id="sec-5-6-3-9" name="sec-5-6-3-9"></a><span class="todo TEST">TEST</span> Update Routing table<br  /><div class="outline-text-5" id="text-5-6-3-9">
<p>
We should update our routing table, so that it uses VotingContainer instead of Voting. Once we've done
that, the voting screen will come alive with the data we've put in the Redux store:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore} from 'redux';
import {Provider} from 'react-redux';
import reducer from './reducer';
import App from './components/App';
import {VotingContainer} from './components/Voting';
import Results from './components/Results';
</p>

<p>
const store = createStore(reducer);
store.dispatch({
  type: 'SET<sub>STATE'</sub>,
  state: {
    vote: {
      pair: ['Sunshine', '28 Days Later'],
      tally: {Sunshine: 2}
    }
  }
});
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={Results} /&gt;
  &lt;Route path="/" component={VotingContainer} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Provider store={store}&gt;
    &lt;Router&gt;{routes}&lt;/Router&gt;
  &lt;/Provider&gt;,
  document.getElementById('app')
);
</p>


<p>
 
</p>
</div>
</li>
<li><a id="sec-5-6-3-10" name="sec-5-6-3-10"></a><span class="done DONE">DONE</span> Unit tests<br  /><div class="outline-text-5" id="text-5-6-3-10">
<p>
In the unit tests for Voting we need to change the way the import is done, as we no longer have Voting
as the default export:
</p>

<p>
test/components/Voting<sub>spec</sub>.jsx
import React from 'react/addons';
import {List} from 'immutable';
import {Voting} from '../../src/components/Voting';
import {expect} from 'chai';
</p>

<p>
No other changes are needed for tests. They are written for the pure Voting component, and it isn't
changed in any way. We've just added a wrapper for it that connects it to a Redux store.
</p>

<p>
Now we should just apply the same trick for the Results screen. It also needs the pair and winner
attributes of the state. Additionally it needs tally, in order to show the vote counts:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li>

<li><a id="sec-5-6-3-11" name="sec-5-6-3-11"></a><span class="todo TEST">TEST</span> Connect Result componant<br  /><div class="outline-text-5" id="text-5-6-3-11">
<p>
src/components/Results.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
import {connect} from 'react-redux';
import Winner from './Winner';
</p>

<p>
export const Results = React.createClass({
  mixins: [PureRenderMixin],
  getPair: function() {
    return this.props.pair || [];
  },
  getVotes: function(entry) {
    if (this.props.tally &amp;&amp; this.props.tally.has(entry)) {
      return this.props.tally.get(entry);
    }
    return 0;
  },
  render: function() {
    return this.props.winner ?
      &lt;Winner ref="winner" winner={this.props.winner} /&gt; :
      &lt;div className="results"&gt;
        &lt;div className="tally"&gt;
          {this.getPair().map(entry <code>&gt;
            &lt;div key={entry} className</code>"entry"&gt;
              &lt;h1&gt;{entry}&lt;/h1&gt;
              &lt;div className="voteCount"&gt;
                {this.getVotes(entry)}
              &lt;/div&gt;
            &lt;/div&gt;
          )}
        &lt;/div&gt;
        &lt;div className="management"&gt;
          &lt;button ref="next"
                   className="next"
                   onClick={this.props.next}&gt;
            Next
          &lt;/button&gt;
      &lt;/div&gt;
      &lt;/div&gt;;
  }
});
</p>

<p>
function mapStateToProps(state) {
  return {
    pair: state.getIn(['vote', 'pair']),
    tally: state.getIn(['vote', 'tally']),
    winner: state.get('winner')
  }
}
</p>

<p>
export const ResultsContainer = connect(mapStateToProps)(Results);
</p>
</div>
</li>
<li><a id="sec-5-6-3-12" name="sec-5-6-3-12"></a><span class="todo TEST">TEST</span> Init ResultsContainer<br  /><div class="outline-text-5" id="text-5-6-3-12">
<p>
In index.jsx we should change the results route to then use ResultsContainer instead of Results:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore} from 'redux';
import {Provider} from 'react-redux';
import reducer from './reducer';
import App from './components/App';
import {VotingContainer} from './components/Voting';
import {ResultsContainer} from './components/Results';
</p>

<p>
const store = createStore(reducer);
store.dispatch({
  type: 'SET<sub>STATE'</sub>,
  state: {
    vote: {
      pair: ['Sunshine', '28 Days Later'],
      tally: {Sunshine: 2}
    }
  }
});
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={ResultsContainer} /&gt;
  &lt;Route path="/" component={VotingContainer} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Provider store={store}&gt;
    &lt;Router&gt;{routes}&lt;/Router&gt;
  &lt;/Provider&gt;,
  document.getElementById('app')
);
</p>
</div>
</li>

<li><a id="sec-5-6-3-13" name="sec-5-6-3-13"></a><span class="todo TEST">TEST</span> Unit testing Result Container   <br  /><div class="outline-text-5" id="text-5-6-3-13">
<p>
Finally, in the Results test we should update the import statement to use the named export for
Results:
</p>

<p>
test/components/Results<sub>spec</sub>.jsx
import React from 'react/addons';
import {List, Map} from 'immutable';
import {Results} from '../../src/components/Results';
import {expect} from 'chai';
</p>
</div>
</li>

<li><a id="sec-5-6-3-14" name="sec-5-6-3-14"></a><span class="todo TODAY">TODAY</span> talks<br  /><div class="outline-text-5" id="text-5-6-3-14">
<p>
And that's how you can connect pure React components to a Redux store, so that they get their data in
from the store.
</p>

<p>
For very small apps that just have a single root component and no routing, connecting the root
component will be enough in most cases. The root can then just propagate the data to its children as
props. For apps with routing, such as the one we're making, connecting each of the router's components
is usually a good idea. But any component can be separately connected, so different strategies can be
used for different app architectures. I think it's a good idea to use plain props whenever you can,
because with props it is easy to see what data is going in and it is also less work since you don't
need to manage the "wiring" code.
</p>
</div>
</li>
<li><a id="sec-5-6-3-15" name="sec-5-6-3-15"></a><span class="todo TEST">TEST</span> Removing Hardcoded Props<br  /><div class="outline-text-5" id="text-5-6-3-15">
<p>
Now that we've got the Redux data in our UI, we no longer need the hardcoded props in App.jsx, so it
becomes even simpler than before:
</p>

<p>
src/components/App.jsx
import React from 'react';
</p>

<p>
export default React.createClass({
  render: function() {
    return this.props.children;
  }
});
</p>

<p>
 
</p>
</div>
</li></ol>
</div>
</div>

<div id="outline-container-sec-5-7" class="outline-3">
<h3 id="sec-5-7"><span class="section-number-3">5.7</span> <span class="done DONE">DONE</span> Setting Up The Socket.io Client</h3>
<div class="outline-text-3" id="text-5-7">

<p>
Now that we have a Redux app going in the client, we can talk about how we can connect it to the other
Redux app we have running on the server. The two currently reside in their own universes, with no
connection between them whatsoever.
</p>

<p>
The server is already prepared to take incoming socket connections and emit the voting state to them.
The client, on the other hand, has a Redux store into which we could easily dispatch incoming data.
All we need to do is to draw the connection.
</p>

<p>
This begins by getting the infrastructure in place. We need a way to make a Socket.io connection from
the browser to the server. For that purpose we can use the socket.io-client library, which is the
client-side equivalent to the socket.io library that we used on the server:
</p>
<div class="org-src-container">

<pre class="src src-sh">npm install --save socket.io-client
</pre>
</div>


<p>
Importing this library gives us an io function that can be used to connect to a Socket.io server.
Let's connect to one that we assume to be on the same host as our client, in port 8090 (matching the
port we used on the server):
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore} from 'redux';
import {Provider} from 'react-redux';
import io from 'socket.io-client';
import reducer from './reducer';
import App from './components/App';
import {VotingContainer} from './components/Voting';
import {ResultsContainer} from './components/Results';
</p>

<p>
const store = createStore(reducer);
store.dispatch({
  type: 'SET<sub>STATE'</sub>,
  state: {
    vote: {
      pair: ['Sunshine', '28 Days Later'],
      tally: {Sunshine: 2}
    }
  }
});
</p>

<p>
const socket = io(`${location.protocol}//${location.hostname}:8090`);
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={ResultsContainer} /&gt;
  &lt;Route path="/" component={VotingContainer} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Provider store={store}&gt;
    &lt;Router&gt;{routes}&lt;/Router&gt;
  &lt;/Provider&gt;,
  document.getElementById('app')
);
</p>


<p>
 
</p>

<p>
If you now make sure you have the server running, open the client app in a browser and inspect the
network traffic, you should see it make a WebSocket connection and start transmitting Socket.io
heartbeats on it.
</p>

<p>
During development there will actually be two Socket.io connections on the page. One is ours and the
other is supporting Webpack's hot reloading. 
</p>
</div>
</div>

<div id="outline-container-sec-5-8" class="outline-3">
<h3 id="sec-5-8"><span class="section-number-3">5.8</span> <span class="done DONE">DONE</span> Receiving Actions From The Server</h3>
<div class="outline-text-3" id="text-5-8">
<p>
Given that we now have a Socket.io connection, there's actually not much we need to do to get data in
from it. The server is sending us state events - once when we connect and then every time something
changes. We just need to listen to those events. When we get one, we can simply dispatch a SET<sub>STATE</sub>
action to our Store. We already have a reducer that will handle it:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore} from 'redux';
import {Provider} from 'react-redux';
import io from 'socket.io-client';
import reducer from './reducer';
import App from './components/App';
import {VotingContainer} from './components/Voting';
import {ResultsContainer} from './components/Results';
</p>

<p>
const store = createStore(reducer);
</p>

<p>
const socket = io(`${location.protocol}//${location.hostname}:8090`);
socket.on('state', state =&gt;
  store.dispatch({type: 'SET<sub>STATE'</sub>, state})
);
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={ResultsContainer} /&gt;
  &lt;Route path="/" component={VotingContainer} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Provider store={store}&gt;
    &lt;Router&gt;{routes}&lt;/Router&gt;
  &lt;/Provider&gt;,
  document.getElementById('app')
);
</p>


<p>
 
</p>

<p>
Note that we've removed the hardcoded SET<sub>STATE</sub> dispatch. We no longer need it because the server will
give us the real state.
</p>

<p>
Looking at the UI - either the voting or the results one - will now show the first pair of entries, as
defined by the server. Our server and client are connected!
</p>
</div>
</div>

<div id="outline-container-sec-5-9" class="outline-3">
<h3 id="sec-5-9"><span class="section-number-3">5.9</span> <span class="todo TODAY">TODAY</span> Dispatching Actions From React Components</h3>
<div class="outline-text-3" id="text-5-9">
</div>
<div id="outline-container-sec-5-9-1" class="outline-4">
<h4 id="sec-5-9-1"><span class="section-number-4">5.9.1</span> Introduction</h4>
<div class="outline-text-4" id="text-5-9-1">
<p>
We know how to get data in from the Redux Store to the UI. Let's discuss how we can get actions out
from the UI.
</p>
</div>
</div>
<div id="outline-container-sec-5-9-2" class="outline-4">
<h4 id="sec-5-9-2"><span class="section-number-4">5.9.2</span> <span class="todo TODAY">TODAY</span> Dispatching voting buttons</h4>
<div class="outline-text-4" id="text-5-9-2">
</div><ol class="org-ol"><li><a id="sec-5-9-2-1" name="sec-5-9-2-1"></a>INTRODUCTION<br  /><div class="outline-text-5" id="text-5-9-2-1">
<p>
The best place for us to start thinking about this is the voting buttons. When we were building the
UI, we assumed that the Voting component will receive a vote prop whose value is a callback function.
The component invokes that function when the user clicks on one of the buttons. But we haven't
actually supplied the callback yet - except in unit tests.
</p>

<p>
What should actually happen when a user votes on something? Well, the vote should probably be sent to
the server, and that's something we'll discuss a bit later, but there's also client-side logic
involved: The hasVoted prop should be set on the component, so that the user can't vote for the same
pair again.
</p>
</div>
</li>
<li><a id="sec-5-9-2-2" name="sec-5-9-2-2"></a><span class="done DONE">DONE</span> Prepare Unit test for hasVoted<br  /><ol class="org-ol"><li><a id="sec-5-9-2-2-1" name="sec-5-9-2-2-1"></a><span class="todo TEST">TEST</span> U1<br  /><div class="outline-text-6" id="text-5-9-2-2-1">
<p>
This will be the second client-side Redux action we have, after SET<sub>STATE</sub>. We can call it VOTE. It
should populate a hasVoted entry in the state Map:
</p>

<p>
test/reducer<sub>spec</sub>.js
it('handles VOTE by setting hasVoted', () =&gt; {
  const state = fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    }
  });
  const action = {type: 'VOTE', entry: 'Trainspotting'};
  const nextState = reducer(state, action);
</p>

<p>
  expect(nextState).to.equal(fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    },
    hasVoted: 'Trainspotting'
  }));
});
</p>
</div>
</li>

<li><a id="sec-5-9-2-2-2" name="sec-5-9-2-2-2"></a><span class="todo TEST">TEST</span> U2<br  /><div class="outline-text-6" id="text-5-9-2-2-2">
<p>
It might also be a good idea to not set that entry if, for any reason, a VOTE action is coming in for
an entry that's not under vote at the moment:
</p>

<p>
test/reducer<sub>spec</sub>.js
it('does not set hasVoted for VOTE on invalid entry', () =&gt; {
  const state = fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    }
  });
  const action = {type: 'VOTE', entry: 'Sunshine'};
  const nextState = reducer(state, action);
</p>

<p>
  expect(nextState).to.equal(fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    }
  }));
});
</p>
</div>
</li></ol>
</li>
<li><a id="sec-5-9-2-3" name="sec-5-9-2-3"></a><span class="done DONE">DONE</span> Code in reducer<br  /><div class="outline-text-5" id="text-5-9-2-3">
<p>
Here's the reducer extension that'll do the trick:
</p>

<p>
src/reducer.js
import {Map} from 'immutable';
</p>

<p>
function setState(state, newState) {
  return state.merge(newState);
}
</p>

<p>
function vote(state, entry) {
  const currentPair = state.getIn(['vote', 'pair']);
  if (currentPair &amp;&amp; currentPair.includes(entry)) {
    return state.set('hasVoted', entry);
  } else {
    return state;
  }
}
</p>

<p>
export default function(state = Map(), action) {
  switch (action.type) {
  case 'SET<sub>STATE'</sub>:
    return setState(state, action.state);
  case 'VOTE':
    return vote(state, action.entry);
  }
  return state;
}
</p>
</div>
</li>
<li><a id="sec-5-9-2-4" name="sec-5-9-2-4"></a><span class="done DONE">DONE</span> Re-set HASVOTED<br  /><div class="outline-text-5" id="text-5-9-2-4">
<p>
The hasVoted entry should not remain in the state forever. It should be re-set when the vote moves on
to the next pair, so that the user can vote on that one. We should handle this in SET<sub>STATE</sub>, where we
can check if the pair in the new state contains the entry the user has voted on. If it doesn't, we
should erase the hasVoted entry:
</p>

<p>
test/reducer<sub>spec</sub>.js
it('removes hasVoted on SET<sub>STATE</sub> if pair changes', () =&gt; {
  const initialState = fromJS({
    vote: {
      pair: ['Trainspotting', '28 Days Later'],
      tally: {Trainspotting: 1}
    },
    hasVoted: 'Trainspotting'
  });
  const action = {
    type: 'SET<sub>STATE'</sub>,
    state: {
      vote: {
        pair: ['Sunshine', 'Slumdog Millionaire']
      }
    }
  };
  const nextState = reducer(initialState, action);
</p>

<p>
  expect(nextState).to.equal(fromJS({
    vote: {
      pair: ['Sunshine', 'Slumdog Millionaire']
    }
  }));
});
</p>

<p>
We can implement this by composing another function, called resetVote on the SET<sub>STATE</sub> action handler:
</p>

<p>
src/reducer.js
import {List, Map} from 'immutable';
</p>

<p>
function setState(state, newState) {
  return state.merge(newState);
}
</p>

<p>
function vote(state, entry) {
  const currentPair = state.getIn(['vote', 'pair']);
  if (currentPair &amp;&amp; currentPair.includes(entry)) {
    return state.set('hasVoted', entry);
  } else {
    return state;
  }
}
</p>

<p>
function resetVote(state) {
  const hasVoted = state.get('hasVoted');
  const currentPair = state.getIn(['vote', 'pair'], List());
  if (hasVoted &amp;&amp; !currentPair.includes(hasVoted)) {
    return state.remove('hasVoted');
  } else {
    return state;
  }
}
</p>

<p>
export default function(state = Map(), action) {
  switch (action.type) {
  case 'SET<sub>STATE'</sub>:
    return resetVote(setState(state, action.state));
  case 'VOTE':
    return vote(state, action.entry);
  }
  return state;
}
</p>

<p>
This logic for determining whether the hasVoted entry is for the current pair is slightly problematic.
See the exercises for a way to improve it. 
</p>
</div>
</li>

<li><a id="sec-5-9-2-5" name="sec-5-9-2-5"></a><span class="done DONE">DONE</span> Connecting the hasVoted entry to the props on Voting<br  /><div class="outline-text-5" id="text-5-9-2-5">
<p>
src/components/Voting.jsx
function mapStateToProps(state) {
  return {
    pair: state.getIn(['vote', 'pair']),
    hasVoted: state.get('hasVoted'),
    winner: state.get('winner')
  };
}
</p>

<p>
Now we still need a way to give a vote callback to Voting, which will cause this new action to be
dispatched. We should keep Voting itself pure and unaware of actions or Redux. Instead, this is
another job for the connect function from react-redux.
</p>
</div>
</li>
<li><a id="sec-5-9-2-6" name="sec-5-9-2-6"></a><span class="done DONE">DONE</span> Test Results<br  /><div class="outline-text-5" id="text-5-9-2-6">
<div class="org-src-container">

<pre class="src src-sh">npm run test
</pre>
</div>
</div>
</li></ol>
</div>

<div id="outline-container-sec-5-9-3" class="outline-4">
<h4 id="sec-5-9-3"><span class="section-number-4">5.9.3</span> <span class="done DONE">DONE</span> Action Createtor</h4>
<div class="outline-text-4" id="text-5-9-3">

<p>
In addition to wiring up input props, react-redux can be used to wire up output actions. Before we can
do that though, we need to introduce another core Redux concept: Action creators.
</p>

<p>
As we have seen, Redux actions are just simple objects that (by convention) have a type attribute and
other, action-specific data. We have been creating these actions whenever needed by simply using
object literals. It is preferable, however, to use little factory functions for making actions
instead. Functions such as this one:
</p>

<p>
function vote(entry) {
  return {type: 'VOTE', entry};
}
</p>
</div>

<ol class="org-ol"><li><a id="sec-5-9-3-1" name="sec-5-9-3-1"></a><span class="done DONE">DONE</span> Action Creators<br  /><div class="outline-text-5" id="text-5-9-3-1">
<p>
These functions are called action creators. There's really not much to them - they are pure functions
that just return action objects - but what they do is encapsulate the internal structure of the action
objects so that the rest of your codebase doesn't need to be concerned with that. Actions creators
also conveniently document all the actions that can be dispatched in a given application. That
information would be more difficult to gather if it was sprinkled all over the codebase in object
literals.
</p>

<p>
Let's create a new file that defines the action creators for our two existing client-side actions:
</p>

<p>
src/action<sub>creators</sub>.js
export function setState(state) {
  return {
    type: 'SET<sub>STATE'</sub>,
    state
  };
}
</p>

<p>
export function vote(entry) {
  return {
    type: 'VOTE',
    entry
  };
}
</p>

<p>
We could also very easily write unit tests for these functions, but I usually don't bother with that
unless an action creator actually does something more than just returns an object. Feel free to add
the unit tests, however, if you consider them useful! 
</p>
</div>
</li>
<li><a id="sec-5-9-3-2" name="sec-5-9-3-2"></a><span class="done DONE">DONE</span> Applying<br  /><div class="outline-text-5" id="text-5-9-3-2">
<p>
In index.jsx we can now use the setState action creator in the Socket.io event handler:
</p>

<p>
src/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore} from 'redux';
import {Provider} from 'react-redux';
import io from 'socket.io-client';
import reducer from './reducer';
import {setState} from './action<sub>creators'</sub>;
import App from './components/App';
import {VotingContainer} from './components/Voting';
import {ResultsContainer} from './components/Results';
</p>

<p>
const store = createStore(reducer);
</p>

<p>
const socket = io(`${location.protocol}//${location.hostname}:8090`);
socket.on('state', state =&gt;
  store.dispatch(setState(state))
);
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={ResultsContainer} /&gt;
  &lt;Route path="/" component={VotingContainer} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Provider store={store}&gt;
    &lt;Router&gt;{routes}&lt;/Router&gt;
  &lt;/Provider&gt;,
  document.getElementById('app')
);
</p>
</div>
</li>

<li><a id="sec-5-9-3-3" name="sec-5-9-3-3"></a><span class="done DONE">DONE</span> Action Creator in action<br  /><div class="outline-text-5" id="text-5-9-3-3">
<p>
A really neat thing about action creators is the way react-redux can connect them to React components:
We have a vote callback prop on Voting, and a vote action creator. Both have the same name and the
same function signature: A single argument, which is the entry being voted. What we can do is simply
give our action creators to the react-redux connect function as the second argument, and the
connection will be made:
</p>

<p>
src/components/Voting.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
import {connect} from 'react-redux';
import Winner from './Winner';
import Vote from './Vote';
import * as actionCreators from '../action<sub>creators'</sub>;
</p>

<p>
export const Voting = React.createClass({
  mixins: [PureRenderMixin],
  render: function() {
    return &lt;div&gt;
      {this.props.winner ?
        &lt;Winner ref="winner" winner={this.props.winner} /&gt; :
        &lt;Vote {&#x2026;this.props} /&gt;}
    &lt;/div&gt;;
  }
});
</p>

<p>
function mapStateToProps(state) {
  return {
    pair: state.getIn(['vote', 'pair']),
    hasVoted: state.get('hasVoted'),
    winner: state.get('winner')
  };
}
</p>

<p>
export const VotingContainer = connect(
  mapStateToProps,
  actionCreators
)(Voting);
</p>

<p>
The effect of this is that a vote prop will be given to Voting. That prop is a function that creates
an action using the vote action creator, and also dispatches that action to the Redux Store. Thus,
clicking a vote button now dispatches an action! You should be able to see the effects in the browser
immediately: When you vote on something, the buttons will become disabled.
</p>
</div>
</li></ol>
</div>
</div>

<div id="outline-container-sec-5-10" class="outline-3">
<h3 id="sec-5-10"><span class="section-number-3">5.10</span> <span class="todo TODAY">TODAY</span> Sending Actions To The Server Using Redux Middleware</h3>
<div class="outline-text-3" id="text-5-10">

<p>
The final aspect of our application that we need to address is getting the results of the user's
actions to the server. This should happen when the user votes on something, as well as when the vote
manager hits the Next button on the result screen.
</p>

<p>
Let's begin by discussing Voting. Here's an inventory of what we already have in place:
</p>
</div>

<div id="outline-container-sec-5-10-1" class="outline-4">
<h4 id="sec-5-10-1"><span class="section-number-4">5.10.1</span> A VOTE action is created and dispatched to the client-side Redux Store when the user votes.</h4>
</div>
<div id="outline-container-sec-5-10-2" class="outline-4">
<h4 id="sec-5-10-2"><span class="section-number-4">5.10.2</span> VOTE actions are handled by the client-side reducer by setting the hasVoted state.</h4>
</div>
<div id="outline-container-sec-5-10-3" class="outline-4">
<h4 id="sec-5-10-3"><span class="section-number-4">5.10.3</span> The server is ready to receive actions from clients via the action Socket.io event. It dispatches</h4>
<div class="outline-text-4" id="text-5-10-3">
<p>
all received actions to the serverside Redux Store. 
</p>
</div>
</div>
<div id="outline-container-sec-5-10-4" class="outline-4">
<h4 id="sec-5-10-4"><span class="section-number-4">5.10.4</span> VOTE actions are handled by the serverside reducer by registering the vote and updating the tally.</h4>
<div class="outline-text-4" id="text-5-10-4">
<p>
It would seem like we actually have almost everything we need! All that is missing is the actual
sending of the client-side VOTE action to the server, so that it would be dispatched to both of the
Redux stores. That's what we'll do next.
</p>

<p>
How should we approach this? There's nothing built into Redux for this purpose, since supporting a
distributed system like ours isn't really part of its core functionality. It is left to us to decide
where and how we send client-side actions to the server.
</p>

<p>
What Redux does provide is a generic way to tap into actions that are being dispatched to Redux
stores: Middleware.
</p>
</div>
</div>
<div id="outline-container-sec-5-10-5" class="outline-4">
<h4 id="sec-5-10-5"><span class="section-number-4">5.10.5</span> Middleware</h4>
<div class="outline-text-4" id="text-5-10-5">
</div><ol class="org-ol"><li><a id="sec-5-10-5-1" name="sec-5-10-5-1"></a>Defination<br  /><div class="outline-text-5" id="text-5-10-5-1">
<p>
A Redux middleware is a function that gets invoked when an action is dispatched, before the action
hits the reducer and the store itself. Middleware can be used for all kinds of things, from logging
and exception handling to modifying actions, caching results, or even changing how or when the action
will reach the store. What we are going to use them for is sending client-side actions to the server.
</p>

<p>
Note the difference between Redux middleware and Redux listeners: Middleware are called before an
action hits the store, and they may affect what happens to the action. Listeners are called after an
action has been dispatched, and they can't really do anything about it. Different tools for different
purposes. 
</p>
</div>
<ol class="org-ol"><li><a id="sec-5-10-5-1-1" name="sec-5-10-5-1-1"></a><span class="todo TEST">TEST</span> outbound socket io Middleware<br  /><div class="outline-text-6" id="text-5-10-5-1-1">
<p>
What we're going to do is create a "remote action middleware" that causes an action to be dispatched
not only to the original store, but also to a remote store using a Socket.io connection.
</p>

<p>
Let's set up the skeleton for this middleware. It is a function that takes a Redux store, and returns
another function that takes a "next" callback. That function returns a third function that takes a
Redux action. The innermost function is where the middleware implementation will actually go:
</p>

<p>
src/remote<sub>action</sub><sub>middleware</sub>.js
export default store =&gt; next =&gt; action =&gt; {
</p>

<p>
}
</p>

<p>
The code above may look a bit foreign but it's really just a more concise way of expressing this:
</p>

<p>
export default function(store) {
  return function(next) {
    return function(action) {
</p>

<p>
    }
  }
}
</p>

<p>
This style of nesting single-argument functions is called currying. In this case it's used so that the
Middleware is easily configurable: If we had all the arguments in just one function (function(store,
next, action) { }) we'd also have to supply all the arguments every time the middleware is used. With
the curried version we can call the outermost function once, and get a return value that "remembers"
which store to use. The same goes for the next argument.
</p>

<p>
The next argument is a callback that the middleware should call when it has done its work and the
action should be sent to the store (or the next middleware):
</p>

<p>
src/remote<sub>action</sub><sub>middleware</sub>.js
export default store =&gt; next =&gt; action =&gt; {
  return next(action);
}
</p>

<p>
The middleware could also decide not to call next, if it decided that the action should be halted. In
that case it would never go into the reducer or the store. 
</p>
</div>
</li></ol>
</li>

<li><a id="sec-5-10-5-2" name="sec-5-10-5-2"></a><span class="todo TEST">TEST</span> Applly log in middleware<br  /><div class="outline-text-5" id="text-5-10-5-2">
<p>
Let's just log something in this middleware so that we'll be able to see when it's called:
</p>

<p>
src/remote<sub>action</sub><sub>middleware</sub>.js
export default store =&gt; next =&gt; action =&gt; {
  console.log('in middleware', action);
  return next(action);
}
</p>

<p>
If we now plug in this middleware to our Redux store, we should see all actions being logged. The
middleware can be activated using an applyMiddleware function that Redux ships with. It takes the
middleware we want to register, and returns a function that takes the createStore function. That
second function will then create a store for us that has the middleware included in it:
</p>

<p>
src/components/index.jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Router, {Route} from 'react-router';
import {createStore, applyMiddleware} from 'redux';
import {Provider} from 'react-redux';
import io from 'socket.io-client';
import reducer from './reducer';
import {setState} from './action<sub>creators'</sub>;
import remoteActionMiddleware from './remote<sub>action</sub><sub>middleware'</sub>;
import App from './components/App';
import {VotingContainer} from './components/Voting';
import {ResultsContainer} from './components/Results';
</p>

<p>
const createStoreWithMiddleware = applyMiddleware(
  remoteActionMiddleware
)(createStore);
const store = createStoreWithMiddleware(reducer);
</p>

<p>
const socket = io(`${location.protocol}//${location.hostname}:8090`);
socket.on('state', state =&gt;
  store.dispatch(setState(state))
);
</p>

<p>
const routes = &lt;Route component={App}&gt;
  &lt;Route path="/results" component={ResultsContainer} /&gt;
  &lt;Route path="/" component={VotingContainer} /&gt;
&lt;/Route&gt;;
</p>

<p>
ReactDOM.render(
  &lt;Provider store={store}&gt;
    &lt;Router&gt;{routes}&lt;/Router&gt;
  &lt;/Provider&gt;,
  document.getElementById('app')
);
</p>

<p>
This is another instance of the curried style of configuring things that we just discussed. Redux APIs
use it quite heavily. 
</p>


<p>
 
</p>
</div>
</li>
<li><a id="sec-5-10-5-3" name="sec-5-10-5-3"></a><span class="todo TEST">TEST</span> Passing socket io to middleware<br  /><div class="outline-text-5" id="text-5-10-5-3">
<p>
If you now reload the app, you'll see the middleware logging the actions that occur: Once for the
initial SET<sub>STATE</sub>, and again for the VOTE action from voting.
</p>

<p>
What this middleware should actually do is send a given action to a Socket.io connection, in addition
to giving it to the next middleware. Before it can do that, it needs the connection to send it to. We
already have a connection in index.jsx - we just need the middleware to have access to it too. That's
easily accomplished by using currying once more in the middleware definition. The outermost function
should take a Socket.io socket:
</p>

<p>
src/remote<sub>action</sub><sub>middleware</sub>.js
export default socket =&gt; store =&gt; next =&gt; action =&gt; {
  console.log('in middleware', action);
  return next(action);
}
</p>

<p>
Now we can pass in the socket from index.jsx:
</p>

<p>
src/index.jsx
const socket = io(`${location.protocol}//${location.hostname}:8090`);
socket.on('state', state =&gt;
  store.dispatch(setState(state))
);
</p>

<p>
const createStoreWithMiddleware = applyMiddleware(
  remoteActionMiddleware(socket)
)(createStore);
const store = createStoreWithMiddleware(reducer);
</p>

<p>
Note that we need to flip around the initialization of the socket and the store, so that the socket is
created first. We need it during store initialization.
</p>

<p>
All that remains to be done now is to actually emit an action event from the middleware:
</p>

<p>
src/remote<sub>action</sub><sub>middleware</sub>.js
export default socket =&gt; store =&gt; next =&gt; action =&gt; {
  socket.emit('action', action);
  return next(action);
}
</p>

<p>
And that's it! If you now click on one of the voting buttons, you'll also see the tally numbers
update, both within the same browser window and any other ones that you run the app in. The vote is
being registered!
</p>
</div>
</li>
<li><a id="sec-5-10-5-4" name="sec-5-10-5-4"></a><span class="todo TEST">TEST</span> Optimizaion<br  /><div class="outline-text-5" id="text-5-10-5-4">
<p>
There is one major problem we have with this though: When we get the state update from the server and
dispatch the SET<sub>STATE</sub> action, it also goes right back to the server. Although the server does nothing
with that action, its listener is still triggered, causing a new SET<sub>STATE</sub>. We have created an
infinite loop! That's certainly not good.
</p>

<p>
It is not appropriate for the remote action middleware to send each and every action to the server.
Some actions, such as SET<sub>STATE</sub>, should just be handled locally in the client. We can extend the
middleware to only send certain actions to the server. Concretely, we should only send out actions
that have a {meta: {remote: true}} property attached:
</p>

<p>
This pattern is adapted from the rafScheduler example in the middleware documentation. 
</p>

<p>
src/remote<sub>action</sub><sub>middleware</sub>.js
export default socket =&gt; store =&gt; next =&gt; action =&gt; {
  if (action.meta &amp;&amp; action.meta.remote) {
    socket.emit('action', action);
  }
  return next(action);
}
</p>

<p>
The action creator for VOTE should now set this property, where as the one for SET<sub>STATE</sub> should not:
</p>

<p>
src/action<sub>creators</sub>.js
export function setState(state) {
  return {
    type: 'SET<sub>STATE'</sub>,
    state
  };
}
</p>

<p>
export function vote(entry) {
  return {
    meta: {remote: true},
    type: 'VOTE',
    entry
  };
}
</p>

<p>
Let's recap what's actually happening here:
</p>

<p>
1 The user clicks a vote button. A VOTE action is dispatched. 
2 The remote action middleware sends the action over the Socket.io connection. 
3 The client-side Redux store handles the action, causing the local hasVote state to be set. 
4 When the message arrives on the server, the serverside Redux store handles the action, updating the
  vote in the tally. 
5 The listener on the serverside Redux store broadcasts a state snapshot to all connected clients. 
6 A SET<sub>STATE</sub> action is dispatched to the Redux store of every connected client. 
7 The Redux store of every connected client handles the SET<sub>STATE</sub> action with the updated state from
  the server. 
</p>

<p>
To complete our application, we just need to make the Next button work as well. Just like with voting,
the server has the appropriate logic already. We just need to connect things up.
</p>
</div>
</li>
<li><a id="sec-5-10-5-5" name="sec-5-10-5-5"></a><span class="todo TEST">TEST</span> action creator for NEXT<br  /><div class="outline-text-5" id="text-5-10-5-5">
<p>
The action creator for NEXT needs to create a remote action of the correct type:
</p>

<p>
src/action<sub>creator</sub>.js
export function setState(state) {
  return {
    type: 'SET<sub>STATE'</sub>,
    state
  };
}
</p>

<p>
export function vote(entry) {
  return {
    meta: {remote: true},
    type: 'VOTE',
    entry
  };
}
</p>

<p>
export function next() {
  return {
    meta: {remote: true},
    type: 'NEXT'
  };
}
</p>

<p>
The ResultsContainer component should connect the action creators in as props:
</p>

<p>
src/components/Results.jsx
import React from 'react';
import PureRenderMixin from 'react-addons-pure-render-mixin';
import {connect} from 'react-redux';
import Winner from './Winner';
import * as actionCreators from '../action<sub>creators'</sub>;
</p>

<p>
export const Results = React.createClass({
  mixins: [PureRenderMixin],
  getPair: function() {
    return this.props.pair || [];
  },
  getVotes: function(entry) {
    if (this.props.tally &amp;&amp; this.props.tally.has(entry)) {
      return this.props.tally.get(entry);
    }
    return 0;
  },
  render: function() {
    return this.props.winner ?
      &lt;Winner ref="winner" winner={this.props.winner} /&gt; :
      &lt;div className="results"&gt;
        &lt;div className="tally"&gt;
          {this.getPair().map(entry <code>&gt;
            &lt;div key={entry} className</code>"entry"&gt;
              &lt;h1&gt;{entry}&lt;/h1&gt;
              &lt;div className="voteCount"&gt;
                {this.getVotes(entry)}
              &lt;/div&gt;
            &lt;/div&gt;
          )}
        &lt;/div&gt;
        &lt;div className="management"&gt;
          &lt;button ref="next"
                   className="next"
                   onClick={this.props.next}&gt;
            Next
          &lt;/button&gt;
        &lt;/div&gt;
      &lt;/div&gt;;
  }
});
</p>

<p>
function mapStateToProps(state) {
  return {
    pair: state.getIn(['vote', 'pair']),
    tally: state.getIn(['vote', 'tally']),
    winner: state.get('winner')
  }
}
</p>

<p>
export const ResultsContainer = connect(
  mapStateToProps,
  actionCreators
)(Results);
</p>

<p>
And&#x2026; that's it! We now have a complete, functioning application. Try opening the results screen on
your computer and the voting screen on a mobile device. You'll see the actions applied on one device
immediately taking effect on another - which always feel magical: Vote on one screen, see the results
view update on another screen. Click "Next" on the results screen and see the vote proceed on your
voting device. To make it even more fun, arrange a vote with some friends the next time you get
together!
</p>
</div>
</li></ol>
</div>
</div>
</div>

<div id="outline-container-sec-6" class="outline-2">
<h2 id="sec-6"><span class="section-number-2">6</span> Exercises</h2>
<div class="outline-text-2" id="text-6">
</div><div id="outline-container-sec-6-1" class="outline-3">
<h3 id="sec-6-1"><span class="section-number-3">6.1</span> 1. Invalid Vote Prevention</h3>
</div>
<div id="outline-container-sec-6-2" class="outline-3">
<h3 id="sec-6-2"><span class="section-number-3">6.2</span> 2. Improved Vote State Reset</h3>
</div>
<div id="outline-container-sec-6-3" class="outline-3">
<h3 id="sec-6-3"><span class="section-number-3">6.3</span> 3. Duplicate Vote Prevention</h3>
</div>
<div id="outline-container-sec-6-4" class="outline-3">
<h3 id="sec-6-4"><span class="section-number-3">6.4</span> 4. Restarting The Vote</h3>
</div>
<div id="outline-container-sec-6-5" class="outline-3">
<h3 id="sec-6-5"><span class="section-number-3">6.5</span> 5. Indicating Socket Connection State</h3>
</div>
<div id="outline-container-sec-6-6" class="outline-3">
<h3 id="sec-6-6"><span class="section-number-3">6.6</span> Bonus Challenge: Going Peer to Peer</h3>
<div class="outline-text-3" id="text-6-6">
</div><div id="outline-container-sec-6-6-1" class="outline-4">
<h4 id="sec-6-6-1"><span class="section-number-4">6.6.1</span> Loading Entries</h4>
</div>
<div id="outline-container-sec-6-6-2" class="outline-4">
<h4 id="sec-6-6-2"><span class="section-number-4">6.6.2</span> Starting The Vote</h4>
</div>
<div id="outline-container-sec-6-6-3" class="outline-4">
<h4 id="sec-6-6-3"><span class="section-number-4">6.6.3</span> Voting</h4>
</div>
<div id="outline-container-sec-6-6-4" class="outline-4">
<h4 id="sec-6-6-4"><span class="section-number-4">6.6.4</span> Moving to The Next Pair</h4>
</div>
<div id="outline-container-sec-6-6-5" class="outline-4">
<h4 id="sec-6-6-5"><span class="section-number-4">6.6.5</span> Ending The Vote</h4>
</div>
</div>

<div id="outline-container-sec-6-7" class="outline-3">
<h3 id="sec-6-7"><span class="section-number-3">6.7</span> Introducing Actions and Reducers</h3>
</div>
<div id="outline-container-sec-6-8" class="outline-3">
<h3 id="sec-6-8"><span class="section-number-3">6.8</span> A Taste of Reducer Composition</h3>
</div>
<div id="outline-container-sec-6-9" class="outline-3">
<h3 id="sec-6-9"><span class="section-number-3">6.9</span> Introducing The Redux Store</h3>
</div>
<div id="outline-container-sec-6-10" class="outline-3">
<h3 id="sec-6-10"><span class="section-number-3">6.10</span> Setting Up a Socket.io Server</h3>
</div>
<div id="outline-container-sec-6-11" class="outline-3">
<h3 id="sec-6-11"><span class="section-number-3">6.11</span> Broadcasting State from A Redux Listener</h3>
</div>
<div id="outline-container-sec-6-12" class="outline-3">
<h3 id="sec-6-12"><span class="section-number-3">6.12</span> Receiving Remote Redux Actions</h3>
</div>
</div>
<div id="footnotes">
<h2 class="footnotes">Footnotes: </h2>
<div id="text-footnotes">

<div class="footdef"><sup><a id="fn.1" name="fn.1" class="footnum" href="#fnr.1">1</a></sup> <p>DEFINITION NOT FOUND.</p></div>

<div class="footdef"><sup><a id="fn.2" name="fn.2" class="footnum" href="#fnr.2">2</a></sup> <p>DEFINITION NOT FOUND.</p></div>


</div>
</div></div>
<div id="postamble" class="status">
<p class="author">Author: root</p>
<p class="date">Created: 2015-11-29 Sun 04:16</p>
<p class="creator"><a href="http://www.gnu.org/software/emacs/">Emacs</a> 24.5.2 (<a href="http://orgmode.org">Org</a> mode 8.2.10)</p>
<p class="validation"><a href="http://validator.w3.org/check?uri=referer">Validate</a></p>
</div>
</body>
</html>
