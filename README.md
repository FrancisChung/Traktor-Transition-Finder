
<p align="center"><img src="docs/icon.png" width="128" height="128"></img></p>
<h1 align="center">Traktor Transition Finder</p></h1>
<p align="center">A small tool for automatically finding the next song to play when DJing using Traktor</p>
<p align="center"><a href="https://github.com/andersfischernielsen/Traktor-Transition-Finder/releases/latest">Download</a></p>

***

When a song is dropped into the app the best transitions from that song are displayed based on BPM and the keys of songs. 

Two songs can also be dropped into the app in order to find the shortest path between two songs, allowing a DJ to quickly transition between two desired songs.

The DJ can then pick a song from the list in Traktor.

![Screenshot](readme/readme.png) 

The tool creates a weighted digraph of every song in a Traktor collection of songs, where the weights determine what song is best to mix into from the current song. The weight is calculated using the BPM of the songs and their different keys. 

<span class="badge-paypal"><a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&amp;hosted_button_id=ME8E22EZTC5G4" title="Donate to this project using Paypal"><img src="https://img.shields.io/badge/paypal-donate-yellow.svg" alt="PayPal donate button" /></a> if you would like to support the development of this application. </span>

## How to Use
- Open the app and select `File` -> `Open Collection...` and select your Traktor collection. 
- Let the app analyse the collection and the available transitions.
- Drag a file from the song list in Traktor or from Finder into the app to get a list of possible transitions from the song.
- Double-click transitions in the transition list to explore continuous transitions.
- Double-click transition in the transition history to jump back to a previous song.


## Implementation
* The first version of the app consisted of a F# backend handling parsing the Traktor 2 collection and serving results as JSON to the Electron frontend. 
* The second version of the app was implemented in TypeScript and Electron. 
* The third (current) version of the app is implemented in Swift, available for macOS. 
