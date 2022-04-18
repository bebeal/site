---
weight: 1
title: Mastering Doom with DRL
---

# Mastering Doom with DRL

[Doom](https://en.wikipedia.org/wiki/Doom_(franchise)) has always been a favorite game of mine, I played Doom and Doom II on my grandfathers DOS machine as a kid. After digging into neural nets (NN) and deep reinforcement learning (DRL) I learned that there were a multitude of Doom agents being made using DRL techniques, but the issue is that from what I saw, they all pretty much sucked at the game and most of them use very primitive DRL techniques. For reference, the majority of articles/blog posts that you can find online attempting to create an agent that learns to play Doom, either use the very primitive [DQN algorithm](https://deepmind.com/research/open-source/dqn) (which while impressive for it's time has been extremely improved upon and/or outclassed in recent years) and/or use a more complicated algorithm but import their entire solution from a giant library like [stable-baslines-3](https://github.com/DLR-RM/stable-baselines3) and use the default parameters, resulting in ~7 lines of code, 0 understanding of the deeper complexities of the algorithms, and an agent that plays the game like this:

I figured I could make a better agent and this is essentially my (ongoing) attempt.

At first I was surprised that using DRL we could [master games like Atari, Go, Chess](https://deepmind.com/blog/article/muzero-mastering-go-chess-shogi-and-atari-without-rules), and more recently even [*(sorta) solve* one of, if not the, biggest challenges in biology, protein folding](https://deepmind.com/blog/article/alphafold-a-solution-to-a-50-year-old-grand-challenge-in-biology), but yet the same techniques struggled to produce a seemingly intelligent agent on a game from 1993 that you can [play on a pregnancy test](https://twitter.com/Foone/status/1302820468819288066?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1302820468819288066%7Ctwgr%5E%7Ctwcon%5Es1_&ref_url=https%3A%2F%2Fmashable.com%2Farticle%2Fpregnancy-test-doom). But it turns out DRL isn't as stable and straightforward as I naively thought. However, in my opinion, it definitely gets more flak than it deserves from others in the DL community who stricly work on supervised learning solutions with enormous datasets that have papers released every day that include a .01% improvement on performance. With a little tweaking and tuning, DRL can still produce impressive results.

Moreover I wanted to create an agent that plays the game using similar input devices as we humans, like a keyboard and mouse. Because after doing more research into the dissapointing solutions that currently exist I found that most of them only allow the agent to either move around the map and shoot (essentilly playing with no mouse) or they discretize the action space of the mouse into different increments of movement, which I just particularly find a little lame and didn't want to do.

## Doom Background

Just for completion sake if you have no idea what Doom is, it's an FPS game developed in 1993. It has a single player mode that tasks the player with completing multiple episodic missions, fight a variety of enemies, each of which have different abilities, attack ranges, and effects, all while managing supplies of ammunition, health, and armor. It also had a multi-player deathmatch mode where instead of fighting demons you fight other doom agents.

### Enemies
The game has multiple enemies shown here.

### Weapons and Ammo
There a total of X weapons in the game each of which have their own type of ammo that you can find on the ground (walk over the ammo to "pick it up").

### Supplies
There are also health and armor pickups in the game that increase your health and armor each to a maximum of X%. You die if your health reaches 0% and armor effectively acts as extra health. 

## The Environment 
I'll be using [VizDoom](http://vizdoom.cs.put.edu.pl/) which is essentially a contained little Doom emulator that allows for customization and easy control. It also includes a few default "scenarios" that others have used in the past which allows me to benchmark my performance vs theirs. Note that I did configure the environment for my model meaning I changed what buttons were available in the game to use, the rewards given in the scenario, and other configurable options but the main goal or task of each scenario is the same.
An explanation of each scenario is below:

---

### Basic

The purpose of the scenario is just to check if using this framework to train some AI in a 3D environment is feasible.

Map is a rectangle with gray walls, ceiling and floor. Player is spawned along the longer wall, in the center. A red, circular monster is spawned randomly somewhere along the opposite wall. Player can only (config) go left/right and shoot. 1 hit is enough to kill the monster. Episode finishes when monster is killed or on timeout.

REWARDS:

+101 for killing the monster -5 for missing Episode ends after killing the monster or on timeout.

Further configuration:

* living reward = -1,
* 3 available buttons: move left, move right, shoot (attack)
* timeout = 300

---

### Deadly Corridor

The purpose of this scenario is to teach the agent to navigate towards his fundamental goal (the vest) and make sure he survives at the same time.

Map is a corridor with shooting monsters on both sides (6 monsters in total). A green vest is placed at the oposite end of the corridor. Reward is proportional (negative or positive) to change of the distance between the player and the vest. If player ignores monsters on the sides and runs straight for the vest he will be killed somewhere along the way. To ensure this behavior doom_skill = 5 (config) is needed.

REWARDS:

+dX for getting closer to the vest. -dX for getting further from the vest.

Further configuration:

* 5 available buttons: turn left, turn right, move left, move right, shoot (attack)
* timeout = 4200
* death penalty = 100
* doom_skill = 5

---

### Defend The Center

The purpose of this scenario is to teach the agent that killing the monsters is GOOD and when monsters kill you is BAD. In addition, wasting amunition is not very good either. Agent is rewarded only for killing monsters so he has to figure out the rest for himself.

Map is a large circle. Player is spawned in the exact center. 5 melee-only, monsters are spawned along the wall. Monsters are killed after a single shot. After dying each monster is respawned after some time. Episode ends when the player dies (it's inevitable becuse of limitted ammo).

REWARDS: +1 for killing a monster

Further configuration:
* 3 available buttons: turn left, turn right, shoot (attack)
* death penalty = 1

--- 

<br>

I made an overly complex gym wrapper to ease using it and allow for me to more easily control the reward function and observation/action spaces. It is available with the rest of the code on my github if interested.

## The Agent



## References
<table>

<tr valign="top">
<td align="right" class="bibtexnumber">
[<a name="VizDoomSite">1</a>]
</td>
<td class="bibtexitem">
Vizdoom.
 <a href="http://vizdoom.cs.put.edu.pl">http://vizdoom.cs.put.edu.pl</a>.

</td>
</tr>

</table> 