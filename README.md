💧 DewDoll
Sip & Glow
DewDoll is a pocket-sized, Tamagotchi-inspired hydration companion designed to look like a vintage makeup compact.
The device combines fashion, nostalgia, physical computing, and interactive design into a small personal object. A round touchscreen replaces the traditional mirror inside the compact, displaying a custom digital fashion avatar that reacts to the user's hydration throughout the day.

Every time the user finishes a glass or bottle of water, they can tap the touchscreen to log their intake. As hydration increases, the avatar becomes happier, healthier, and more glamorous.

The goal is to turn something as ordinary as drinking water into a playful and visually rewarding experience.

🎀 Why I Made DewDoll
DewDoll is a project that combines two sides of my interests that don't always feel like they belong together.
I'm a micro-influencer who loves girly things, fashion, beauty, and cute technology, while also studying in a male-dominated field where I don't always see projects that reflect those interests.

I wanted to create something that felt like me.

Instead of hiding the feminine and playful aspects of my interests, I wanted to use them as part of the design language of a technical project.

The hydration aspect of DewDoll is also personal. I tend to get dehydrated easily and have often struggled with remembering to drink enough water. I wanted to explore whether a small, cute, interactive object could make hydration feel less like a chore and more like taking care of a little digital companion.

DewDoll is ultimately designed for people who might relate to that experience — people who love cute, feminine, nostalgic, and personalized technology, but may not always see themselves represented in traditional hardware projects.

Rather than creating another generic health tracker, I wanted to create something that feels like a beauty accessory, a virtual pet, and a piece of technology all at once.

Concept
The core interaction is simple:
        Drink water
             ↓
        Tap DewDoll
             ↓
       Water is logged
             ↓
       Avatar responds
             ↓
      DewDoll gets happier

The avatar acts as a visual representation of the user's hydration.
Instead of only showing a number such as 32 oz, DewDoll gives that number personality.

Avatar progression
Hydration	DewDoll's state
💧 0–15 oz	😴 Tired
💧 16–31 oz	💦 Thirsty
💧 32–47 oz	🙂 Feeling Better
💧 48–63 oz	✨ Glowing
💧 64+ oz	💕 Fabulous

These values are part of the current prototype and may change during development.
Physical Design
DewDoll is designed to fit inside a vintage makeup compact or a 3D-printed replica.
The traditional mirror area becomes the digital display.

The goal is for the electronics to be hidden so that, when closed, the object looks like an ordinary vintage beauty compact.

When opened, the user discovers a tiny digital world inside.

Design direction
Vintage makeup compact
Feminine beauty aesthetic
Pink and pastel color palette
Fashion-doll inspired avatar
Rounded interface
Pixel-art / retro digital graphics
Sparkles, hearts, and beauty-inspired UI elements
Small enough to carry in a bag or keep on a desk
Hardware
Microcontroller
Adafruit QT Py RP2040
The QT Py acts as the brain of DewDoll.

It will handle:

Water intake data
Touchscreen input
Display graphics
Avatar states
Animations
User interaction
Display
Planned display:
1.28-inch round 240 × 240 capacitive touchscreen

The display is intended to replace the mirror inside the compact.

Current target specifications:

1.28-inch round display
240 × 240 resolution
Full color
Capacitive touch
GC9A01 display controller
CST816S/CST816T touch controller
SPI display communication
I²C touch communication
The exact display model and library will be documented once the final hardware is confirmed.
Battery
Planned battery:
Adafruit 3.7V 500mAh Lithium Polymer Battery

Product ID: 1578

The battery will eventually allow DewDoll to operate as a portable device.

The initial prototype will be powered through USB while the electronics and software are being developed.

Software
DewDoll is being developed using:
Arduino IDE
C++ / Arduino
RP2040 board support
Display and touchscreen libraries appropriate for the final display
The software will be developed incrementally rather than building the entire application at once.
Current Software Architecture
The first version of DewDoll tracks a few core pieces of information:
int waterOz = 0;
const int waterGoal = 64;
String avatarMood;

The amount of water determines the avatar's current state.
For example:

waterOz < 16
      ↓
   TIRED

waterOz < 32
      ↓
   THIRSTY

waterOz < 48
      ↓
FEELING BETTER

waterOz < 64
      ↓
   GLOWING

waterOz >= 64
      ↓
  FABULOUS

The first prototype uses the Arduino Serial Monitor to test this logic before connecting the touchscreen.
Planned Features
Hydration Tracking
Users can log water intake directly through the touchscreen.
The initial interaction will be:

💧 +8 OZ

Each tap increases the daily water total.
👱‍♀️ Dynamic Avatar
DewDoll's appearance changes according to hydration.
Possible visual changes include:

