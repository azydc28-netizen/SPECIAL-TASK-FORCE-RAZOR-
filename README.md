# 📡 LIVE RADIO TRANSMISSION  
## SPECIAL TASK FORCE 457 "RAZOR"

**Signal:** Stable  
**Channel:** Secure  
**Audience:** Operator / Programmer  

---

### COMMAND, THIS IS RAZOR

What you are running is a **text-based Python tactical simulator**.  
No graphics. No mouse. Only commands, choices, and consequences.

This transmission explains **exactly how the program operates**, from launch to shutdown.

---

## 🔧 PROGRAM BOOT SEQUENCE

1. The program starts by loading:
   - Operator data (name, rank, XP, HP, team, weapon)
   - Weapon database
   - Mission list
   - Difficulty settings
   - Rank progression table

2. You are prompted to enter a **callsign**.
3. You are automatically issued a **standard M4A1**.
4. You must immediately **select a team**.

Once this is done, the program enters a **continuous command loop**.

---

## 🧭 MAIN COMMAND LOOP (CORE OF THE PROGRAM)

The program now repeats the following steps until you exit:

1. **Update Rank**
   - Rank is recalculated every loop using:
     ```
     XP // 150
     ```
   - Rank changes automatically. No manual promotion.

2. **Display Command Menu**

Check Profile

Change Team

Visit Armory

Start Mission

Exit Operation

3. **Wait for User Input**
- Your choice determines which block of code runs next.
- Invalid input returns you to the menu.

---

## 📄 OPTION 1: CHECK PROFILE

Displays current operator data:
- Callsign
- Rank
- XP
- Team
- Equipped weapon
- Current HP

No data is modified here.  
This option is **read-only**.

---

## 🔁 OPTION 2: CHANGE TEAM

- Re-displays the team list.
- Updates `operator["team"]` based on input.
- Team change does not affect stats directly.
- Used mainly for role-play and immersion.

---

## 🔫 OPTION 3: VISIT ARMORY

1. The program lists **all weapons** with:
- Code
- Name
- Type
- Damage
- XP cost

2. You enter a weapon code.
3. The program checks:
- Does the weapon exist?
- Do you have enough XP?

4. If both checks pass:
- XP is reduced
- Weapon is equipped immediately

No refunds. XP spent is permanent.

---

## 🚁 OPTION 4: START MISSION

This option triggers the **combat system**.

### STEP 1: Mission Selection
You choose one mission from a predefined list.

### STEP 2: Difficulty Selection
Difficulty affects:
- Enemy HP
- Enemy damage
- XP reward

### STEP 3: Combat Initialization
- Enemy HP = `150 × difficulty multiplier`
- Player HP = current operator HP

---

## ⚔️ COMBAT LOOP (MISSION CORE)

The program now enters a second loop that runs **until someone drops or you retreat**.

Each round follows this exact order:

1. Display:
- Player HP
- Enemy HP

2. Prompt action:


Fire Weapon

Tactical Maneuver

Retreat


3. Resolve player action:
- **Fire Weapon**
  - Damage is randomized based on weapon stats.
  - Enemy HP decreases.
- **Tactical Maneuver**
  - Player regains random HP.
- **Retreat**
  - Mission ends immediately with HP penalty.

4. Enemy attacks (unless you retreated):
- Damage is randomized.
- Scaled by difficulty.
- Player HP decreases.

5. Loop repeats.

---

## 🏁 MISSION END CONDITIONS

### SUCCESS
- Enemy HP reaches zero first.
- XP is awarded:


70 × difficulty multiplier

- Player returns to command menu.

### FAILURE
- Player HP reaches zero.
- HP penalty applied.
- No XP gained.

### RETREAT
- Mission aborted manually.
- Reduced HP.
- No XP gained.

After any outcome:
- HP is clamped to a minimum of 50.
- Rank is recalculated.
- Control returns to main menu.

---

## 🎖️ RANK SYSTEM LOGIC

Rank is purely XP-based:

| XP | Rank |
|----|------|
| 0–149 | Recruit |
| 150–299 | Private |
| 300–449 | Corporal |
| 450–599 | Sergeant |
| 600–749 | Lieutenant |
| 750–899 | Captain |
| 900+ | Major |

No rank affects combat yet.  
Rank is **progress tracking and immersion**.

---

## 🧠 IMPORTANT PROGRAM NOTES

- There are **no functions**; code runs sequentially.
- No save system. Progress resets on restart.
- All randomness comes from Python’s `random` module.
- Every menu is input-driven and blocking.
- Invalid input never crashes the program; it redirects.

---

## 📴 PROGRAM SHUTDOWN

Selecting **Exit Operation**:
- Calls `sys.exit()`
- Terminates the program cleanly.

---

### FINAL TRANSMISSION

This program is a **command-line simulation**, not a full game engine.  
Its strength is clarity, structure, and logic flow.

Ideal for:
- Beginners learning control flow
- Menu-driven programs
- Loops and state management
- Text-based game logic

**RAZOR OUT. SIGNAL TERMINATED.**
