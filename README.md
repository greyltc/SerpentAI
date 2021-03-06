![](https://s3.ca-central-1.amazonaws.com/serpent-ai-assets/SerpentFBCover.png)

# Serpent.AI - Game Agent Framework (Python)

[![](https://img.shields.io/badge/project-website-brightgreen.svg?colorB=1bcc6f&longCache=true)](http://serpent.ai)
[![](https://img.shields.io/badge/project-blog-brightgreen.svg?colorB=1bcc6f&longCache=true)](http://blog.serpent.ai)
[![](https://img.shields.io/badge/project-wiki-brightgreen.svg?colorB=1bcc6f&longCache=true)](https://github.com/SerpentAI/SerpentAI/wiki)    
[![](https://img.shields.io/badge/pypi-v2018.1.2-brightgreen.svg?colorB=007ec6&longCache=true)]()
[![](https://img.shields.io/badge/python-3.6-brightgreen.svg?colorB=007ec6&longCache=true)]()
[![](https://img.shields.io/badge/license-MIT-brightgreen.svg?colorB=007ec6&longCache=true)]()  
[![](https://img.shields.io/badge/twitter-@Serpent__AI-brightgreen.svg?colorB=1da1f2&longCache=true)](https://twitter.com/Serpent_AI)

## Bummer: Upstream end of life (November 2018)

#### The upstream development work on the framework has stopped as of some time in August 2018 with an official EOL anncouncement in November 2018. In this fork, I'll attempt to maintain and expand this toolkit because I think it's a fun and interesting project. I'll only develop and test in Arch Linux, which means Windows and Mac are probably already broken here and will likey stay that way unless someone else wants to join in and maintain one or both of those.

Serpent.AI is a simple yet powerful, novel framework to assist developers in the creation of game agents. Turn ANY video game you own  into a sandbox environment ripe for experimentation, all with familiar Python code. The framework's _raison d'être_ is first and foremost to provide a valuable tool for Machine Learning & AI research. It also turns out to be ridiculously fun to use as a hobbyist (and dangerously addictive; a fair warning)!

The framework features a large assortment of supporting modules that provide solutions to commonly encountered scenarios when using video games as environments  as well as CLI tools to accelerate development. It provides some useful conventions but is absolutely NOT opiniated about what you put in your agents: Want to use the latest, cutting-edge deep reinforcement learning algorithm? ALLOWED. Want to use computer vision techniques, image processing and trigonometry? ALLOWED. Want to randomly press the Left or Right buttons? _sigh_ ALLOWED. To top it all off, Serpent.AI was designed to be entirely plugin-based (for both game support and game agents) so your experiments are actually portable and distributable to your peers and random strangers on the Internet.

You'll also be glad to hear that only Arch Linux is supported!

![](https://s3.ca-central-1.amazonaws.com/serpent-ai-assets/demo_isaac.gif)

_Experiment: Game agent learning to defeat Monstro (The Binding of Isaac: Afterbirth+)_

## Background

The project was born out of admiration for / frustration with [OpenAI Universe](https://github.com/openai/universe). The idea is perfect, let's be honest, but some implementation details leave a lot to be desired. From these, the core tennets of the framework were established:

1. Thou shall run natively. Thou shalt not use Docker containers or VNC servers.
2. Thou shall allow a user to bring their own games. Thou shalt not wait for licensing deals and special game APIs.
3. Thou shall encourage diverse and creative approaches. Thou shalt not only enable AI flavors of the month.

_Want to know more about how Serpent.AI came to be? Read [The Story Behind Serpent.AI](http://blog.serpent.ai/the-story-behind-serpent-ai/) on the blog!_

## Documentation

Guides, tutorials and videos are being produced and added to the [GitHub Wiki](https://github.com/SerpentAI/SerpentAI/wiki). It currently is the official source of documentation.

### Installation and Setup
These instructions supersede any installation instuctions found on the upstream project's wiki (linked above). There is no more pyenv, there is no more pip and no more wheels (also no more Windows and no more Mac). Everything is now managed by Arch's package manager, pacman, so we have a one command install for all features:
```
yay -S python-serpent-ai-git # replace yay with your favorite AUR helper
```
This package is for the dev-greyltc branch here. Maybe I'll make a stable release package at some point.

Now you have the `serpent` command. Setup a serpent workspace folder with
```
mkdir serpent_workspace
cd serpent_workspace
serpent setup # just copies some setup files into the cwd
```
and the project is ready to use.

With everything natively compiled for Arch now instead of using precompiled .whl packages, we should in theory, see a performance improvement.

![](https://s3.ca-central-1.amazonaws.com/serpent-ai-assets/demo_ymbab.gif)

_Experiment: Game agent learning to match tiles (You Must Build a Boat)_