Facial expressions
Hair styles
Outfits
Accessories
Blush
Sparkles
Energy level
Animations
✨ Animations
Future versions may include:
Blinking
Idle animations
Dancing
Sparkle effects
Water-drop animations
Outfit changes
Celebration animations
Sleeping/tired animations
💕 Daily Goal
The initial prototype uses a 64 oz daily goal.
When the goal is reached, DewDoll can enter a special celebration state.

Example:

✨ ✨ ✨ ✨ ✨

       👱‍♀️
    💕 FABULOUS 💕

      64 / 64 OZ

   !!

✨ ✨ ✨ ✨ ✨

The hydration goal is customizable and is intended as a playful project mechanic rather than medical guidance.
Development Roadmap
Phase 1 — Software Logic
 Define project concept
 Define hydration states
 Create basic water-tracking variables
 Create avatar mood logic
 Test water tracking on QT Py
Phase 2 — Electronics
 Set up QT Py RP2040
 Upload first Arduino program
 Connect touchscreen
 Test display
 Test touch input
Phase 3 — Interface
 Create DewDoll home screen
 Create water counter
 Create avatar graphics
 Connect avatar states to hydration
 Create touchscreen controls
Phase 4 — Animation
 Add idle animation
 Add facial expressions
 Add sparkle effects
 Add hydration animations
 Add goal celebration
Phase 5 — Portable Device
 Add LiPo battery
 Add charging/power management
 Test battery operation
 Optimize wiring
Phase 6 — Compact
 Find suitable vintage compact
 Measure internal dimensions
 Design screen mounting
 Design electronics placement
 Assemble prototype
 Create final enclosure
Phase 7 — Final Prototype
 Test complete device
 Document final design
 Photograph finished prototype
 Create project video
 Document lessons learned
 Repository Structure
dewdoll/
│
├── README.md
│
├── src/
│   ├── dewdoll.ino
│   ├── water_tracker.cpp
│   ├── avatar.cpp
│   └── avatar.h
│
├── assets/
│   ├── concept-sketches/
│   ├── avatar-designs/
│   ├── screen-designs/
│   └── prototype-photos/
│
├── hardware/
│   ├── parts-list.md
│   ├── wiring-diagram.png
│   └── pinout.md
│
├── design/
│   ├── concept.md
│   ├── visual-identity.md
│   └── enclosure.md
│
└── docs/
    ├── development-log.md
    └── troubleshooting.md

The repository will grow as the project develops.
Design Goals
DewDoll is designed around several ideas:
Technology can be feminine.

Hardware projects don't have to look industrial or masculine to be technically interesting.

Personal interests can influence technical design.

Fashion, beauty, nostalgia, and cute aesthetics can all become meaningful parts of an interactive technology project.

Health tracking doesn't have to feel clinical.

DewDoll explores whether playful interaction and emotional attachment to a digital character can make a routine habit feel more enjoyable.

Small objects can create meaningful experiences.

The goal isn't to build the most technologically complicated device. It's to create a small object that feels personal and delightful to use.

Development Log
This repository will document the project as it develops.
Rather than only showing the finished product, I want to document:

Design decisions
Hardware experiments
Coding experiments
Failed attempts
Debugging
Prototypes
Avatar development
Circuit diagrams
Enclosure development
Lessons learned
This is my first hardware project, so part of the purpose of DewDoll is learning how to turn an idea into a working physical object.
What I'm Learning
Through DewDoll, I'm learning:
Arduino programming
C++
Microcontrollers
RP2040 development
Electronics
Breadboarding
Touchscreen interfaces
SPI and I²C communication
Battery-powered electronics
Physical computing
Interactive design
Pixel art
Product prototyping
Enclosure design
Project Philosophy
DewDoll is intentionally a little unusual.
It's not meant to look like a traditional electronics project.

It's meant to feel like something you might find inside a makeup bag — until you open it and discover a tiny digital companion.

Beauty object on the outside.
Technology on the inside.
Digital companion at the center.

Project Documentation
Photos, sketches, prototypes, screen designs, and development updates will be added to this repository as the project progresses.
Concept → Prototype → Final Object
 IDEA
   ↓
 CONCEPT
   ↓
 CODE
   ↓
 ELECTRONICS
   ↓
 TOUCHSCREEN
   ↓
 DEWDOLL
   ↓
 COMPACT
   ↓
 FINAL PROTOTYPE

⚠️ Project Status
🚧 In Development
DewDoll is currently in the early prototyping stage.

The first milestone is getting the water-tracking and avatar mood system working on the Adafruit QT Py RP2040 before integrating the touchscreen and physical enclosure.

💧 DewDoll
A little hydration. A little glamour. A tiny digital bestie.
Sip & Glow💕
