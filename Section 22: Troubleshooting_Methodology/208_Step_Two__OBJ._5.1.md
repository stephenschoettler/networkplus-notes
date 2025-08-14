## 💡 Step Two (OBJ. 5.1)
This section outlines the second step of the troubleshooting methodology: establishing a theory of probable cause, questioning the obvious, and utilizing various research and inspection techniques to narrow down the problem.

✅ **Step 2: Establish a theory of probable cause and question the obvious**
- Purpose: Formulate the most likely cause based on observed symptoms.

✅ **Probable Cause**
- Focus on the *most likely* explanation, not just any possibility.
- Start by questioning the obvious and simplest explanations.

✅ **Research & Inspection**
- **External Research:** Use search engines, vendor docs, outage trackers (e.g., Downdetector).
- **Internal Research:** Check system logs, diagnostic tools, system documentation.
- **Physical Inspection:** Look, listen, smell for clues (e.g., fan, hard drive sounds, burning smell).
- **Reproduce Problem:** Attempt to recreate intermittent issues to gather more data.

✅ **Troubleshooting Approaches (using OSI Model)**
- **Top-to-Bottom:** Start at Layer 7 (Application) and work down to Layer 1 (Physical).
- **Bottom-Up:** Start at Layer 1 (Physical) and work up to Layer 7 (Application).
- **Divide and Conquer:** Start in the middle (e.g., ping `8.8.8.8` to test Layer 1-4).
  - Success: Problem is above (L5-7).
  - Failure: Problem is below (L1-4).

✅ **Consult Others**
- If others worked on the system, understand their actions to avoid repeating failed steps.