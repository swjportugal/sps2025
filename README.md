# SPS 2025 Nuremberg 

SWJ will be showcasing its offerings in embedded Software and Hardware development, Validation & Testing and PMTs. Visit us in Hall 6, Stand 430. 

This repository contains contcat information and technical information for all demos showcased at SPS.

# SWJ at SPS: Daniel Mraß

Angestellt, Projektingenieur, SWJ Germany GmbH
Bonn, Germany

Email: Daniel.Mrass@swj.de

# Our demos at SPS

## NFC Business card

The business card showcases a 0.8mm PCB in the traditional 85x55mm format.

We designed the PCB tracks in a way to create an NFC antenna and added an NFC chip from NXP to provide quick transfer of contact information.
An LED was also added, to give the user the unusuall feedback of failed and successful attempts at NFC communicaiton (short led pulse = failed; long led = succeeded)

Further to this, the team decided to add a "cool" factor to the business card, by creating a sound synthesizer form the classic 555 timer. What better to flex your E/E knwoledge?
You can find the BOM and schematics to populate this circuit and build your own synthesizer here.

## Smart controlled Windmills

The windmill demo shocases a distributed control system with a layred closed loop approach.

This is fully designed by SWJ: mechanics, electronics and software.

At the lowest level, the winmills have a motor with an encoder on the output shaft ( before the reduction box ) to allow precise control of speed.
The lower level control loop commands the speed controller on the motors and continuously senses the real rotation and stall and error conditions.

At the higher level, a control loop was created in CANoe, that collects the current motor status (Speed, errors), and injects dynamic behaviours and reactions into the system.
The demonstration can behave in different, selectable, modes:
* Constant sum of speed: if any windmill is blocked or has its speed reduced, the other windmills and spun up to that the sum of all speeds remains constant within the system
* Follow the leader: by manipulating one windmill, the others will follow (i.e. if you slow it down, the others slow down; if you block, the others block it)
* Winding clock: if you spin up the windmill manually, the others spin up as well, and their speed slowly decays as if winding down a spring

This project is a combination of multiple disciplines:
* EE schamtics: for the Windmill motor drivers and the master STM low level controller (speed)
* Software: embedded software for the STM low level controller (speed), and CANoe high level control
* 3D models: for the windmills and bases
