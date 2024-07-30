# Mediasoup Sample App

A minimal Client/Server app based on Mediasoup and Socket.io


## Dependencies

* [Mediasoup v3 requirements](https://mediasoup.org/documentation/v3/mediasoup/installation/#requirements)
* Node.js >= v8.6
* [Browserify](http://browserify.org/)


## Run

The server app runs on any supported platform by Mediasoup. The client app runs on a single browser tab.
```
# create and modify the configuration
# make sure you set the proper IP for mediasoup.webRtcTransport.listenIps
cp config.example.js config.js
nano config.js

# install dependencies and build mediasoup
npm install

# create the client bundle and start the server app
npm start
```

# install mkcert using choco:


How to Install Chocolatey on Windows:

1. Open PowerShell as Administrator:
   - Click on the Start menu, type `powershell`, right-click on Windows PowerShell, and select `Run as Administrator`.

2. Run the Installation Command:
   - Copy and paste the following command into the PowerShell window and press Enter:
     ```sh
     Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
     ```

3. Verify Chocolatey Installation:
   - Close and reopen PowerShell as Administrator.
   - Run the following command to verify the installation:
     ```sh
     choco -v
     ```
   - You should see the version number of Chocolatey if it is installed correctly.

Install mkcert Using Chocolatey:

1. Install mkcert:
   ```sh
   choco install mkcert

2. Install the local CA: 
    ```sh
   mkcert -install

# Generate SSL certificats:

cd path\to\your\project\directory
mkcert -key-file ssl-cert-snakeoil.key -cert-file ssl-cert-snakeoil.pem localhost 127.0.0.1 ::1

This command will generate two files: ssl-cert-snakeoil.key (private key) and ssl-cert-snakeoil.pem (certificate).