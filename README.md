# WebSDR Cat-Control // Orbitron2WebSDR
This application is developed to track satellite radio signals via WebSDR, taking into account the Doppler shift by using the MyDDE driver of the satellite tracker "Orbitron."
WebSDR (Web = accessible via the Internet, SDR = Software Defined Radio) is a radio receiver operating in a web browser. It feeds what it receives on the amateur radio bands live to the Internet and makes it available to all interested listeners via a web page.

"Orbitron" is a satellite tracking system for radio amateurs and satellite observers. It determines the positions of satellites in real-time, whether you want the information at the current time of day or later. To forward the Doppler-shifted reception frequency of the satellite to an amateur radio receiver, a so-called CAT-Control driver for this receiver is needed. The WebSDR radio could be operated remotely via the browser through the CAT-Control.

Orbitron provides a driver called MyDDE for this purpose. This driver transmits the receive frequency via DDE. In computing, DDE or Dynamic Data Exchange is a technology for interprocess communication used in early versions of Microsoft Windows and OS/2. DDE allows programs to manipulate objects provided by other programs and respond to user actions affecting those objects.
The application "WebSDR Cat-Control" now establishes a connection from Orbitron to the WebSDR receiver via the MyDDE-Driver and forwards the Doppler-shifted reception frequency of the satellite to be tracked in real-time. WebSDR Cat-Control // Orbitron2WebSDR is developed in LabVIEW 2021.

Requirements:
----------------
1) Orbitron version 3.71  (Download here: http://www.stoff.pl/)

2) MyDDE driver  (Download here: http://www.stoff.pl/orbitron/files/mydde.zip)

3) Virtual audio cable enables audio signals to be streamed from the web browser running WebSDR to 
   the corresponding satellite decoder modem (f.ex.: soundmodem, Funcube dashboard, RCSSTV, WX2IMG). 
   Download here: https://vb-audio.com/Cable/

4) Install the modem needed to decode the satellite's audio signal into processable telemetry or satellite image
   (f.ex.: soundmodem, Funcube dashboard, RCSSTV, WX2IMG). Notice that here you must investigate which modem is needed 
   to decode your satellite's telemetry data, auto beacons, or space-born images. Sometimes you must also set up correct 
   modem options like baud rates (or bit rates), modulation modes, and other parameters.
   
        Some example satellite modems:
             - For APRS satellites and the ISS: latest version of soundmodem:
               http://uz7.ho.ua/packetradio.htm
               
             - For cubesats using higher baudrates use latest version of hs_soundmodem:
               http://uz7.ho.ua/packetradio.htm
               
             - For AO73/FUNcube-1, NAYIF, JY1SAT over VHF: 
               https://funcube.org.uk/working-documents/funcube-telemetry-dashboard/
               
             - For SSTV from the ISS over VHF: 
               https://www.qsl.net/on6mu/rxsstv.htm
               
             - NOAA and Meteor weather satellites - WX2IMG
               https://wxtoimgrestored.xyz/downloads/
               or:
               https://www.wraase.de/wxtoimg/
               and for updating the TLE's in WX2IMG:
               https://wxtoimgrestored.xyz/other-software/

             - Meteor weather satellites (I didn't test this one):
               https://leshamilton.co.uk/MeteorLRPTSuite.htm
    
5) Download prefered web browser. I have tested those two with Orbitron2WebSDR: 

              - Firefox is recommended; download here: https://www.mozilla.org/en-US/firefox/new/).
              - Google chrome: https://www.google.com/chrome/?brand=YTUH&gclid=CjwKCAjwhJukBhBPEiwAniIcNQcMnoN9f7adkIPBTzIeZHJMiBlrEGvkuRs4LQamYxyKoYvDNWF9mBoCD6wQAvD_BwE&gclsrc=aw.ds.

