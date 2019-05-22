# Traktor Transition Finder

<span class="badge-paypal"><a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&amp;hosted_button_id=GFDKRJ7LCQFQS" title="Donate to this project using Paypal"><img src="https://img.shields.io/badge/paypal-donate-yellow.svg" alt="PayPal donate button" /></a> if you think this project is awesome. </span>

A small tool for automatically finding the next song to play when DJing using Traktor Pro 2.

The tool works by creating a weighted graph of every song in a Traktor collection of songs, where the weights determine what song is best to mix into. 
The weight is calculated using the BPM of the songs and their different keys. 

The tool is written in F# and Node.js/Electron. The backend is written in F#, and acts as a small web server receiving graph/song requests. 
The frontend is written in Node.js/Electron and sends requests to the F# web server.

When a song is dropped into the app, the best transitions from that song are displayed. 
The DJ can then pick a song from the list in Traktor Pro 2. The app merely functions as a suggestion list.

#### [Download](https://github.com/andersfischernielsen/Traktor-Transition-Finder/releases/latest)

![Screenshot](readme/readme.png) 

## How to Use
- Open the app and click the button to find your Traktor collection. 
- Browse to the location of your collection.nml file.
- Let the app analyse the collection.
- Drag a file from the song list in Traktor into the app to get a list of possible transitions from the song.


## Implementation
The first version of the app consists of a F# backend handling parsing the Traktor 2 collection and serving results as JSON to the Electron frontend. 

The second version of the app is fully implemented in TypeScript and Electron. 

The third (current) version of the app is implemented in Swift, available for macOS. 
