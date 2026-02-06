# Road Building with an Agent Based Model for Netlogo 7.0.0

This is the repository for **Road Building 0.2**, an agent-based model built in Netlogo designed to simulate how roads and pathways may develop over time. This model is the culmination of the 2025/2026 "Agent Based Modelling for Archaeologists" (https://github.com/CoDArchLab-ABM/course-guide/tree/main). As such it is a student project designed to help teach agent based modelling and coding.

## Download

To access the model, simply download it from the repository.

## Model Description

<img width="604" height="347" alt="visual concept" src="https://github.com/user-attachments/assets/6dc9071c-add9-460e-a2c3-c0b475534142" />

Taking the concept for the idea of a 'least cost path' which is now commonly employed in software like GIS, the idea of the model is Trader agents to find the least costly path from their home settlement and the settlement with which they wish to trade. This is referred to as **pathCost** inside the model, the higher the pathCost value the more costly the movement. With each run each Trader will evaluate the possible travel options they have and try and take the least costly path that will bring them closer to their target.

**pathCost** is increased by great height, deep ravines, and the precence of rivers or trees.

<img width="322" height="323" alt="road-buildin1" src="https://github.com/user-attachments/assets/9a232c00-b71a-4f9e-bcb1-8375d7a9803e" />

There is also **roadValue**. The **roadValue** of each patch is 0 at the beginning of each model run, but as a Trader moves over a patch they will very slightly increase the **roadValue**. This is intended to represent the developed of preferred pathways or roads over time, and the more a path or road is used the more familiar it becomes. In this manner the Traders naturally create roads across the landscape which reduce the **pathCost**. These roads can be used by any Traders, not just the one that created them.

<img width="320" height="321" alt="road-buildin2" src="https://github.com/user-attachments/assets/529df5ff-f0c4-4f89-9e91-e89d71000c0e" />

## Upcoming & Planned Features

Currently there is a basic economy system where trader will attempt to trade with the most profitable settlement. This is incredibly simple, with each trade the value of each settlement going up. I would like this to be a more prominent feature of model so the planned features are as follows:

- Decay values for both **roads** and **settlements**
- The number of Traders bound to a settlement to be based incrementally on the **value of that settlement**
- Cap the maximum roadValue a single patch can have, but to independantly record **how often each patch has been travelled**. Which may prove useful for analysis after the fact.

