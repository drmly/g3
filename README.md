    XPOST, from a team sub: http://www.reddit.com/r/ProjectDNET/comments/2g4xsr/g3/

g3, or game
=========

* [Initial Concept](#initial-concept)
* [Feedback](#feedback)
* [Ethercraft](#ethercraft)
  * [How to](#how-to)
  * [Message A](#message-a)
  * [Contract: Winderness](#contract-wilderness)

##Initial concept

Is a contract that has a property #start, which has the value of the first message. Which itself is the first item of a linked list of messages.

Add-ons are created by creating a contract that despite its inner working should return a value that corresponds to a message in the above linked list. 
These return values are considered the possible outcomes of the possible actions of the given player.

To add to the game a player must be informed of which contracts (moves) are possible actions to take, to a greater or lesser degree. This informing is done by adding a message to the contacts linked list.

This way the 'game' what ever that might be will forever be editable, verifiable and truly decentralised. What it would or even could become is beyond me.

#Feedback

From [u/avsa on r/ethereum](http://www.reddit.com/r/ethereum/comments/2g4yke/g3_an_ethereum_game/ckg9xv3):


> I don;t really understand the game.. Is it a "build your own rules", [Nomic](http://en.wikipedia.org/wiki/Nomic) game? Is it a "output the input" [Quine](http://en.wikipedia.org/wiki/Quine) competition?

Having thereby just come across the concept of Nomic games, as described by the author in his [Initial Ruleset](http://legacy.earlham.edu/~peters/writing/nomic.htm) It seems as through the framework can be applied to **g3**. I'm still busy processing the implications of such a framework and what the initial ruleset would be under such a system.

#Ethercraft

Is a prototypicical implementation of the currently evolving idea of **g3**, the game, and considered to be the first implemnetation but by no means the last, let alone canonical.

## How to

To start you need a message hash and a contract. Creating a TX with the data: "extend" #contract-address.

Once submitted, a player can call that contract via the genesis contract by creating a TX with data: #contract-address #action [.. params].

The value returned from such a call should equal an existing message hash in the origin contract and the callers address within is changed to this message hash (from this point on thought of as a #state)

The player having just moved states within the context of the genisis node. And also having entered into ideally an initial #state within the the node with which they interacted.

This allows the creation of decentralised nodes representing the current #state of the game at large. Which can easily interact with one another to move players within the game.

##Message A

    The swirling wisps of ether start dissipating just ahead of your field of vision.

    Beyond you can only just make out an empty expanse, a wilderness.

    /enter 

###Contract: wilderness

