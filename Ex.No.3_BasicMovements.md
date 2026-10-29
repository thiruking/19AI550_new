# Ex.No: 3 Basic movements in Unity
**DATE: 26/10/26**  
**REGISTER NUMBER: 212224240176**  

## AIM:
To learn the basic movements translation, scaling and rotation of game objects through code.

## Procedure:
1. Setup the Scene.
2. Open Unity and create a 3D Scene.
3. Add three objects:
   * Cube → Rename to `Object1` (for movement)
   * Sphere → Rename to `Object2` (for rotation)
   * Capsule → Rename to `Object3` (for scaling)
4. Add the Script: Create a C# Script → Name it `TransformOperations.cs`.
5. Write the code for translation, scaling and rotation, save and close the script.
6. Save the script.
7. Select any empty GameObject (or create one: GameObject → Create Empty).
8. Attach the `TransformOperations` script to it.
9. In the Inspector, assign:
   * `Object1` → Drag the Cube
   * `Object2` → Drag the Sphere
   * `Object3` → Drag the Capsule
10. Run the Scene: Press Play ▶️ in Unity.
11. Stop the program.

## Program:
```csharp
using UnityEngine;

public class TransformOperations : MonoBehaviour
{
    public Transform object1; // Object for translation
    public Transform object2; // Object for rotation
    public Transform object3; // Object for scaling

    public float moveSpeed = 2f;   // Speed of translation
    public float rotateSpeed = 50f; // Speed of rotation
    public float scaleSpeed = 0.5f; // Speed of scaling

    void Update()
    {
        // Translate (Move) object1 along the X-axis
        if (object1 != null)
        {
            object1.Translate(0.02f, 0, 0);
        }

        // Rotate object2 around the Y-axis
        if (object2 != null)
        {
            object2.Rotate(0, 0.02f, 0);
        }

        // Scale object3 up and down
        if (object3 != null)
        {
            object3.localScale += new Vector3(0.02f, 0.02f, 0);
        }
    }
}
```

## OUTPUT :
<img width="1920" height="1080" alt="Screenshot 2026-10-29 183222" src="https://github.com/user-attachments/assets/5e14f20f-c26f-4bbb-bacd-305a23f81db7" />
<img width="788" height="611" alt="Screenshot 2026-10-29 185057" src="https://github.com/user-attachments/assets/d9b8cff7-8fbb-4820-8e98-cd2a984db5ae" />

## RESULT :
Thus the basic movement is learned through scripting.
