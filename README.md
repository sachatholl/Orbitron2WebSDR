# WebSDR Cat-Control // Orbitron2WebSDR
This application is developed to track satellite radio signals via WebSDR, taking into account the Doppler shift by using the MyDDE driver of the satellite tracker "Orbitron." 

WebSDR (Web = accessible via the Internet, SDR = Software Defined Radio) is a radio receiver operating in a web browser. It feeds what it receives on the amateur radio bands live to the Internet and makes it available to all interested listeners via a web page.

"Orbitron" is a satellite tracking system for radio amateurs and satellite observers. It determines the positions of satellites in real-time, whether you want the information at the current time of day or later. To forward the Doppler-shifted reception frequency of the satellite to an amateur radio receiver, a so-called CAT-Control driver for this receiver is needed. The WebSDR radio could be operated remotely via the browser through the CAT-Control.

Orbitron provides a driver called MyDDE for this purpose. This driver transmits the receive frequency via DDE. In computing, DDE or Dynamic Data Exchange is a technology for interprocess communication used in early versions of Microsoft Windows and OS/2. DDE allows programs to manipulate objects provided by other programs and respond to user actions affecting those objects.

The application "WebSDR Cat-Control" now establishes a connection from Orbitron to the WebSDR receiver via the MyDDE-Driver and forwards the Doppler-shifted reception-frequency of the satellite to be tracked in real-time. WebSDR Cat-Control // Orbitron2WebSDR is developped in LabVIEW 2020

Requirements:
----------------
1)Orbitron version 3.71  (Download here: http://www.stoff.pl/)

2)MyDDE driver  (Download here: http://www.stoff.pl/orbitron/files/mydde.zip)

3)prefered web browser (Firefox is recommended; download here: https://www.mozilla.org/en-US/firefox/new/)

4)LabVIEW 21 32bit runtime engine (https://www.ni.com/de-de/support/downloads/software-products/download.labview-runtime.html#443250)

5)Install Orbitron2WebSDR Build for win 10: https://github.com/sachatholl/Orbitron2WebSDR/tree/main/Orbitron2Websdr_Win10Build
Basically you should just nrrd to start the executable to work



Videos:
----------------

[![Orbitron2Websdr](https://user-images.githubusercontent.com/3606905/159119945-d6d3702a-a1e7-4796-a31f-a2ced8f14182.JPG)](https://www.youtube.com/watch?v=LkdO7o0-AwY)


[![image](https://user-images.githubusercontent.com/3606905/155881896-1a0cb6a4-7386-4a0d-8725-96ccdb60dfef.png)](https://www.youtube.com/watch?v=3J_UkhTQFNA)
