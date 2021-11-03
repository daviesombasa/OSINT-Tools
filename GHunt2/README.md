# Google Hunt Tool 
<p> Will help you obtain information concerning gmail accounts.</p>
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_20.png">
<h2>The information that can be obtained include:</h2>

<ol>
  <li>Possible owner's name and profile picture</li>
  <li>Google ID</li>
  <li>Possible YouTube channel</li>
  <li>Google Maps reviews</li>
  <li>Activated Google services (YouTube, Photos, Maps, News360, Hangouts, etc.)</li>
  <li>Possible physical location</li>
</ol>

## INSTALLATION Requirements:
<ol>
  <li>Linux OS with root access - preferable Kali-Linux</li>
  <li>Python 3.7+ installed</li>
  <li>Google Chrome or Firefox installed</li>
  <li>Docker installed (only if you intend to use the docker option)</li>
  <li>Internet connectivity (obviously :))</li>
 </ol>

## LETS HACK!

### 1. Download the source code from the github link : https://github.com/mxrch/GHunt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git clone https://github.com/-mxrch/GHunt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_1.png">

## 2. Change directory to GHunt	
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cd GHunt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_2.png">

## 3. Installing the python depencies
#### NB: This will take some time.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
python3 -m pip install -r requirements 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_19.png">
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_3.png">

## 4. Configuring the cookies. 
This is done during the first installation but also may be required from time to time. There is an automated way of doing this and a manual way.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
python3 check_and_gen.py
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_4.png">

### a. The Manual Way 
To obtain the cookies to use:
<ol>
  <li>Login to your gmail account (advisable to use an account you don't use oftnely)</li> 
  <li>Go to www.google.com on your browser</li>
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_5.png">
  <li>Right click and select the Inspect option</li>
	<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_6.png">
  <li>Select the Application tab at the top and then go to the cookies section on the left and click on www.google.com. </li>
  <li>The cookies will be displayed on the right. (Be carefull to copy them properly and avoid having spaces or identation)</li>
	<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_7.png">
  <li>NB: For firefox, you'll find them under the Storage tab</li>
	<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_8.png">
</ol>

	   
### b. Alternatively you can use the cookies-editor addon to obtain your cookies
<ol>
  <li>
    Download the cookie-editor from chrome web store or firefox extensions <br>
    → Chrome link : https://chrome.google.com/webstore/detail/cookie-editor/hlkenndednhfkekhgcdicdfddnkalmdm?hl=en <br>
    → Firefox link: https://addons.mozilla.org/en-US/firefox/addon/cookie-editor/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search <br></li>
  <img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_9.png">
  <li>Once download, go to your www.google.com page and click on the cookie-editor addon to view your cookies</li>
	<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_17.png">
  <li>Now go back to your python script and copy in the cookies. (Be carefull to copy them properly and avoid having spaces or identation)</li>
	<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_10.png">
</ol>

### c. Using the automated way (not compatible with docker)
<ol>
  <li>Obtain the GHunt cookie addon ( available only on Firefox from - https://addons.mozilla.org/fr/firefox/addon/ghunt-companion/ )</li>
	<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_18.png">
  <li>Select option 1 to use the GHunt addon. GHunt will begin listening on a port generated.</li>
	<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_16.png">
  <li>Go back to www.google.com and open the GHunt addons.</li>
  <li>Then click on Method 1. The cookies will be updated automatically.</li>
</ol>

## 5. Using the tool:
### a. Using the email option to gather information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
python3 ghunt.py email target_email@gmail.com
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_12.png">

### b. Using the google doc link option to gather information 	
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
python3 ghunt.py doc <google docs link>
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_13.png">

### c. Using the youtube link option to gather information  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
python3 ghunt.py  youtube <youtube link>
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_14.png">

### d. Using the google id option to gather information    
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
python3 ghunt.py gaia <Google Authentication Identification ID>
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
<img src="https://github.com/daviesombasa/OSINT-Tools/blob/02d2820917c0f7bc017b4e50a0de983f0f2625ce/GHunt2/img/img_15.png">
<hr>
<div><b><i>THE END</i></b></div>

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Comic+Sans&color=%23001980&size=15&center=false&vCenter=false&multiline=true&width=600&height=100&lines=sudo-apt+get+happiness+%F0%9F%98%8A+;from+daviesombasa)](https://git.io/typing-svg)
