# Feudal Sim

Daml templates designed for basic feudal simulation.

### Overview 

Fiefs can be split, and nobles can fight over fiefs.

### Workflow

Initially there should just a single fief, controlled by the king, with all the serfs, and a list of all potential/landless nobles, including the king.

The owner of fiefs can split them, giving one half to another noble and keeping one half for themselves.
Initially that means the king can carve off some kingdom to give to nobles.
The nobles can also split their fiefs to give to other nobles.
Every split, it is decided who gets which serfs.

Nobles can also fight over fiefs.
The winner gets both fiefs (both fiefs' serfs) and the looser is landless.

### Future work

Right now the noble who initiates the fight decides who wins.
That is silly; they would never make themselves loose!
Instead, we should have a third party act as the source of randomness (like a "dungeon master"), and decide who wins.
To do that, we would need to create fight contracts with the designated dungeon master.
In a separate step they would decide the outcome.

### Building
To compile the project
```
$ daml build
```

### Testing
To test all scripts:
Either run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```

### Running
To load the project into the sandbox and start navigator:
```
$ daml start
```