6) LabVIEW 21 32bit runtime engine (https://www.ni.com/de-de/support/downloads/software-products/download.labview-runtime.html#443250)

7) Install Orbitron2WebSDR Build for win 10: https://github.com/sachatholl/Orbitron2WebSDR/tree/main/Orbitron2Websdr_Win10Build
   Convinniently, you can download all of it using the provided .zip file 
   under in the upper right corner on this page. The executable "Orbitron2WebSDR.exe"
   is located in the folder "Orbitron2Websdr_Win10Build" There, you find also the 
   runtime engine "ni-labview-2021-runtime-engine-x86_21.1_online.exe".
   After having poperly installed the runtime engine, you should be able
   to start "Orbitron2WebSDR.exe" out of the box.
   
8) Configure Audio routing between the Webbrowser with active WebSDR station and 
   the satellite modem. Conveniently perform the steps as shown in the tutorial 
   video below, or perform the following steps similarly:

             - Configure VB-Audio Cable as the default audio device:
                  - Right-click the speaker icon in the Windows taskbar and select "Open Sound settings."
                  - Under the "Output" section, select VB-Audio Cable as the default audio device for playback.
                  - Under the "Input" section, select VB-Audio Cable as the default audio device for recording.

             - Set up the WebSDR satellite ground station:
                  - Open your preferred web browser and navigate to the WebSDR satellite ground station 
                    you want to use.
                  - Tune the receiver to the appropriate frequency and ensure you can hear the audio output.

             - Configure audio routing:
                  - Open the Control Panel on your computer.
                  - Navigate to "Hardware and Sound" and click on "Sound."
                  - In the "Playback" tab, select the audio output device corresponding to your speakers 
                    or headphones and set it as the default device.
                  - In the "Recording" tab, select VB-Audio Cable as the default recording device.
                    Double click on VB-Audio Cable: Under "
                  - Alternatively check the "Listen" tab in the properties of VB-Audio Cable output. 
                    It allows you to enable the "Listen to this device" feature, which essentially allows 
                    you to hear the audio being routed through VB-Audio Cable in real-time through your speakers.

                    ![image](https://github.com/sachatholl/Orbitron2WebSDR/assets/3606905/dfad3f51-5ea6-4835-97b3-6307b45b0c49)

                    When you check the "Listen to this device" checkbox and select your speakers as the playback device, 
                    any audio that is sent through VB-Audio Cable will be simultaneously played through your speakers. 
                    This feature can be useful when you want to monitor the audio that is being routed through VB-Audio Cable 
                    without having to rely on separate monitoring methods or applications. Enabling the "Listen to this device" 
                    feature with your speakers selected as the playback device can help you verify that the audio is being 
                    properly routed and allows you to hear the output in real-time. It can be particularly useful when 
                    troubleshooting audio routing issues or when you need to monitor the audio for any specific purpose, 
                    such as quality assurance or real-time feedback.
                    
             - Configure your satellite's software modem/decoder to use VB-Audio Cable as the audio input. 
               Please consult the technical reference of the intended software modem/decoder.
           
             - Start decoding-test if possible:
                  - Launch the satellite's software modem/decoder.
                  - Ensure the audio is playing from the WebSDR satellite ground station and 
                    routed through VB-Audio Cable. (radio unmuted; squelsch unchecked; ajust WebSDR audio volume)
                  - Start the decoding process of your satellite's software modem/decoder if needed.

             - The WebSDR satellite ground station audio signal should now be received by your satellite's software modem/decoder 
               and used for decoding the telemetry data, auto beacons, or space-born satellite images.
   
   Whish you a nice time :-)
   have fun,
  
   Sacha



Videos:
----------------

[![Orbitron2Websdr](https://user-images.githubusercontent.com/3606905/159119945-d6d3702a-a1e7-4796-a31f-a2ced8f14182.JPG)](https://www.youtube.com/watch?v=LkdO7o0-AwY)


[![image](https://user-images.githubusercontent.com/3606905/155881896-1a0cb6a4-7386-4a0d-8725-96ccdb60dfef.png)](https://www.youtube.com/watch?v=3J_UkhTQFNA)
