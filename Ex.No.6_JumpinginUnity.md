# Ex.No: 6  Implementation of Jumping  behaviour- Unity
### DATE: 30/10/26                                                                      
### REGISTER NUMBER : 212224240176
### AIM: 
To write a program to simulate the process of jumping in Unity.
### Algorithm:
```
1. Create a new 3D Unity project
2. Add a Plane
3. Right-click Hierarchy → 3D Object → Plane → Rename to Ground
4. Add a Cube (Player)
5. Right-click Hierarchy → 3D Object → Cube → Rename to Player
6. Set Position: (0, 0.5, 0)
7. Add a Rigidbody to the Player
8. With the Player selected: Inspector → Add Component → Rigidbody
9. Set Constraints > Freeze Rotation X, Z (optional for stability)
10.Create the Jump Script and Apply the Script Player
11.Run the game
Press Play
Press Spacebar to jump
Your cube should only jump when touching the ground
```
###
**Program **
```c
using UnityEngine;

public class PlayerJump : MonoBehaviour
{
    private Rigidbody rb;
    public float jumpForce = 5f;
    
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space) )
        {
            rb.AddForce(Vector3.up * jumpForce, ForceMode.Impulse);
            
        }
    }

   
}
```
### Output:


<img width="1915" height="1078" alt="Screenshot 2026-10-30 180629" src="https://github.com/user-attachments/assets/507908fd-746b-4806-8a4a-57ad8d81277d" />

<img width="1076" height="677" alt="Screenshot 2026-10-30 180656" src="https://github.com/user-attachments/assets/05c289ae-b287-42f4-a1b4-b82548ca6dbd" />



### Result:
Thus the simple jumping behavior was implemented successfully.
