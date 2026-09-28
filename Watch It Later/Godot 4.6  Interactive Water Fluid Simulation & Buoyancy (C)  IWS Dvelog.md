---
url: "https://www.youtube.com/watch?v=yfTjq5o6QMA"
tags:
  - "video"
status: "readed"
date: "2026-09-28T14:16:19+08:00"
---
![Godot 4.6 | Interactive Water: Fluid Simulation & Buoyancy (C#) | IWS Dvelog](https://www.youtube.com/watch?v=yfTjq5o6QMA)

https://www.youtube.com/watch?v=yfTjq5o6QMA
无作者 

[章节] Intro

This is a quick preview of the interactive water system for Godot 4.In this demo, I want to show you buoyancy, multiple water bodies, how to customize the look, and different types of water interactions.

[章节] Buoyancy Physics

The first example is buoyancy.I’ve set up four objects with different densities and shapes.This basketball is super light, so it barely makes a splash and just sits on top.The wooden log and crate have some weight, so they float half-submerged.And this anvil is just really heavy, so it sinks straight to the bottom.To make this work, each object is just a standard RigidBody3D.You just drop in a BuoyancyBody component, and it automatically generates voxel pontoons around the collider to handle the math.I also tossed a PointImpactEmitter on them so they actually disturb the water when they move.

[章节] Customizing Water Appearance

For water appearance, I’ve set up two common scenarios.The first is typical clear, transparent water.The second simulates murky river water with more impurities and sediment.You only need to adjust two groups of parameters: Turbidity and RefDepth for visibility,and Shallow Color and Deep Color for the tint.For the clear water, I only increased the RefDepth.This controls how visible the underwater area is and also affects the depth of the blue tone.Turbidity, on the other hand, makes the water look murky and actually increases the surface roughness.So for the river water, I tweaked both of those and pulled some shallow and deep colors from real photos.

[章节] Character Interaction & Chopper Downwash

For character interaction, simply add the CharacterWaterInteraction component to your CharacterBody3D.As your character moves through the water, it automatically creates splashes, wake trails, and pushes foam outward.I also used a DiscPressureEmitter to simulate helicopter downwash,producing continuous circular depressions on the surface.All these disturbances are generated automatically and fed into the GPU ripple simulation.

[章节] Underwater Effects

Finally, the underwater effect is powered by a CompositorEffect in the WorldEnvironment node.It uses a compute shader that reads the scene depth buffer to calculate the waterline per pixel, ensuring it always stays aligned with the animated waves.



--- 由 vCaptions 生成 ---