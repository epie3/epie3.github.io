---
layout: post
title: "SAE Baja Powertrain"
author: "Edward Pieluc"
categories: sample
tags: [documentation,sample]
image: BajaJump.jpg
---
During my first year designing the powertrain for the stevens baja team, the team decided on a full car redesign. Switching from a front braced to rebraced design, and a switch to a transverse engine mounting. With the redesign, we desired to reduce the center of mass of the vehicle to resolve a tipping issue in the previous cars. To do this we moved the prop shaft to the side of the vehicle, so instead of the driver sitting above the propshaft they sit on the floor of the vehicle beside it. 

Once the overall layout/ design changes were identified I started to perform analysis on the overall system to determine the required reduction ratios inside of the powertrain. To do this I performed CFD studies in Ansys Fluent, with a goal of estimating the drag coefficient on the vehicle. After a reasonable estimate was obtained, I developed a set of matlab scripts to simulate the vehicle in a variety of conditions. These scripts found a ideal overall gear ratio for the vehicle
<style>
* {
  box-sizing: border-box;
}

.column {
  float: left;
  width: 50%;
  padding: 5px;
}

/* Clearfix (clear floats) */
.row::after {
  content: "";
  clear: both;
  display: table;
}
</style>

<div class="row">
  <div class="column">
    <img src="{{ site.github.url }}/assets/img/BajaCAD.jpg" alt="PedalArmFEA" style="width:100%">
  </div>
  <div class="column">
    <img src="{{ site.github.url }}/assets/img/CFD.jpg" alt="PedalFEA" style="width:100%">
  </div>
</div>
<img src="{{ site.github.url }}/assets/img/GearboxGraphs.jpg" alt="PedalFEA" style="width:100%">

Transfer Case
One of my later projects while working on the powertrain team, I Started from scratch. The previous team had designed a chain based reduction box, that was inefficient and difficult to service. The team and myself decided to switch to a more traditional gear based transfer case which would be more efficient and easier to service.

Overall requirements for this transfer case included minimizing weight/size, meeting the previously determined ideal overall gear ratio, ease of service and high reliability. I started by performing AGMA gear calculations to find the smallest size set of gears that would fit the required gear ratio. All shafts were then designed, stress calculations and FEA were performed to ensure they would withstand the required loads after the internals of the case were designed, the Case was then drawn. It was designed with the intent to be easily manufactured, with minimal mass and internal volume (this reduces the amount of oil needed for gear lubrication) Appropriate bearings and seals were also chosen and included in the design. 

<img src="{{ site.github.url }}/assets/img/TransferCase.jpg" alt="PedalFEA" style="width:100%">

<div class="row">
  <div class="column">
    <img src="{{ site.github.url }}/assets/img/GearFEA.jpg" alt="PedalArmFEA" style="width:100%">
  </div>
  <div class="column">
    <img src="{{ site.github.url }}/assets/img/AGMA.jpg" alt="PedalFEA" style="width:100%">
  </div>
</div>

<div class="row">
  <div class="column">
    <img src="{{ site.github.url }}/assets/img/OverallPowerTrain.jpg" alt="PedalArmFEA" style="width:100%">
  </div>
  <div class="column">
    <img src="{{ site.github.url }}/assets/img/BevelFEA.jpg" alt="PedalFEA" style="width:100%">
  </div>
    <div class="column">
    <img src="{{ site.github.url }}/assets/img/ShaftFEA.jpg" alt="PedalFEA" style="width:100%">
  </div>
</div>
