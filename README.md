# Puzzling Pac-Man: Impact of changing Transition Function in Deep RL
by Weston Ruths

## Demo

[![Demo](https://github.com/tychovdo/PacmanDQN/blob/master/videos/PacmanDQN_wingif.gif)](https://youtu.be/QilHGSYbjDQ)

## Example usage

Run a model on `smallClassic` layout for 15000 episodes, of which 10000 episodes
are used for training. The transition function (the ghosts) will change at the 10000 episode mark
and will switch from a Directional Ghost to a Random Ghost.

```
$ python3 pacman.py -p PacmanDQN -n 6000 -x 5000 -l smallGrid
$ python3 pacman.py -p PacmanDQN -n 15000 -x 10000 -l smallClassic -g DirectionalGhost30 -e RandomGhost --frameTime 0 -q
```

### Layouts
Different layouts can be found and created in the `layouts` directory

### Parameters

Parameters can be found in the `params` dictionary in `pacmanDQN_Agents.py`. <br />
 <br />
Models are saved as "checkpoint" files in the `/saves` directory. <br />
Load and save filenames can be set using the `load_file` and `save_file` parameters. <br />
 <br />
Episodes before training starts: `train_start` <br />
Size of replay memory batch size: `batch_size` <br />
Amount of experience tuples in replay memory: `mem_size` <br />
Discount rate (gamma value): `discount` <br />
Learning rate: `lr` <br />
 <br />
Exploration/Exploitation (ε-greedy): <br />
Epsilon start value: `eps` <br />
Epsilon final value: `eps_final` <br />
Number of steps between start and final epsilon value (linear): `eps_step` <br />

## Acknowledgements
RL Agent by
* [tychovdo](https://github.com/tychovdo/PacmanDQN) ([https://github.com/tychovdo/PacmanDQN](https://github.com/tychovdo/PacmanDQN))

DQN Framework by  (made for ATARI / Arcade Learning Environment)
* [deepQN_tensorflow](https://github.com/mrkulk/deepQN_tensorflow) ([https://github.com/mrkulk/deepQN_tensorflow](https://github.com/mrkulk/deepQN_tensorflow))

Pac-man implementation by UC Berkeley:
* [The Pac-man Projects - UC Berkeley](http://ai.berkeley.edu/project_overview.html) ([http://ai.berkeley.edu/project_overview.html](http://ai.berkeley.edu/project_overview.html))
