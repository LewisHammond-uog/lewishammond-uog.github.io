---
layout: default
title: Network Bomberman
modal-id: 12
date: 2020-06-12
img: 2Doods.png
project-date: May 2020 (2nd Year)
role: Progammer
language: C# (Unity)

description: This project is a Networked Version of the game <a href="https://www.youtube.com/watch?v=l-HvJ07lIko">bomberman</a> and was created using OpenGL for rendering and <a href="http://www.jenkinssoftware.com/">Raknet</a> was used for the networking stack. The project uses a authoritative server a dumb client architecture where clients connect and send packets to the server which processes the events in the game world. Up to 6 players can connect to a server and the server owner can set a number of perameters, such as max player and wait timers, as well as the level rotation. Game levels are downloaded from the Server and then are played by the clients. Once a match is completed the clients are prompted to either disconnect or play again.<br><br> The project includes an interpolation technique as recomended in the <a href="http://www.jenkinssoftware.com/raknet/manual/programmingtips.html">RakNet documentation</a>.  This system writes positions that it receives from the server, which dictates the current game state, and interpolates between the time that those messages were sent and the current time to provide the position to the client. This means that if we miss a packet or receive a packet late, we lerp towards a more updated position rather than teleporting. This also means that we don’t need to send a position every frame because we use both time and the position.<br>Dead reckoning is used in addition to this, as inputs from the client are only sent to the server when they change so that if inputs are received late the player simply keeps remaining direction of travel.


summary: A Networked version of the classic local co-op game Bomberman

contribution: I was the programmer in a team of 2, one programmer and one designer, so implemented all of the features present in the game. <br>Features Implemented:<ul><li>3D Movement</li><li>2D Movement</li><li>Transision between 3D and 2D Movement, including the transision of held objects</li><li>Item Pickup</li><li>Interactable Items (i.e Door Opening, Pipe Releveal)</li><li>Water Rising</li><li>Water Visual Effect</li><li>Item Pickup VFX</li></ul>

githubrepo: https://github.com/LewisHammond-uog/FlatGame

video: https://www.youtube.com/embed/FpCJzHtnH1A

---
