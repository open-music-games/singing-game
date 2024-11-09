#

# VOCALUXE (Remake)

## Concept and Game Design Document

Version: 1.0.1
(100% complete)

Written by:

Marwin (Lead / Open Music Games.org)

Last update: 6\. Nov. 2024
Location: Berlin
Status:  In Progress > Done

# CONCEPT

## BASIC SPECS

### Game Name:

Vocaluxe (Remake)

### Genre:

music game, rhythm game, karaoke, sing-along

### Game Elements:

What basic activities will the player be doing for fun?

* Sing alone and collect scores
* Sing with friends together or against each other
* browse and listen to songs
* watch music videos

### Player:

The number of players that can play the game at once

* 1-4 Players

### Inspired by:

SingStar Celebration (2017), Let’s Sing 2023, UltraStar Deluxe (2008)

### Price:

free (non-commercial & open source), yet music have to be buyed in trusted stores

### Planned Release Date:

31th December 2025

### Developer:

Open Music Games Organization (Germany)

### Publisher:

Open Music Games Organization (Germany)

## TECHNICAL SPECS

### Technical Form:

Basically there are 2D graphics (flat) and 3D graphics (form):

* 2D graphics (flat)

### View:

Camera view from which the player will experience the game:

* 3rd Person
* Front, only Screens
* Fixed Camera, no rotation

### Platform:

Cross-Platform, Web-App, Browser, Desktop-App

### Language:

TypeScript, JavaScript, CSS, C#

### Device:

Desktop, Tablet, Mobile

### Engine:

Selfmade Vocaluxe (Remake) Engine

### Frameworks & Libraries:
Recommended are
* Runtime environment: NodeJS
* Framework: Electron
* Front-end framework: ReactJS + SASS
* Task runner: Gulp
* Package manager: npm

### Integrated Developement Environment (IDE):
Recommended are
MS Visual Studio Code, Webstorm, MS Visual Studio Community 2022

## GAME PLAY

### Game Play Outline

Vocaluxe (Remake) is a singing game with boundless possibilities. Players sing along their favorite songs and try to hit notes for points. Feel like a superstar while you break the highscore\! Invite your family and friends to rock the virtual stage together\!

Unlike Singstar or Let’s sing you can use custom songs from your own music collection on pc.There are already a zillion song txt files out there, and in case your favorite song is not yet available, why don't you start creating it yourself and share it with the community?
But customization doesn't stop with your personal song collection. Both games allow extensive theming and skinning or player profiles and avatars. As you can see, the sky is the limit. Make it your game\!
To start: Plug in up to four wireless USB-Microphones into your pc and connect your pc with your tv and your ready for a legendary singing party. For controlling you can use a gamepad or mouse.

### Key Features

Which game elements are the most attractive to the player?

1. **Custom Songs:** the game use the community-grown UltraStar format. players can find many underground songs that are not hyped or charted. they can build a very individual song collection

2. **Scoring:** the game analyzes pitch and rhythm of the voice in real time and gives immediate visual feedback to players how good they sing.

3. **High Score and statistics:** the game collects all scores for each song over time and renders a statistics screen.

4. **Solos, Duets, Groups:** Sing a duet where each player has different lyrics and notes. Or throw a party and sing with many players at the same time.

5. **Music video Background:** while singing and looking at the score players can enjoy the music video as background.

6. **Party modes**: Play multiple rounds or start a knock-out tournament.

7. **Song Queue:** Play multiple songs from the queue without interruption.

8. **Medleys:** Play a shortened mix of songs in the queue.

9. **Individual profile for player:** a player can define a profile and choose an avatar.

10. **Jukebox**: player can use the game as a media player that plays random songs without scoring. This helps to always have background music for the party.

# DESIGN

This document describes how GameObjects behave, how they’re controlled and their properties. This is often referred to as the “mechanics” of the game. This documentation is primarily concerned with the game itself. This part of the document is meant to be modular, meaning you could have several different Game Design Documents attached to the Concept Document.

## DESIGN GUIDELINES

This is an important statement about any creative restrictions that need to be considered and includes brief statements about the general (i.e., overall) goal of the design.

1. Vocaluxe must provide a similar experience like singstar celebration (2017).

2. But it must not be a simple copy, which means:

   1. It must have unique party modes

   2. It must have different visuals and sounds.

   3. Also they must have a good UI for large music collections that can handle over thousands of songs.

