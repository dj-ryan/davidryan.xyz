+++
title = "Earth Departures"
date = 2023-01-01
template = "post.html"
draft = false

[extra]
description = "Flip-dot display countdown clock for tracking rocket launches with silent electromagnetic actuation system"
+++

# Description 
Around the world there is on average one rocket launch every two days. This is based on 2022 statistics which had the highest rate of launch in history. Currently in 2023 that rate is already higher. Soon rocket launches will be as common as an international flight.  This abundance of departures from earth warrants a way to keep track of them. 

My design will be a flip-dot display to count down the hours until the next earth departure. A flip-dot display is a matrix of electromagnetically actuated "dots" that flip around their axis do display one of two colors. All current designs use an electromagnet perpendicular to the dot that stops the dot from over rotation with a small clicking sound. This means that a continuously updating countdown clock would be noisy. 

The solution to this problem in my design is to orient the electromagnet parallel and inside the dot so that the dot only relies  on the magnetic field to change position and come to a stop which means that it does not come into contact with anything eliminating the noise. 
# Hardware
## Flipper design
[Onshape CAD model](https://cad.onshape.com/documents/fb655a988969d47eb917e3cd/w/1195939c91361ee4f1c738e5/e/18ec0121ca61a6fa3ee6f998?renderMode=0&uiState=66edfd87d573f000db64c86a)

![Earth Departures 1](/20240911_231144.jpg)
![Earth Departures 2](/20240917_222125.jpg)


## Electro-magnet



## Circuitry design
<iframe height="450" width="800" allowfullscreen src="https://www.flux.ai/anavid7/earthdepartures?embed=1&editor=schematic"></iframe>
[Link to flux](https://www.flux.ai/anavid7/earthdepartures?editor=schematic)


# Software
## Font
Custom [4x6 Pixel Font](https://drive.google.com/file/d/10hmenNrMEzQyVrhUjFfZUmd8dKZTgsJa/view?usp=sharing)
Heavily inspired from [this source](https://fontstruct.com/fontstructions/show/1650758/4x6-font)

![Earth Departures Font](/earth_departures_4x6_font.drawio.png)