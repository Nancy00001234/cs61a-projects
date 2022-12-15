# Ants Vs. SomeBees

.<img src="https://user-images.githubusercontent.com/104662491/207790389-3b506238-8b5e-4333-ac08-819b1cfb3a89.png" width="450" height="300" />
.<img src="https://user-images.githubusercontent.com/104662491/207789283-36f6e892-22e9-487e-be75-0caee13f0a4d.png" width="450" height="300" />

This project implements a tower defense game similar to Plants Vs. Zombies. Ants(players) protect their territory against the evil bees’ invasion.   
In this game, Bees either try to move toward the end of the territory tunnel or sting ants in their way. As the ant queen, the player **populates** ants' colony with the bravest ants you can muster. Ants perform **different actions** depending on their **type**, such as throwing leaves at the bees. The game **ends** either when a bee reaches the end of the tunnel or ant queen (you lose), or the entire bee flotilla has been vanquished (you win).

## Discriptions
Implement the game utilizing **Object-Oriented Design**:
- Territory   
  - The territory tunnels of ants are formed by multiple connected places, which are instances of a object class, Place.  
  - Methods inside the Place class control ants and bees' appearance, removal, and movement along a tunnel.    
  - The Water class is a subclass of Place. Most types of ants cannot be placed on Water.  
- Insect  
Insect is the parent class of Ants and Bees.
  - Ant   
  16 types of ants are designed through inheritance, multiple inheritance, and attributes override from the Class Ant. They hold different features(armor, damage, etc.) and defense methods(throw leaves, eat bees, stun bees, protect other ants, etc.)  
  - Bee  
  Controls bees' action.
  
## Play the Game
Clone or download (and unzip) the "ants" folder. Then go to the root and type:
```
$ python3 gui.py [-h] [-d DIFFICULTY] [-w] [--food FOOD]
```
```
optional arguments:
  -h, --help     show this help message and exit
  -d DIFFICULTY  sets difficulty of game (test/easy/medium/hard/insane)
  -w, --water    loads a full layout with water
  --food FOOD    number of food to start with when testing
```
To start an older version of the graphics, run
```
$ python3 ants_gui.py [-h] [-d DIFFICULTY] [-w] [--food FOOD]
```

## Directory
```
│  ants.py       // The game logic
│  ants_gui.py   // The original GUI for the game
│  graphics.py   // The original GUI for the game
│  gui.html      // The game interface for gui.py
│  gui.py        // An new GUI for the game
│  mytests.rst   // A space for you to add your custom tests
│  state.py   // Abstraction for gamestate for gui.py
│  ucb.py     // Utility functions for CS 61A
│  utils.py   // Wrapper functions
│  
├─assets  // The frontend of the game
│  │  animate.css
│  │  app.css
│  │  app.js
│  │  enchant.js
│  │  logo.png
│  │  main-background.png
│  │  new-ants-gui.png
│  │  splash.png
│  │  sweetalert.css
│  │  sweetalert.min.js
│  │  swirl_pattern.png
│  │  
│  ├─insects  
│  │      ant_bodyguard.gif
│  │      ant_fire.gif
│  │      ant_harvester.gif
│  │      ant_hungry.gif
│  │      ant_longthrower.gif
│  │      ant_ninja.gif
│  │      ant_queen.gif
│  │      ant_scuba.gif
│  │      ant_shortthrower.gif
│  │      ant_slow.gif
│  │      ant_stun.gif
│  │      ant_tank.gif
│  │      ant_thrower.gif
│  │      ant_wall.gif
│  │      bee.gif
│  │      remove.png
│  │      
│  └─tiles
│      ├─ground
│      │      1.png
│      │      2.png
│      │      3.png
│      │      water.png
│      │      
│      └─sky
│              1.png
│              2.png
│              3.png
│              
├─img
│      ants_vs_bees.png
│      ant_fire.gif
│      ant_freeze.gif
│      ant_harvester.gif
│      ant_hungry.gif
│      ant_laser.gif
│      ant_longthrower.gif
│      ant_ninja.gif
│      ant_queen.gif
│      ant_scuba.gif
│      ant_shortthrower.gif
│      ant_stun.gif
│      ant_thrower.gif
│      ant_wall.gif
│      ant_weeds.gif
│      bee.gif
│      boss.gif
│      collab-demo.png
│      custom_test.png
│      gui_explanation.png
│      hornet.gif
│      new_ants_gui.png
│      ninjabee.gif
│      remover.gif
│      tunnel.gif
│      wasp.gif
│      
├─tests
│      00.py
│      01.py
│      02.py
│      03.py
│      04.py
│      05.py
│      06.py
│      07.py
│      08.py
│      09.py
│      10.py
│      11.py
│      12.py
│      13.py
│      EC.py
│      __init__.py
│      
└─__pycache__
        ants.cpython-310.pyc
        graphics.cpython-310.pyc
        state.cpython-310.pyc
        ucb.cpython-310.pyc
        utils.cpython-310.pyc
```        