3. Vocaluxe must follow the [official ultrastar song format specification](https://github.com/UltraStar-Deluxe/format/blob/main/spec.md) \- a shared standard for all open music games.

4. The game is delivered without songs. This is due general license issues. Players have to get songs on their own discretion from 3rd-parties. A legal proper database is a totally separate project.

## GAME DESIGN DEFINITIONS

This section established the definition of the game play. Definitions should include how a player wins, loses, transitions between modes, and the main focus of the gameplay.

Vocaluxe has these following features:

| **Song Collection** | Custom Songs. Limit is 10.000 songs. |
| :---- | :---- |
| **License** | Open Source, MIT-License |
| **Highscore** | For each song, for each difficulty, for each player |
| **Statistics** | most played songs, songs never played |
| **In Built Store** | No |
| **Files Stored** | Locally |
| **Translations (UI)**  | Czech, Dutch, English, French, German, Hungarian, Italian, Portuguese, Spanish, Swedish, Turkish, Chinese, Japanese |
| **Difficulty levels** | easy, medium, difficult |
| **Theme support** | yes, each game provides customization of look and feel. description below. |
| **Playlist support** | yes (.m3u) |
| **Party modes** | yes: each game has at least 3 different party modes. description below. |
| **Sing modes** | yes: Versus (Duell), Co-Op (Duet), Co-Op 2 (Pass the mic), Medley Duell |
| **Freestyle notes support (F)** | yes |
| **Golden notes support (\*)** | yes |
| **Jukebox mode** | yes, play Songs without scoring, lyrics, and player profiles |
| **Player Profiles** | yes, Player has at least own avatar image, name and individual high score |
| **Song Menu Style** | Grid, each game has different styles of Grid view, but all are grids. |
| **Song Menu Search and Filter** | yes, filter by: year, genre, artist, favorites |
| **Gamepad supported** | yes, xbox controller, Wii-Mote are supported |
| **Smartphone supported** | yes, webbroswer app, AndroidApp, iOS App |
| **Automatic Updates** | yes |
| **Built-In Manual** | yes |
| **Song formats** | UltraStar txt, official UltraStar Song format |
| **Supported text file encodings** | UTF8 |
| **Supported audio containers/formats (file suffix)** | .mp3 (CBR)  .ogg  .wav .opus .m4a .webm |
| **Supported video containers/formats (file suffix)** | MPEG MP4 (.mp4, .m4v) MPEG-1/MPEG-2 (.mpg, .mpeg, .ps) Microsoft Audio Video Interleave (.avi) DivX Media Format (.divx) Google WebM (.webm) Xiph.org Ogg (.ogv) Apple Quicktime (.mov, .qt) Matroska (.mkv) |
| **Supported cover/background filetypes** | JPEG (.jpg) Portable Network Graphics (.png) |

These features totally change the game experience for the players and make the Vocaluxe stand out from other open source singing games:

| Online-Multiplayer | No |
| :---- | :---- |
| **Song Editor** | No in-built song editor |
| **Modification** | No Modification by users |
| **Microphone types** | Classic Microphones |
| **Controlling / UI** | Keyboard and gamepad |
| **Party Modes** | Yes: Tic Tac Toe Mode Challenge mode |
| **Song Grid** | 3x4 (=12 songs per page) |
| **Theming** | choose from a predefined set of 6 themes |
| **Animation of Notes** | static |
| **Option for classic karaoke evening** | No \- only supports classic singstar experience |
| **Max. number of simultaneous singers** | 1-4 Players |
| **Look & Feel** | like singstar celebration (2017) |
| **Rap mode** | Yes, Rap-O-Meter: ignore pitch of notes score only rhythm don’t display normal notes show a Rap-O-Meter  |
| **Practice mode** | No |
| **Collectables and score** | **collect fame, collect medals gold silver bronze**  |

## GAME FLOWCHART

The game flow chart provides a visual of how the different game elements and their properties interact. Game flowcharts should represent Objects, Properties, and Actions present in the game.

### Objects

| 1/n | Objects | Properties | Actions |
| :---- | :---- | :---- | :---- |
| n | **Players** | Player profile | sing throw a party change, add, delete profiles change options play songs in jukebox change, add, delete songs or playlists |
| n | **Player Profiles** | Profile Picture, Name, associated Microphone profile, Favorite songs, Favorite music styles, Profile created (Date), total score of all time, Level (experience), Number of finished songs, Badges | be changed, added or deleted |
| n | **Microphone Profiles** | Device Channel Color | be changed, added or deleted |
| n | **Song Collection** | Songs Playlists Owner File Location | update import export remove |
| n | **Songs** | Over 30 properties According to official UltraStar Song Format standard | be changed, added or deleted |
| n | **Playlists** | Entries: Songs | be changed, added or deleted |
| 1 | **Statistic Database** | Top 5 High Score for each song, for each difficulty, for each singing mode total number of songs Progress singing modes % progress party modes % progress songs completed %, Trophies Top 5 most sung songs Top 5 never sung songs etc….. | update import export reset |
| 1 | **Option Config** | Over 30 properties | be changed |

### Screens

| Layer 1 | Layer 2 | Layer 3 | Layer 4 | Layer 5 | Layer 6 |
| ----- | ----- | ----- | ----- | ----- | ----- |
|  **Loading & Title** |  **Main Menu** | **Singing Modes:** Duel, Duet, Medley, Practice, Rap |  | **Song Selection and Player Selection and High Score** |  **Sing Screen and Rating**  |
|  |  | **Party Modes** Party Mode 1 Party Mode 2 Party Mode 3 | **Party Mode Subscreens** |  |  |
|  |  | **Jukebox Mode** |  |  |  |
|  |  | **Statistics** |  |  |  |
|  |  | **Playlists (aka Mixtapes)** |  |  |  |
|  |  | **Options** |  |  |  |
|  |  | **Profiles** |  |  |  |
|  |  | **Credits** |  |  |  |
|  |  | **Manual** |  |  |  |
|  |  | **~~Community~~** |  |  |  |
|  |  | **~~Store~~** |  |  |  |

## PLAYER DEFINITION

### Player Definitions

A suggested list may include: Health, Weapons, Actions

* A player is a singer.

* By using his or her voice he can collect points. The better the player gets (and/or the longer the player plays) the more bonus items and features she unlocks during the game.

* A player designs a profile for himself by choosing an Artist name and avatar plus selecting favorite songs and music genres.

### Player Properties

Each property should mention feedback as a result of the property changing.

* High Score \- get High score when singing a song

* Profile Picture

* Name

* Microphone

* Favorite songs

* Favorite music styles

* Profile created (Date)

* total score of all time

* Level (experience) \- increased by total score

* Number of finished songs

### Player Rewards

Make a list of all objects that affect the player in a positive way (e.g., health replenished)

The better the player sings, the better the feedback of the game.

* A player is rewarded with rating pop ups, glitter effects, filled note bars right on the sing screen.

* On Rating screen: If the score raises, the applause sound effects gets more intense and the background music gets more uplifting.

* If the total score of a player increases there is a level-up. A Level Up allows a player to add more favorite songs to his or her profile.

* In this game the player makes continuous progress, there’s no throwback. If someone sings good he or she progresses faster.

## USER INTERFACE (UI)

This is where you’ll include a description of the user’s control of the game. Think about which buttons on a device would be best suited for the game. A visual representation can be added where you relate the physical controls to the actions in the game.
The whole games consist of UI, HUD, Visual effects, Transition effects, and music videos. There’s no world and no player avatar moving. The player navigates through a big menu with several layers, screens and sub screens.

Vocaluxe focuses on the Keyboard / Gamepad.

## STYLE GUIDELINES

How should the game look & Sound? Even if players can customize the look of the game it needs good original design in the first place. We set these guidelines to make the game stand out:

Theme:
Pop colorful, contemporary music tv
Backgrounds:
Flat, abstract, geometric, animated
Background Music:
calm, motivating, pop
Avatars:
Realistic with an animelike western style (3:2)

# TEAM / CREDITS

We need a proper designated team.

|  | Vocaluxe |
| :---- | ----- |
| Production |  |
| Project Leader / Owner | [Marwin](https://github.com/marwin89) (2023-today) |
| Project and Team Manager | [Marwin](https://github.com/marwin89) (2023-today) |
| Maintainer | Florian (2013-today) |
| Gameplay Design |  |
| Design Director  | Florian Marwin |
| Original Concept / Idea  |  |
| Game Play Design |  |
| Party Mode Design | Alexander Eckhart (2011-2015) Florian (2013-today) |
| Programming / Engineering |  |
| Technical Director |  |
| Software Engineer |  |
| Programmer |  |
| QA Programmer |  |
| Art / Graphics |  |
| Art Director |  |
| Graphics Artist | [Marwin](https://github.com/marwin89) (2023-today) |
| UI / HUD Designer |  |
| Visual effects |  |
| Animator |  |
| Illustrator |  |
| Sound / Music Designer | [Marwin](https://github.com/marwin89) (2023-today) |
| Audio Producer | Ivymusic |
| QA Team |  |
| QA Manager |  |
| Tester |  |
| Localization Testing |  |
| Technology |  |
| Website Developer |  |
| Webmaster |  |
| Tools |  |
| Localization |  |
| Localization |  |
| Localization Supervisor |  |
| Translator: Chzech |  |
| Translator: Chinese |  |
| Translator: Dutch |  |
| Translator: French |  |
| Translator: German |  |
| Translator: Hungarian |  |
| Translator: Italian |  |
| Translator: Japanese |  |
| Translator: Portoguese |  |
| Translator: Spanish |  |
| Translator: Swedish |  |
| Translator: Turkish |  |

# APPROVALS

Following Project Owner approved this Game Design Document:

| Approval | Status | Date |
| :---- | :---- | :---- |
| Marwin(Open Music Games Lead) | Genehmigt |  |
| Florian(Vocaluxe Maintainer) | Nicht gestartet |  |

# CONTACT

Mail:
[contact@open-music-games.org](mailto:contact@open-music-games.org), [join@open-music-games.org](mailto:join@open-music-games.org)

Website:
[open-music-games.org](http://www.open-music-games.org)

GitHub:
[github.com/open-music-games](https://github.com/open-music-games)
