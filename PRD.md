# 🏎️ DRIFT KINGS: UNLEASHED

### Product Requirements Document (PRD) — Open Source Game Design

---

## 💙 The Story Behind This Game

**This game was entirely designed by Albert, a 10-year-old boy.**

It's always been Albert's dream to have his own video game — not just to play one, but to *create* one. He sat down, thought about everything he'd want in the ultimate driving game, and wrote out his vision. Every single feature in this document comes directly from his imagination.

No professional game designers. No focus groups. No market research. Just a kid called Albert who knows exactly what would make the most fun game in the world.

His mum helped bring his vision to life in this document, but the ideas — every car, every map, every cheeky NPC conversation, every tameable cat — are entirely his.

**This project is open source because great ideas deserve to be shared.** If you're a developer, artist, designer, or just someone who loves games — you're welcome to help make Albert's dream a reality. Whether you build the whole thing, use parts of it in your own project, or just get inspired by a 10-year-old's creativity — that's a win.

*Dreams don't have an age requirement.*

---

## 📋 Table of Contents

- [1. Product Overview](#1-product-overview)
- [2. Target Audience & Platform](#2-target-audience--platform)
- [3. World Design](#3-world-design)
- [4. Vehicle System](#4-vehicle-system)
- [5. On-Foot Gameplay & AI Conversations](#5-on-foot-gameplay--ai-conversations)
- [6. Pet & Animal Companion System](#6-pet--animal-companion-system)
- [7. Multiplayer & Lobby System](#7-multiplayer--lobby-system)
- [8. Day/Night Cycle & Weather](#8-daynight-cycle--weather)
- [9. Fuel System (Optional Toggle)](#9-fuel-system-optional-toggle)
- [10. Graphics & Audio Requirements](#10-graphics--audio-requirements)
- [11. Progression & Rewards](#11-progression--rewards)
- [12. Technical Architecture](#12-technical-architecture)
- [13. Post-Launch Roadmap](#13-post-launch-roadmap)
- [14. User Stories](#14-user-stories)
- [15. Acceptance Criteria](#15-acceptance-criteria)
- [16. Contributing](#16-contributing)
- [17. Licence](#17-licence)

---

## 1. Product Overview

### 1.1 Elevator Pitch

**Forza Horizon meets MudRunner meets The Sims** — with cheeky talking NPCs and tameable pets.

Players drop into a stunning, hyper-realistic open world where they can race sports cars through neon-lit city streets, wrestle mud trucks through swamps, drift rally cars sideways through mountain passes, and tear up dirt tracks on motorbikes. Between races, they walk around on foot, chat with hilarious AI characters, adopt cats and dogs, and hang out with up to 20 mates in shared lobbies. The world runs on real UK time with gorgeous day/night cycles, and players choose whether they want the hardcore challenge of managing fuel levels or just pure, chaotic fun.

### 1.2 Core Design Pillars

| Pillar | Description |
|--------|-------------|
| **Drive Anything, Anywhere** | From a Lamborghini on a neon highway to a mud truck axle-deep in a bog — every vehicle feels completely different and utterly satisfying |
| **Cheeky Conversations** | Walk up to any NPC and have a proper chat. They're funny, they're rude (in a kid-friendly way), and they remember what you said last time |
| **Your World, Your Rules** | Toggle fuel simulation on or off. Play solo or with 20 friends. Race at midnight under real UK stars or at noon in blazing sunshine |
| **Pets That Love You Back** | Tame cats and dogs that ride in your passenger seat, react to your driving, and have their own personalities |
| **Endlessly Fresh** | Maps that procedurally repeat but never feel the same twice, with dynamic weather, traffic, and events |

### 1.3 Game Identity

| Attribute | Detail |
|-----------|--------|
| **Title** | Drift Kings: Unleashed |
| **Genre** | Open-World Racing / Sandbox / Social Simulation |
| **Tone** | Hyper-realistic visuals with cheeky, warm British humour |
| **Rating Target** | PEGI 7 / ESRB E10+ |
| **Monetisation** | Premium (one-time purchase). No loot boxes. No pay-to-win. Free seasonal content updates |

---

## 2. Target Audience & Platform

### 2.1 Primary Audience

- **Age range:** 7–35
- **Player types:** Casual racers, car enthusiasts, sandbox explorers, social gamers, pet lovers
- **Accessibility:** The toggle-based design (fuel on/off, time override, solo/multiplayer) means the game adapts to any skill level

### 2.2 Platform Targets

| Platform | Priority | Notes |
|----------|----------|-------|
| PC (Windows) | P0 — Launch | Primary development platform |
| PlayStation 5 | P0 — Launch | DualSense haptics for terrain feedback |
| Xbox Series X/S | P0 — Launch | Smart Delivery for both consoles |
| Nintendo Switch 2 | P1 — Post-launch | Scaled visuals, portable play |
| Steam Deck | P1 — Post-launch | Verified compatibility target |

---

## 3. World Design

### 3.1 The Three Endless Maps

The game world is split into three massive, interconnected biomes. Each map is "endless but repeating" — the road stretches on forever using a procedural tile system that remixes terrain, obstacles, shortcuts, and scenery so it always feels fresh even though the core layout loops.

#### 🟤 Mud Map

| Attribute | Detail |
|-----------|--------|
| **Inspiration** | Scottish Highlands, Welsh valleys, MudRunner |
| **Terrain** | Deep bogs, river crossings, forest trails, fallen trees, mudslides |
| **Weather** | Rain is near-constant. Thick fog. Occasional thunderstorms |
| **Best vehicles** | Mud trucks, rally cars, dirt bikes |
| **NPC flavour** | Grizzled farmers, lost hikers, a man who's been stuck in the mud for "three days" |
| **Fun fact** | Sports cars *can* enter this map. They will get hilariously stuck. NPCs will laugh at you |

#### 🟠 Drift Map

| Attribute | Detail |
|-----------|--------|
| **Inspiration** | Japanese touge mountain passes, Initial D, Swiss alpine roads |
| **Terrain** | Winding mountain passes, hairpin bends, cliffside roads, tunnels |
| **Scenery** | Cherry blossom trees, neon-lit tunnels, spectator areas |
| **Best vehicles** | Sports cars, rally cars, motorbikes |
| **NPC flavour** | Cheering (or heckling) spectators, a self-proclaimed "drift master" who can't actually drive, a cat café owner at the summit |
| **Fun fact** | Mud trucks technically work here. The NPCs will absolutely roast you for it |

#### ⚫ Street Map

| Attribute | Detail |
|-----------|--------|
| **Inspiration** | London, Tokyo, and Los Angeles mashed together |
| **Terrain** | Motorways, backstreets, car parks, tunnels, a proper high street with shops |
| **Atmosphere** | Night time transforms it with neon and street lights |
| **Best vehicles** | Sports cars rule. Bikes weave through traffic |
| **NPC flavour** | Café owners, mechanics, a bloke convinced his hatchback is faster than your supercar |
| **Fun fact** | Mud trucks cause absolute chaos here. NPCs comment on it. Cats scatter |

### 3.2 Seamless Map Transitions

All three maps connect without loading screens:

```
Mud Map ──── Country Road ────► Street Map
   ▲                                │
   │                                │
Mountain Pass                  Tunnel System
   │                                │
   └──────── Drift Map ◄────────────┘
```

### 3.3 Procedural "Endless But Repeating" System

- **Core loop length:** ~15–20 minutes of unique driving per map
- **Remix system:** Each loop shuffles obstacle placement, NPC locations, animal spawns, weather, traffic density, and shortcuts
- **Landmark anchors:** Key locations (garages, cafés, pet shelters) stay fixed for navigation
- **Difficulty scaling:** Terrain challenge increases the further you drive from the hub

---

## 4. Vehicle System

### 4.1 Vehicle Categories

| Category | Examples | Handling | Personality |
|----------|----------|----------|-------------|
| **Sports Cars** | Supercars, hypercars, JDM legends, classic muscle | Razor-sharp, fast, punishing if overcocked | NPCs whistle and take photos |
| **Mud Trucks** | Monster trucks, lifted 4x4s, military surplus | Heavy, slow to turn, unstoppable in mud | NPCs step back nervously. Dogs bark |
| **Rally Cars** | WRC hatchbacks, Group B legends, rally SUVs | Twitchy, slides beautifully, needs correction | Work everywhere, master of none |
| **Motorbikes** | Superbikes, dirt bikes, café racers, scooters | Lightning quick, vulnerable, lean steering | NPCs gasp at wheelies. Cats ignore you |

### 4.2 Vehicle Customisation

- Paint jobs, wraps, decals, and custom livery design
- Body kits, spoilers, bumpers, wide-body conversions
- Wheels, tyres, suspension (visual and performance)
- Engine tuning, exhaust sound, turbo/supercharger options
- Interior mods (dashboard ornaments, seat covers, steering wheels)
- **"Mud-O-Meter"** showing vehicle dirtiness — wash at car washes or embrace the filth

### 4.3 Vehicle Physics Requirements

| System | Requirement |
|--------|-------------|
| **Tyre model** | Per-tyre simulation with grip, temperature, deformation |
| **Mud physics** | Volumetric mud that deforms, fills tyre treads, slows vehicles |
| **Water** | Puddle splash, river fording, hydroplaning |
| **Damage** | Visual + mechanical — dents, scratches, cracked glass, reduced performance |
| **Bike physics** | Lean steering, low/high-side crashes, wheelie/stoppie mechanics |

---

## 5. On-Foot Gameplay & AI Conversations

### 5.1 Third-Person Walking Mode

Players exit any vehicle at any time and walk around in third person. On foot, they can explore garages, shops, cafés, pet shelters, lookout points, and hidden areas vehicles can't reach.

### 5.2 AI Conversation System — The Heart of the Game

**Every NPC in the world can be talked to.** Walk up, press interact, and a full AI-powered conversation begins.

#### Conversation Design Principles

| Principle | Detail |
|-----------|--------|
| **Tone** | British banter meets cartoon humour. Kid-friendly but genuinely funny for adults. Sass, sarcasm, ridiculous observations — no swearing |
| **Context-aware** | NPCs comment on your vehicle, driving history, weather, pets, and nearby players |
| **Memory** | NPCs remember previous conversations within a session and build running jokes |
| **Reactive** | NPCs respond to real-time events — if someone crashes nearby, the NPC comments on it |

#### NPC Archetypes

| Type | Location | Personality |
|------|----------|-------------|
| **Mechanics** | Garages | Gruff, helpful, will roast your vehicle choices |
| **Café Owners** | Rest stops | Cheery gossips who know everyone's business |
| **Spectators** | Drift viewing areas | Enthusiastic or hilariously unimpressed |
| **Pet Shelter Volunteers** | Shelters | Guilt-trip masters. "That cat's been waiting…" |
| **Random Pedestrians** | Everywhere | Mundane problems, strong opinions, zero filter |

#### Example Conversation

> **Mechanic:** "Alright! What's the damage? And I mean that literally — your bumper's hanging off."
>
> **Player option:** "It's a style choice."
>
> **Mechanic:** "Yeah? Well your 'style choice' is dragging on the road and scaring the cats."

### 5.3 Player-to-Player Conversations

When two human players walk up to each other, the AI conversation system generates cheeky commentary and banter prompts. Players can challenge each other to races, trade vehicle designs, or just mess about.

---

## 6. Pet & Animal Companion System

### 6.1 Tameable Animals

Cats and dogs roam freely across all three maps. Players earn their trust through a taming mini-game (offering food, gentle interaction).

| Pet | Where Found | In-Vehicle Behaviour | Personality |
|-----|-------------|---------------------|-------------|
| **Cats** | Walls, cafés, near warm engines | Sit on dashboard. Purr when slow, meow when drifting, yowl and glare when crashing | Independent, judgemental, occasionally helpful |
| **Dogs** | Parks, shops, pet shelters | Passenger seat or truck bed. Head out window, bark at speed, wag at cool moves | Enthusiastic about everything, bark at mud trucks |

### 6.2 Pet Features

- Pets ride in your vehicle with reactive animations
- Each pet has a unique name, personality traits, and appearance
- Pets can be dressed up (tiny hats, bandanas, sunglasses)
- NPCs comment on your pets ("That cat is definitely judging me")
- Maximum 3 active companions (mix of cats and dogs)
- "Pet Home" in each map for extra pets between adventures

---

## 7. Multiplayer & Lobby System

### 7.1 Main Lobby

A stylish garage/hangout area for vehicle customisation, pet management, settings, and seeing friends online.

### 7.2 Game Lobbies

| Feature | Detail |
|---------|--------|
| **Max Players** | 20 per lobby |
| **Lobby Types** | Public (open), Private (invite-only), Solo (you + NPCs) |
| **Host Controls** | Map selection, fuel toggle, time override, vehicle restrictions, weather lock |
| **Activities** | Free roam, races (point-to-point/circuit), drift comps, mud challenges, hide & seek, convoy runs |
| **Voice Chat** | Proximity-based (louder as you approach) |
| **Text Chat** | With quick-emote wheel |
| **Interactions** | Challenge to races, trade designs, honk repeatedly |

---

## 8. Day/Night Cycle & Weather

### 8.1 Real UK Time

The game runs on live UK time (GMT/BST). 10pm in London = 10pm in-game.

- **Night:** Headlights cut through darkness, neon-lit streets, mud tracks barely visible
- **Day:** Golden hour sunsets, morning fog, midday heat haze
- **Override:** Players can lock to permanent day or night in settings

### 8.2 Dynamic Weather

| Condition | Effect on Driving | Visual Impact |
|-----------|-------------------|---------------|
| **Rain** | Reduced grip, hydroplaning, puddles | Wet reflections, wipers, spray from tyres |
| **Fog** | Limited visibility | Volumetric fog, headlight scatter |
| **Thunderstorm** | Heavy rain + wind gusts | Lightning strikes, dramatic skies |
| **Snow** (seasonal) | Ice physics, sliding | White-out, tracks in snow |
| **Clear** | Optimal grip | Sharp shadows, heat shimmer |

---

## 9. Fuel System (Optional Toggle)

**Toggled ON or OFF in the main menu before joining a session.**

### Fuel ON (Simulation Mode)

- Vehicles consume fuel realistically based on engine size and driving style
- Different tank sizes per vehicle (mud trucks = thirsty, bikes = sippers)
- Petrol stations scattered across all maps
- Running out = walking or getting towed by a mate
- Adds strategic depth to long runs

### Fuel OFF (Arcade Mode)

- Unlimited fuel
- Pure fun, no consequences, just vibes

---

## 10. Graphics & Audio Requirements

### 10.1 Visual Quality Target

Hyper-realistic visuals on par with Forza Motorsport / Gran Turismo, plus real-time mud deformation. Every screenshot should look like a photograph.

| Element | Requirement |
|---------|-------------|
| **Lighting** | Ray-traced global illumination, realistic wet-road reflections, volumetric fog, god rays |
| **Materials** | PBR on every surface. Mud looks thick and wet. Metal shines. Rubber deforms |
| **Vehicles** | Full interior modelling, working dials/mirrors, damage with dents/scratches/cracked glass |
| **Environment** | Dense foliage, realistic water, dynamic clouds, detailed city streets |
| **Animals** | Motion-captured animations, fur rendering, personality through body language |

### 10.2 Audio Design

| Element | Requirement |
|---------|-------------|
| **Engines** | Sampled from real vehicles. Each sounds unique. Exhaust pops, turbo flutter, supercharger whine |
| **Environment** | Rain on metal, tyres on gravel, mud squelching, wind, distant shop music |
| **NPC Voices** | AI-generated with distinct character. British accents encouraged |
| **Music** | Dynamic soundtrack: electronic in city, folk-rock in mud, synthwave on drift map |

---

## 11. Progression & Rewards

### 11.1 XP System

Players earn XP for racing, drifting, exploring, taming animals, conversations, helping players, and spectacular crashes ("Well, That Happened" bonus). XP unlocks vehicles, customisation, pet accessories, and conversation topics.

### 11.2 Achievements & Challenges

- **Daily:** "Drift 500m continuously", "Tame a cat in the rain"
- **Map milestones:** "Complete the Mud Map loop without getting stuck"
- **Social:** "Have 50 different NPC conversations", "Convoy with 10 players"
- **Hidden:** "Find all 100 hidden cat statues"
- **Silly:** "Bring a sports car into the mud map and regret everything"

---

## 12. Technical Architecture

### 12.1 Engine & Infrastructure

| Spec | Target |
|------|--------|
| **Engine** | Unreal Engine 5 (Nanite + Lumen) |
| **Frame Rate** | 60fps Performance / 30fps Quality (max ray tracing) |
| **Resolution** | 4K native (Quality), Dynamic 4K (Performance), 1080p (min PC) |
| **AI Conversations** | On-device language model with cloud fallback |
| **Networking** | Dedicated servers for 20-player lobbies, P2P fallback |
| **Physics** | Custom vehicle physics: tyre deformation, mud simulation, water dynamics |
| **Map Streaming** | Seamless between biomes, zero loading screens during play |

### 12.2 AI Conversation Architecture

```
┌─────────────────┐     ┌──────────────────┐     ┌─────────────────┐
│  Player Input    │────►│  Context Engine   │────►│  Response Gen   │
│  (text/choice)   │     │  (vehicle, pets,  │     │  (personality,  │
│                  │     │   weather, history)│     │   humour, tone) │
└─────────────────┘     └──────────────────┘     └─────────────────┘
                                                          │
                                                          ▼
                                                  ┌─────────────────┐
                                                  │  NPC Animation  │
                                                  │  (lip sync,     │
                                                  │   gestures,     │
                                                  │   expressions)  │
                                                  └─────────────────┘
```

- **Context window** includes: current vehicle, vehicle condition, pet companions, weather, time of day, recent driving events, conversation history, nearby players
- **Personality layer** ensures each NPC archetype has consistent voice and humour style
- **Safety filter** maintains PEGI 7/E10+ rating at all times

---

## 13. Post-Launch Roadmap

### Year 1 — Free Seasonal Updates

| Season | Theme | Content |
|--------|-------|---------|
| **S1** | ❄️ Snow Day | Winter weather, ice physics, snowmobiles |
| **S2** | 🏖️ Beach Run | Coastal map extension, sand physics, jet skis |
| **S3** | 🚜 Farm Life | Rural expansion, tractors, barn finds, horse companions |
| **S4** | 🌙 Night Shift | Underground racing, neon upgrades, nocturnal animals |

### Community Features

- **Track Editor:** Build and share custom race routes
- **Livery Marketplace:** Share and download vehicle designs
- **Photo Mode:** Camera with filters, angles, and pet posing
- **Replay System:** Save and edit best moments

---

## 14. User Stories

### Core Experience

| ID | As a... | I want to... | So that... |
|----|---------|-------------|------------|
| US-01 | Player | Choose between sports cars, mud trucks, rally cars, and bikes | I can drive whatever suits my mood |
| US-02 | Player | Walk up to any NPC and have a funny conversation | The world feels alive and entertaining |
| US-03 | Player | Tame cats and dogs that ride with me | I have companions that react to my adventures |
| US-04 | Player | Drive seamlessly between mud, drift, and street maps | The world feels massive and connected |
| US-05 | Player | Toggle fuel simulation on or off | I can choose simulation depth |
| US-06 | Player | Play in real UK time with day/night cycles | The game world feels real and immersive |
| US-07 | Player | Join lobbies with up to 20 friends | We can race, explore, and mess about together |
| US-08 | Player | Customise every aspect of my vehicles | My cars feel uniquely mine |

### Social

| ID | As a... | I want to... | So that... |
|----|---------|-------------|------------|
| US-09 | Host | Control lobby settings (map, fuel, weather) | I create the experience I want |
| US-10 | Player | Walk up to other players and interact | Multiplayer feels personal, not just racing |
| US-11 | Player | See NPCs react to my vehicle, driving, and pets | Every session feels unique and personalised |

### Progression

| ID | As a... | I want to... | So that... |
|----|---------|-------------|------------|
| US-12 | Player | Earn XP for everything I do | All playstyles feel rewarding |
| US-13 | Player | Complete silly achievements | I have goals that make me laugh |
| US-14 | Player | Discover hidden secrets across the maps | Exploration always feels rewarding |

---

## 15. Acceptance Criteria

### P0 — Must Have for Launch

- [ ] All four vehicle categories playable with distinct physics
- [ ] Three endless maps with seamless transitions
- [ ] AI conversation system with context-aware, cheeky NPC dialogue
- [ ] Cat and dog taming with in-vehicle companion behaviour
- [ ] 20-player lobbies with host controls
- [ ] Real UK time day/night cycle
- [ ] Fuel toggle (on/off)
- [ ] Vehicle customisation garage
- [ ] Hyper-realistic graphics (ray tracing, PBR, damage modelling)
- [ ] Dynamic weather affecting driving physics
- [ ] Proximity voice and text chat
- [ ] XP and achievement system

### P1 — Fast Follow

- [ ] Photo mode
- [ ] Track editor
- [ ] Livery marketplace
- [ ] Pet accessories (hats, bandanas, sunglasses)
- [ ] Replay system

### P2 — Future

- [ ] Season 1–4 content drops
- [ ] Additional vehicle categories
- [ ] New map biomes
- [ ] Additional pet species

---

## 16. Contributing

This is an open source game design. Everyone is welcome to contribute.

### How You Can Help

- **Game Developers:** Pick up features from the acceptance criteria and build them
- **Artists:** Create concept art, 3D models, or UI designs based on this PRD
- **Writers:** Help write NPC dialogue — keep it cheeky, British, and kid-friendly
- **Sound Designers:** Engine recordings, ambient sounds, music
- **Testers:** When builds are available, test and report bugs
- **Ideas:** Open an issue with suggestions — if a 10-year-old's idea made it this far, yours can too

### Ground Rules

1. **Keep it kid-friendly** — PEGI 7 / E10+ at all times. Cheeky humour, not offensive
2. **Stay true to Albert's vision** — This is a young designer's dream. Respect it
3. **Be kind** — To each other, to the code, and to the cats on the dashboard
4. **Have fun** — If you're not having fun building this, something's gone wrong

---

## 17. Licence

This game design document is released under the **MIT Licence**.

You're free to use, modify, and distribute this design. Build the whole game. Use parts of it. Get inspired. Just credit the original designer — Albert, age 10, a young man with a big dream and an even bigger imagination.

---

## 🎮 HUD Concept

A visual concept of the in-game heads-up display is included in this repository as `hud-concept.html`. Open it in any browser to see an interactive mockup of the game's interface including the speedometer, minimap, NPC chat bubbles, pet companion panel, fuel gauge, drift score, lobby indicator, and real-time UK clock — all set against a neon-lit night street scene.

---

<p align="center">
  <strong>Designed with ❤️ by Albert, age 10, who dreams big.</strong><br>
  <em>Built with help from his mum.</em><br><br>
  <code>Now let's build it.</code>
</p>
