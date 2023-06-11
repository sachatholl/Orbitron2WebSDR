# WebSDR Cat-Control // Orbitron2WebSDR
This application is developed to track satellite radio signals via WebSDR, taking into account the Doppler shift by using the MyDDE driver of the satellite tracker "Orbitron." 

WebSDR (Web = accessible via the Internet, SDR = Software Defined Radio) is a radio receiver operating in a web browser. It feeds what it receives on the amateur radio bands live to the Internet and makes it available to all interested listeners via a web page.

"Orbitron" is a satellite tracking system for radio amateurs and satellite observers. It determines the positions of satellites in real-time, whether you want the information at the current time of day or later. To forward the Doppler-shifted reception frequency of the satellite to an amateur radio receiver, a so-called CAT-Control driver for this receiver is needed. The WebSDR radio could be operated remotely via the browser through the CAT-Control.

Orbitron provides a driver called MyDDE for this purpose. This driver transmits the receive frequency via DDE. In computing, DDE or Dynamic Data Exchange is a technology for interprocess communication used in early versions of Microsoft Windows and OS/2. DDE allows programs to manipulate objects provided by other programs and respond to user actions affecting those objects.

The application "WebSDR Cat-Control" now establishes a connection from Orbitron to the WebSDR receiver via the MyDDE-Driver and forwards the Doppler-shifted reception-frequency of the satellite to be tracked in real-time. WebSDR Cat-Control // Orbitron2WebSDR is developped in LabVIEW 2020

Requirements:
----------------
1) Orbitron version 3.71  (Download here: http://www.stoff.pl/)

2) MyDDE driver  (Download here: http://www.stoff.pl/orbitron/files/mydde.zip)

4) Virtual audio cable enables audio signals to be streamed from the web browser running WebSDR to 
   the corresponding satellite decoder modem (f.ex.: soundmodem, Funcube dashboard, RCSSTV, WX2IMG). 
   Download here: https://vb-audio.com/Cable/

5) Install the modem needed to decode the satellite's audio signal into processable telemetry or satellite image
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
    
6) Prefered web browser (Firefox is recommended; download here: https://www.mozilla.org/en-US/firefox/new/)
   But google chrome works also fine since the latest update of the Orbitron2WebSDR.

7) LabVIEW 21 32bit runtime engine (https://www.ni.com/de-de/support/downloads/software-products/download.labview-runtime.html#443250)

8) Install Orbitron2WebSDR Build for win 10: https://github.com/sachatholl/Orbitron2WebSDR/tree/main/Orbitron2Websdr_Win10Build
   Convinniently, you can download all of it using the provided .zip file 
   under in the upper right corner on this page. The executable "Orbitron2WebSDR.exe"
   is located in the folder "Orbitron2Websdr_Win10Build" There, you find also the 
   runtime engine "ni-labview-2021-runtime-engine-x86_21.1_online.exe".
   After having poperly installed the runtime engine, you should be able
   to start "Orbitron2WebSDR.exe" out of the box.
   
   Whish you a nice time :-)
   have fun,
  
   Sacha



Videos:
----------------

[![Orbitron2Websdr](https://user-images.githubusercontent.com/3606905/159119945-d6d3702a-a1e7-4796-a31f-a2ced8f14182.JPG)](https://www.youtube.com/watch?v=LkdO7o0-AwY)


[![image](https://user-images.githubusercontent.com/3606905/155881896-1a0cb6a4-7386-4a0d-8725-96ccdb60dfef.png)](https://www.youtube.com/watch?v=3J_UkhTQFNA)
