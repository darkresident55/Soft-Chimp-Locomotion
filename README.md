# Soft Chimp Locomotion (SCL)

This project is a part of many movement systems I use in my main games. If you'd like to support me, feel free to do so here: [https://bmc.link/anemunt](https://bmc.link/anemunt)

## -- About --
Soft Chimp Locomotion (SCL) is a customizable locomotion system used in games like *Chimps Life*, *Recharge*, and more.
It was created by **Anemunt** and **Terminal**, with rights belonging to both.

## -- Movement Properties --
*SCL includes a flexible movement system that can be tuned through the **Motion Settings** script, located under the **Chimp** object inside the prefab.*
* **Motion Settings** now includes a **Movement Settings Profile system**,
  this lets you create and swap between different physics settings, for example: realistic, arcade-style, or experimental.
* All core locomotion values are controlled here, no need to directly edit the hand objects anymore.

## -- Setup --
### Getting started with SCL is simple:

1. Go to the **Soft Chimp Locomotion** folder.
2. Drag the **SCL V10** (or newer) prefab into your Unity scene.
3. By default, it will load with 3 different **Movement Settings Profiles**, so your player can move right away
   *(default set to In-Between).*
4. To customize, open the **Motion Settings** script under **Chimp** and either adjust the current profile or create a new one.

## -- Usage Example --
Here’s a quick example showing how to access the **Chimp** object and tweak gravity for the active profile:

```csharp
using SoftChimpLocomotion;
using UnityEngine;

public class ChimpGravityExample : MonoBehaviour
{
    public Chimp chimp;

    void Start()
    {
        // Grab the motion system from the Chimp object
        MotionSettings motionSettings = chimp.MotionSettings;

        // Get the active Movement Settings Profile
        MovementSettingsProfile currentProfile = motionSettings.ActiveProfile;

        // Just for fun: tweak gravity for this profile
        currentProfile.gravity = 9.8f;
    }
}
```

*Notes:*
* `chimp.MotionSettings` gives you access to the motion system.
* `currentProfile.gravity` can be changed in code or via the inspector.
* Other values like speed, jump height, or friction work the same way if you want to play around with them.

Thank you for considering Soft Chimp Locomotion, enjoy building, tweaking, and experimenting with it!
