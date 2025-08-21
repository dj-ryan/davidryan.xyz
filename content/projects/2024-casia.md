+++
title = "C.A.S.I.A."
date = 2024-01-01
template = "post.html"
draft = false

[extra]
description = "Coordination Among Self-Interested Agents - A simulation exploring multi-agent systems with decentralized coordination"
+++

# C.A.S.I.A
(**C**oordination **A**mong **S**elf-**I**nterested **A**gents)

---

Github [repo](https://github.com/dj-ryan/casia)

---
# Docs
## Abstract
In the realm of multi-agent systems comprised of self-interested agents, the fundamental question revolves around understanding the intricacies of movement coordination. Each agent, functioning as an autonomous entity, is inherently driven by individual goals and preferences. This individualistic motivation introduces a layer of complexity, giving rise to a dynamic environment where collaboration and conflict coexist.

To unravel the mechanisms governing movement coordination, this simulation employs a decentralized approach. The emphasis is placed on investigating how information exchange, consensus algorithms, and adaptive strategies contribute to the overall coordination of agents in their pursuit of individual objectives. The decentralized coordination mechanism serves as a foundational framework for exploring the challenges that arise in such environments.

## Definitions
- **Agent**: An autonomous entity that is capable of making decisions and taking actions.
- **Environment**: The space in which agents operate.
- **Objective**: The goal that an agent is trying to achieve
- **Consensus**: The process of reaching an agreement or common ground among a group of agents.
- **Coordination**: The process of organizing and integrating the actions of agents to achieve a common goal.
- **Decentralized**: A system in which decision-making is distributed among agents, rather than being controlled by a single entity.
- **Self-Interested**: Acting in one's own interest, often without regard for the interests of others.

![Coordination Canvas](/Coordination_among_self-interested_agents_canvas.canvas)
## Swarm Robotics
Swarm robotics is an interesting field of robotics and has included quite a bit of demonstration. However once common theme is that the individual units are operating in a group. They are interested in a common goal.  For example the drone shows that place LEDs on hundreds of drones to display images in the sky. They all have the common goal of making the image. But what if the swarm of robots had two different distinctions?
1. The computation is completely decentralized. Each bot does all of it's own computation and the only network that exists is the communication between individual bots.
2. The bots are selfish. They are not working to a common goal. They are only self interested and.

This would be an interesting concept. As a robot that was much more self-interested would have no incentive to share information. 

However a collection of self-interested parties can benefit from a sharing of information. 

## Application - Self-driving cars
The most obvious application of this scinario would be in the realm of self-driving cars. Each party is only interested in two things possibly a third in some cases
1. The safest commute
2. The fastest commute
3. The most energy efficient commute

This goes along with the three ways any project can be done
1. Done well
2. Done quickly
3. Done cheap

### Example of sharing information among self-interested parties
Lets think about a scenario. Two cars are approaching a two lane 4-way stop intersection. The is one car in the west lane and one car in the south lane. The intersection is blind, as in there is no visibility except once you have reached the intersection. The car in the west lane sees a fast approaching vehicle that would be east to predict is going to blow through the intersection. Even though the car in the south lane has arrived at the intersect first and has the right of way. It would benefit from the information that the other car has. 


---
# Research


## Research papers
[Multi-Agent Path Finding for Self Interested Agents](/18292-Article Text-21808-1-2-20210717.pdf)



---
# Simulation
## v1.0 - Hollow Knight
- 1D environment
    - agents move left or right
- Social credit system
    - The more social credit the more say that you have in justifications 

[branch link](https://github.com/dj-ryan/casia/tree/hollow-knight-v1.0)
### Agent
An acting agent
```c++
class Agent {
private:
    int id;               // unique identifier
    int currentLocation;  // current location
    int targetLocation;   // location the agent wants to go
    int credit;           // total social credit
}
```
### Justification
A plan of action that the agents are able to execute. 
```c++
class Justification {
	vector<int> executionOrder;
public: 

}
```
### Forum
A collection of justifications
```c++
class Forum {
	int location; // location
public: 

}	
```

## v2.0 - Plastic Chip

[link](https://medium.com/agents-and-robots/a-multi-agent-system-in-python-74701f256c3a)

> [!warning] [masa sim python lib](https://mesa.readthedocs.io/en/stable/tutorials/intro_tutorial.html)Look into grid based simple python agent simulation

### Concept

- **Dispenser** - A device that, at a regular intervals, dispenses plastic chips. Dispensers can have different intervals.
- **Chip** - A token with fixed value.
- **Home** - The location that the agent has to bring the chip to receive it's value
- **Social Credit** - The credit that the agent has that allows it to access faster or more valuable dispensers
- **Skill** - A multiplier to the chips that the agent gathers

All agent have a home, a social credit and a skill multiplier.

All dispensers have a distance from the agents home, a dispense rate and a social credit minimum.

All chips are the same value

Dispensers dispense chips of a fixed value and at a fixed rate. They also have a social credit minimum that agents must have so that they can access them. The chips that are dispensed accumulate. The more valuable dispensers are a further distance from the agents homes. 

The agents can go to a dispenser and collect all of the the chips that have accumulated there if they meet the social credit minimum. It can also choose to wait at the dispenser and not take the chips. Every chip that the dispenser makes where the agent does not take them will increase it's social credit. However when the agent decides to take the chips it loses social credit in proportion to how many chips it has taken. The skill multiplier means that some agents can extract more value from the chip. The agent must bring the chips home which costs a time penalty. The farther the dispensary the more the time cost.

## v3.0 - Run Around