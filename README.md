For full documentation see the original repo: https://github.com/vorg/ciid-simulations-and-artificial-behaviours-2014

## About the project
Data is often cold, hard, and lifeless; finding ways to relate to it, however, can enhance our understanding of our environment.

As part of a one week class, in this one-day project, we created two personifications of real-world data, meant to simulate displays that could be embedded in a watch or wearable device. We focused on giving the data a personality that would determine its behavior.

## Frolicking Bitcoin Sensor
- See the bitcoin sensor in action
- Code
The bitcoin sensor gathers bitcoin values throughout the day (in this example, the day’s worth of data is compressed into a minute). As bitcoin values fluctuate, the moving ball jumps and frolics, outlining the current bitcoin value and recent history. Larger bitcoin values are illustrated through longer “petals”. The spikes on the moving ball add additional vivacious behavior, expanding and contracting to show the size of change in bitcoin value.

## Timid/Assertive Glucose Sensor
- See the glucose sensor in action
- Code
The glucose sensor measures glucose levels of an individual throughout the day (compressed into one minute). The agents that personify the sensor change from timid behavior on low glucose levels, stable behavior on normal glucose levels, and assertive behavior on high glucose levels.

In this case, we aimed to personify extreme glucose levels in ways which would imply a deviance from the norm; low glucose would be too weak, while high glucose would be too strong. The background color parallels the agents’ behavior by moving from a weak to high saturation of red.

## Process
We designed these web-based sensors in javascript, using the paper.js library. 

###Credits:
- Francesca Desmarais
- Paula Te
- paper.js
- vorg
- gauthiier

