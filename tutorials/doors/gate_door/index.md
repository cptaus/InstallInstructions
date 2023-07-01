# Installing Gate door

Inside ```Doors/Gate``` there is the main object of the Office door
```Scripts/DoorInteract.lua``` The main scrip handeling all door access and animations,
### Attributes
1. ```AccessLevel``` = What is the minimum access level player need to have (access card).
2. ```AutoCloseTimer``` = How much time the door will remine open. (this is not working on gates.)
3. ```ReqAccess``` = If checked off, ```AccessLevel``` will be ignored and any card can open this door.

### ```KeyPadA/KeyPadB```
Important part of the door, its for using the access cards, you may place them when ever you want.

### ```Becon```
Will rotate, if you dont want it, drag out of sight, <b>DO NOT DELETE.</b>

### ```InteractionZone```
Important zone checker to check if player have any access card in their hand to show the interaction option