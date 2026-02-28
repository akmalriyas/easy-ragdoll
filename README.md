# 🦴 Easy Ragdoll
**A lightweight, plug-and-play ragdoll system for Roblox humanoids.**

[![Latest Version](https://img.shields.io/badge/version-4-blue.svg)](#)
[![Marketplace Link](https://img.shields.io/badge/Roblox-Marketplace-success)](https://create.roblox.com/store/asset/101543083979831/EasyRagdoll)

Easy Ragdoll provides a seamless way to implement physics-based movement on humanoids. It works by dynamically swapping `Motor6D` joints for `BallSocketConstraints`, supporting both **R15** and **R6** character rigs.

## ✨ Features
* **Universal Support:** Full compatibility with R15 and R6.
* **Bi-directional:** Easily ragdoll and unragdoll characters via script.
* **Physics Impulses:** Built-in support for "push" or "tackle" effects upon ragdolling.
* **Cross-Environment:** Logic handles both Client-side states and Server-side network ownership automatically.

---

## 🚀 Quick Start

### Installation
1.  Get the module from the [Roblox Creator Store](https://create.roblox.com/store/asset/101543083979831/EasyRagdoll).
2.  Place the `EasyRagdoll` module script inside `ReplicatedStorage`.

### Basic Usage
```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local RagdollModule = require(ReplicatedStorage:WaitForChild("EasyRagdoll"))

local character = script.Parent -- Assuming this is inside a character or script referencing one

-- 1. Simple Ragdoll
RagdollModule.SetRagdoll(character, true)

-- 2. Ragdoll with a push (Magnitude 200)
RagdollModule.SetRagdoll(character, true, true, 200)

-- 3. Recover/Unragdoll
RagdollModule.SetRagdoll(character, false)
