# GUNJS-Starterkit+Quickstart
#### A collection of tools you need to run a local-first, decentralized graph database.<br>
For GunJS Wiki check also https://github.com/amark/gun/wiki<br>
<br>
##### GunJS can be explained as a decentralized alternative to cloud-based services like Dropbox and Firebase. Both Dropbox and Firebase provide cloud-based storage and synchronization of data, but with GunJS, the data is stored and synchronized across a decentralized network of peers, rather than relying on a central server. In this setup, each user's device acts as a node in the network, storing a copy of the data and making it available to other nodes. This means that data is always accessible, even if one node goes offline, because it can be retrieved from another node. GunJS also provides real-time synchronization, ensuring that all nodes in the network have the latest version of the data, similar to Dropbox and Firebase, but with the added benefits of improved security and privacy, as data is not controlled by a central authority. Additionally, GunJS allows for peer-to-peer data sharing, enabling users to directly exchange data without having to go through a central server. This makes it a flexible and scalable solution for real-time data storage and synchronization, similar to Firebase, but with a decentralized approach.<br>
<br>

![image](https://user-images.githubusercontent.com/67427045/214804241-d1b2b365-fa5d-4b35-9a31-e3301acf466f.png)
<br><br>

# Starterkit Contents
<br>

## Gun, Desktop-Relay, Form, Relay Donation, Digital Globe (location-based services)
### https://github.com/amark/gun
#### An open source cybersecurity protocol for syncing decentralized graph data.

### https://github.com/worldpeaceenginelabs/ELECTRON-GUN
#### A Gun Relay Server executable for Desktop (Windows,-Linux,-MAC)

### https://github.com/worldpeaceenginelabs/FORM-GUN
#### A decentralized form handler with Gun for "static" JAMStack websites on a CDN. Plus "Svelte Compiler Tutorial with Gun"

### https://github.com/worldpeaceenginelabs/DONATE-DECENTRALIZE-UI
#### A little taskbar which empowers your fanbase to deploy a Gun relay on multiple ways to support your decentralized website/app.
 
### https://github.com/worldpeaceenginelabs/CESIUM-GUN
#### This is a POC of a decentralized, open-source Google Earth made with Gun and Cesium.<br>
<br>

## Storage logic

### GunJS - Included and third-party storage solutions https://github.com/amark/gun/wiki/Storage
#### To permanently store all GUN's data, your GUN server app must define which storage engine to use. By default a GUN server will store the data in a file, but this is just meant to be used during development. It is not a sound solution for production.
#### However, GUN is different to most other databases when it comes to dev vs prod setup in that the only distinction is that a production setup can maybe include a persistent storage option (e.g. AWS S3, IPFS...) for a participating relay peer. That's not mandatory though, browsers peers with their localStorage storage are sufficient more often than not, doesn't matter if you're still in development or already running your app in production with customers.<br>
<br>

### https://github.com/worldpeaceenginelabs/1-MEGABYTE-STORE
#### A storage logic to distribute your whole user-database, but with only 1 Megabyte on each user's device. Works with 1, 100, 3333, and 8 Billion users but stays always 1 MB!!!<br>
<br>

## Webcrypto API
#### https://gist.github.com/pedrouid/b4056fd1f754918ddae86b32cf7d803e (Web Cryptography API Examples - A collection of well commented, well ordered snippets for 20 algorithms)
#### https://diafygi.github.io/webcrypto-examples/ (This table is live! Every ✓ or ✗ on this page is a test to see if your browser supports that method in WebCryptoAPI.)
#### God bless the internet, open-source and collaboration. Amen 🙏😂

## Authentication, encryption/hash, security
### https://github.com/worldpeaceenginelabs/DAuth
#### A decentralized OAuth / Metamask Login | Without server, files or API... Just 1kb of logic!

### https://github.com/antelle/argon2-browser
#### Argon2 library compiled for browser runtime

### https://github.com/emn178/js-sha3
#### A simple SHA-3 / Keccak hash function for JavaScript supports UTF-8 encoding.

### https://github.com/brix/crypto-js
#### JavaScript library of crypto standards.

### https://github.com/ai/nanoid
#### A tiny (130 bytes), secure, URL-friendly, unique string ID generator for JavaScript
 
### https://github.com/mozilla/node-srp
#### Secure Remote Password (SRP)<br>
<br>

# QUICKSTART for components, apps, webapps, dapps... (the decentralized back-end)
<br>

## GUN Relays (Gun works local first even without a relay, but for syncing between clients you need a relay)
### [Gun Relay (How to run a node - Deploy a GUN relay server everywhere on GUN WIKI)](https://github.com/amark/gun/wiki#how-to-run-a-node---deploy-a-gun-relay-server-everywhere)
### [Gun Relay Desktop (Electron Gun)](https://github.com/worldpeaceenginelabs/ELECTRON-GUN)
### [Gun Relay Donation Tool (Donate Decentralize UI)](https://github.com/worldpeaceenginelabs/DONATE-DECENTRALIZE-UI)<br>
<br>

## .get() | .put | .on - There are [more methods...](https://gun.eco/docs/API) but these three are the basic ones.
### This is pretty much the core of everything. Notice how easy it is to connect your front-end code with the graph database GUN.
### Notice that no matter how complex your function is: You just drop the result into one or multible variables and connect them to the GUN write function (green boxes, green lines).
### Last, you can easily receive the data in any function, again, no matter how complex, by ```db.on(data => {//your function here});``` and get the data that you wrote to GUN before (red boxes, red lines)<br>
<br>

![image](https://user-images.githubusercontent.com/67427045/212865152-88544d46-f46b-4cd5-9d2e-4f2571dfb80b.png)
![image](https://user-images.githubusercontent.com/67427045/216111036-ee93b490-3506-42cf-a454-e416962b86d3.png)
### This script saves a long/lat pair to the GUN graph, and renders a point on the globe, if the local clients graph (browser local storage) or a connected graph (GUN-Relay) receive a new entry.<br>(the ```.on(graphname)``` subscribes to the GUN graph. Everything's new to the graph will automatically be rendered on the globe) Both local storage graph and/or relay graph changes!
