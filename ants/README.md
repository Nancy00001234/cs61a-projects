# Ants Vs. SomeBees

.<img src="https://user-images.githubusercontent.com/104662491/207790389-3b506238-8b5e-4333-ac08-819b1cfb3a89.png" width="450" height="300" />
.<img src="https://user-images.githubusercontent.com/104662491/207789283-36f6e892-22e9-487e-be75-0caee13f0a4d.png" width="450" height="300" />

This project implement a tower defense game similar to PopCap Games' Plants Vs. Zombies utilizing Object-Oriented Design. Ants(player) protect their territory against the evil bees’ invasion.   
In this game, Bees either try to move toward the end of the territory tunnel or they sting ants in their way. As the ant queen, the player **populate** ants' colony with the bravest ants you can muster. Ants perform **a different action** depending on their **type**, such as throwing leaves at the bees. The game **ends** either when a bee reaches the end of the tunnel or ant queen (you lose), or the entire bee flotilla has been vanquished (you win).

## Discriptions
- Territory   
  - The territory tunnels of ants are formed by multiple connected places, which are instances of a object class, Place.  
  - Methods of the Place class control ants and bees' appearance, removal, and movement along a tunnel.    
  - The Water class is a subclass of Place. All types of ants except for ScubaThrower can be placed on Water.  
- Insects  
The parent class of all of insects, including Ants and Bees.
  - Ants  
  16 types of ants are designed through inheritance, multiple inheritance, and attributes override from the Class Ant. They hold different features(armor, damage, etc.) and defense methods(throw leaves, eat bees, stun bees, protect other ants, etc.)  
  - Bees
  The Bee class controls bees' action.
  

