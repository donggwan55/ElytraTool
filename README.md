# ElytraTool
#Use extra tools instead of firework rockets during Elytra flight

command /push [<player>]:
  permission: push.player
  trigger:
    if arg-1 is not set:
      send "&cUsage: /push (player)" to player
    if arg-1 is set:
      push arg-1 forwards at speed 1.1
      send action bar "rocket ~left!" to player
	  
on right click:
    if player's tool is stick named "Firework":
        make player execute command "push %player%"

