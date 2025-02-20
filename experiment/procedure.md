### Procedure
<b>Step 1 - Simulation Introduction</b>
  <p> <li> You have two simulated browsers. One represents you (the user), and the other belongs to Alice.</li>
   <li> Both browsers will load a blog page, which allows you to post comments.</li>
</P>
<img src="./images/step1.png" alt="step1 "><br/>
<b>Step 2 - Loading the Blog</b>
<li>navigate to the blog page</li>
<li>Observe the comments section where you can post your comments.</li>
<img src="./images/step2.png" alt="step2 "><br/>

<b>Step 3 -Introducing an XSS Payload</b>
<li>In your browser, type the following comment:
  
     <script>alert(1)</script>

   - Submit the comment.
</li>
<img src="./images/step3.png" alt="step3 "><br/>

<b>Step 4 -Triggering the Alert</b>
<li>In your browser, observe that as soon as you submit the comment, an alert with the message "1" pops up.
</li>
<img src="./images/step4.png" alt="step4 "><br/>

<b>step 5- Storing the Payload</b>
<li> In Alice's browser, refresh the blog page.</li>
   <li> Notice that Alice's browser also displays the same alert, which is a consequence of the stored XSS vulnerability.</li>
<img src="./images/step5.png" alt="step5 "><br/>

<b>Step 6 - Preventing Stored XSS</b>
<p>To prevent stored XSS vulnerabilities, </p>
<li> Implement input validation and sanitization on the server-side to filter out or escape potentially malicious content.</li>
<img src="./images/step6.png" alt="step6 "><br/>





