---
layout: post
title: Polaris PCB
description: HPRC Line of Custom Flight Computers
image: assets/images/polaris.jpg
nav-menu: true
dates: "06/2021 – 10/2022"
---

In the 2020-21 academic year, WPI's High Power Rocketry Club set out to develop its first custom avionics board: Fusion. The board contained all the necessary sensors, compute power, and peripherals to meet both the launch vehicle’s needs for predictive flight monitoring and airbrake actuation, and the payload’s needs to robotically self-right and level to take a panoramic photo. Although extremely powerful, Fusion proved to be overcomplicated and full of engineering oversights—as one could reasonably expect for the team’s first attempt at designing custom embedded systems. Manufacturing issues, along with the aggressive timeline of the board meant that, at the end of the year, both the rocket and payload were left without a system to provide the functional capabilities they relied on. Since the team was not travelling to competition due to the pandemic, there was no rush to develop a working solution by the end of the academic year which left open an opportunity to integrate the lessons learned and develop a new computer capable of completing the missions.

During the summer of 2021, I decided to take up this effort and create HPRC’s next flight computer, with the mission of getting the previous year’s “Polaris” lander payload  to be fully functional and autonomous. Working with the team’s new avionics group, we developed a set of system requirements and identified candidates for processors, sensors, and any supporting components. As the brains of the computer, the embedded microcontroller would be a key centerpiece of the design and influence almost every other aspect of the board. After the team’s issues designing around the Teensy 3.2 microcontroller, we settled on a more “plug and play” solution. SparkFun’s line of MicroMod products contain a wide range of embedded processors all in the same form-factor which are designed to slot into an M.2 slot while still providing the compute horsepower needed for the predictive modelling needed to control the rocket’s active airbrakes.

This processor decision drove the rest of the design significantly and allowed the new system to have the same footprint as Fusion, making it easily mountable on the already-manufactured electronics sleds. Using Autodesk EAGLE, I proceeded with schematic capture to board design and eventually landed on the first revision seen in the image below. This board contained all the sensors required: barometer for pressure-based altitude and an IMU (accelerometer, gyroscope, and magnetometer) for inertial measurements and, in theory, the design was sound. Once manufactured and assembled, however, issues were found with certain component footprints and assembly processes which required significant rework and lead to latent failure of multiple components. Despite the issues, the board was fully functional and able to provide datalogging and telemetry capabilities for the team throughout the 2021-22 academic year and at the 2022 Spaceport America Cup.

<iframe width="700" height="394" src="https://www.youtube.com/embed/WUrev8juGok" style="display:block;margin:auto;" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="true"></iframe>

Building off the success and shortcomings of the original Polaris PCB, I set out to develop the iteration of the board to meet future launch needs. This board, Polaris 2, not only had a 35% smaller footprint but also had improved mechanical characteristics and inherent reliability along with new sensors that will be available for years to come instead of being discontinued at the time of design and manufacture. This new board also contained a LoRa radio module for transmitting telemetry, providing both datalogging and transmit capability as well. Once design was finalized, a first revision was manufactured, assembled, and subsequently assembled.

<span class="image fit-med"><img src="{% link assets/images/polaris/polaris-2v1.jpg %}" alt="" /></span>

During assembly and testing of the first revision, multiple issues were encountered that rendered the board not for flight. For the second revision, multiple design improvements were implemented such as tented vias, new solder mask specifications for specific component footprints, and design for manufacturability considerations. With this new board, five individual boards were made, tested, and verified to work to flight requirements and have already been serving useful in the team’s ground station tests along with other acquiring data from high power model rocketry launches.

<span class="image fit-med"><img src="{% link assets/images/polaris/polaris-2v2.JPG %}" alt="" /></span>

For details on the third iteration of the board, Polaris 3, visit <a href="{% link projects/4_mqp.md %}">HPR MQP</a>.