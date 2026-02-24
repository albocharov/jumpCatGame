# Jump Cat Game

A 2D platformer mini-game built with Unity where you guide a cat jumping upward through procedurally generated platforms — inspired by the classic Doodle Jump style.

## Gameplay

The cat automatically bounces off platforms. Your goal is to guide it left and right to keep landing on platforms and climb as high as possible. Reach a score of **25,000** to trigger the win condition and land on the final top platform.

If the cat falls below the bottom of the screen, the game is over.

## Controls

| Input | Action |
|---|---|
| **Mouse click / hold** | Move the cat toward the cursor |
| **Touch / tap** | Move the cat toward the touch position |
| **Any key** | Start the game (dismiss the intro panel) |

## Platform Types

| Platform | Behaviour |
|---|---|
| **Green** | Standard platform — bounces the cat upward |
| **Blue** | Moving platform — slides left and right across the screen |
| **White** | One-time platform — disappears after the cat lands on it |
| **Brown** | Fake platform — does not support the cat |

## Power-ups

| Power-up | Effect |
|---|---|
| **Spring** | Gives a boosted bounce when landed on |
| **Trampoline** | Gives a strong bounce when landed on |
| **Propeller** | Attaches to the cat and launches it very high into the air |

## Scoring

- Score increases as the cat climbs higher.
- The maximum score is **25,000**.
- Reaching the maximum score stops platform generation and spawns the final **Top Platform**.
- Landing on the Top Platform twice ends the game with a victory.
- Scoring below 30% of the maximum triggers the lose sound effect.

## Project Structure

```
Assets/
└── Scripts/
    └── MiniGame/
        └── JumpCat/
            ├── Player_Controller.cs   # Input handling and cat movement
            ├── Game_Controller.cs     # Score tracking, win/lose logic
            ├── Platform_Generator.cs  # Procedural platform spawning
            ├── Platform.cs            # Base platform bounce & destroy logic
            ├── Platform_Blue.cs       # Moving platform behaviour
            ├── Platform_White.cs      # One-time platform behaviour
            ├── Platform_Brown.cs      # Fake platform behaviour
            ├── TopPlatform.cs         # Final win platform logic
            ├── Propeller.cs           # Propeller power-up logic
            └── Camera_Follow.cs       # Camera tracking
```

## Requirements

- **Unity** 2021 or later (2D module required)
- **TextMesh Pro** package (included via Unity Package Manager)

## Getting Started

1. Clone or download this repository.
2. Open the project in **Unity Hub** by selecting the root folder.
3. Allow Unity to import all assets and resolve packages automatically.
4. Open the main game scene located in `Assets/`.
5. Press **Play** in the Unity Editor to run the game.

## Dependencies

All dependencies are managed via the Unity Package Manager (`Packages/manifest.json`):

- `com.unity.feature.2d` — 2D toolset
- `com.unity.textmeshpro` — UI text rendering
- `com.unity.ugui` — Unity UI system
- `com.unity.timeline` — timeline support
- `com.unity.visualscripting` — visual scripting
- `com.unity.uiextensions` — additional UI components
- `dev.thedesign.controllervibrationpackage` — controller vibration support
