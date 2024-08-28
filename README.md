<h1>Amazon Lex Language Translation Bot</h1>


<h2>Description</h2>
In this project I will be building a language translation bot using Amazon Lex, the bot will be able to translate a word or a sentence into another language by the input that is typed to the chatbot. 
<br />


<h2>Services used</h2>

- <b>Amazon Lex
- <b>Amazon Lambda
- <b>AWS IAM
- <b>Amazon Translate

<h2>Architectural Diagram</h2>

<img src="https://imgur.com/zAMG5qV.png" height="80%" width="80%"/>

<h2>Project walk-through:</h2>

<p align="center">
First I navigated to Amazon Lex in the AWS management console and created an empty chatbot by giving the bot a name and a description.  <br/>
<img src="https://imgur.com/F2K44Ha.png" height="80%" width="80%"/>
<br />
<br />
For the IAM role I chose " Create a role with basic Amazon Lex permissions ". For the "Children’s Online Privacy Protection Act (COPPA) " i selected "No" and I left the rest as default.  <br/>
<img src="https://imgur.com/eYd0MyP.png" height="80%" width="80%"/>
<br />
<br />
On the next page you are able to chose the language you want to communicate to the bot in and the voice the bot will have. I kept the options at default for this and now I have my blank chat bot. <br/>
<img src="https://imgur.com/hEHIkGV.png" height="80%" width="80%"/>
<br />
<br />
Now I moved on to the intent section where I gave an intent name and description. <br/>
<img src="https://imgur.com/zpd4sDI.png" height="80%" width="80%"/>
<br />
<br />
Now in the Sample utterances I added some inputs that can be asked by the user. I will come back and add some more. I clicked "Save Intent" and moved to Slot types in the left menu.  <br/>
<img src="https://imgur.com/yshBVEx.png" height="80%" width="80%"/>
<br />
<br />
In the slots types I added a new blank slot type and named it "language"<br/>
<img src="https://imgur.com/oGGqlp9.png" height="80%" width="80%"/>
<br />
<br />
I added a few languages in the slot type values and then saved slot type <br/>
<img src="https://imgur.com/L0BYh1P.png" height="80%" width="80%"/>
<br />
<br />
I then moved back to the intents page and added the slot type I just created.<br/>
<img src="https://imgur.com/Q8mnBJN.png" width="80%"/>
<br />
<br />
I then created another slot for text with the slot type set to AMAZON.FreeFormInput. <br/>
<img src="https://imgur.com/tQbPyHj.png" width="80%"/>
<br />
<br />
I then went back to add some more utterances so if the user inputs a type of language they want to translate to it will recognise it. <br/>
<img src="https://imgur.com/dX9Xrtb.png" width="80%"/>
<br />
<br />
I also added an initial response as a Feeback message for the user   <br/>
<img src="https://imgur.com/9srYvx0.png" width="80%"/>
<br />
<br />
Now I moved down to specify fulfilment section to add feedback on successful and failure inputs. I also clicked on the advanced option and enabled " Use a Lambda function for fulfilment ".<br/>
<img src="https://imgur.com/aGKYh9o.png" width="80%"/>
<br />
<br />
I moved down the closing response sections and added a message for the end of a response. 
<br/>
<img src="https://imgur.com/wU4hwDX.png" width="80%"/>
<br />
<br />
Next I navigated to IAM role to create a role for a Lambda function. 
<br/>
<img src="https://imgur.com/UA7pLaT.png" width="80%"/>
<br />
<br />On the next page I added two policies (TranslateFullAccess and AWSLambdaBasicExecutionRole) and in the next step I entered a role name and description then clicked create role. 
<br/>
<img src="https://imgur.com/PFxRc9W.png" width="80%"/>
<br />
<br />Now I went to the Lambda page to create a function, I gave the function a name and changed the runtime to Python 3.12. I then toggled the default execution role and added my role I made.  
<br/>
<img src="https://imgur.com/Md4c4rq.png" width="80%"/>
<br />
<br />I then added the code in the code source section and clicked deploy. 
<br/>
<img src="https://imgur.com/Y9Po3TL.png" width="80%"/>
<img src="https://imgur.com/B9E6c3Z.png" width="80%"/>
<img src="https://imgur.com/TS9PZzx.png" width="80%"/>
<img src="https://imgur.com/t0vtqcg.png" width="80%"/>
<img src="https://imgur.com/ad4rKh4" width="80%"/>
<br />
<br />
Next I ran a test to make sure that the code was working as intended.  
<br/>
<img src="https://imgur.com/YsrLGZk.png" width="80%"/>
<img src="https://imgur.com/Qo5oJUu.png" width="80%"/>
<br/>
Next I need to add the lambda function to be used by Lex, I clicked on Test on the bot I created and then clicked on the settings cog at the top right of the bot. <br/>
<img src="https://imgur.com/IKOol5t.png" width="80%"/>
<br/>
I then tested the bot to make sure everything I had done was working correctly  
<br/>
<img src="https://imgur.com/9Zui2za.png" width="80%"/>
<img src="https://imgur.com/Vb2s7gO.png" width="80%"/>
<br />
<br />
 
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

