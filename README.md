# 📡 RADIO TRANSMISSION: SPECIAL TASK FORCE 457 "RAZOR"

**Transmission Code:** RAZOR-OPERATOR-BRIEF  
**Date:** Classified  
**Origin:** Special Task Force 457 Command  

---

### **COMMANDER, LISTEN UP**

You are now **active duty** in **Special Task Force 457 "RAZOR"**. All communications are operational. Your callsign will define your mission. Follow orders, choose your team, and complete objectives. Lives depend on your decisions.

**SPECIAL TASK FORCE 457 "RAZOR"** is a text-based tactical combat simulation written in Python.  
The program places the player in command of a special forces operator, allowing them to manage equipment, choose teams, and complete combat missions through a command-line interface.

This project is designed as a **menu-driven simulation** and is ideal for learning basic Python concepts such as loops, dictionaries, conditionals, and state management.

---

## 📌 Program Description

The program simulates a special forces command environment where the player:

- Creates an operator using a callsign
- Selects a combat team
- Purchases and equips weapons using experience points (XP)
- Deploys on missions with different difficulty levels
- Engages in turn-based combat
- Earns XP and ranks up based on mission performance

All gameplay is text-based and controlled through keyboard input.

---

## ⚙️ How the Program Works

### 1. Operator Initialization
When the program starts:
- The player enters a **callsign**
- The operator is assigned:
  - Rank: Recruit
  - Health (HP): 100
  - XP: 0
  - Default weapon: M4A1
- The player selects one of three teams:
  - Alpha Team – Direct Assault
  - Bravo Team – Recon & Stealth
  - Charlie Team – Heavy Support

---

### 2. Main Command Loop
After setup, the program enters a continuous loop that displays the **Command Menu**:

- Check Profile
- Change Team
- Visit Armory
- Start Mission
- Exit Operation

The program keeps running until the user chooses to exit.

---

### 3. Operator Profile
This option displays the operator’s current status:
- Callsign
- Rank
- XP
- Team
- Equipped weapon
- Current HP

No values are modified in this section.

---

### 4. Team Selection
The player may switch teams at any time.  
This updates the operator’s assigned team but does not directly affect combat statistics.

---

### 5. Armory System
The armory allows the player to:
- View all available weapons
- See weapon damage and XP cost
- Purchase and equip weapons if sufficient XP is available

XP is permanently deducted when a weapon is purchased.

---

### 6. Mission System
When starting a mission, the player:
1. Selects a mission type
2. Selects a difficulty level:
   - Easy
   - Normal
   - Hard
   - Extreme

Difficulty affects:
- Enemy health
- Enemy damage
- XP rewards

Enemy health is calculated based on the selected difficulty.

---

### 7. Combat Mechanics
Combat is turn-based and continues until:
- The enemy is defeated
- The player’s HP reaches zero
- The player retreats

Each combat round allows the player to:
- Fire their weapon (deal randomized damage)
- Perform a tactical maneuver (restore HP)
- Retreat from the mission

After the player’s action, the enemy counterattacks.

---

### 8. Mission Outcomes
- **Mission Success**
  - Enemy HP reaches zero
  - Player gains XP
- **Mission Failure**
  - Player HP reaches zero
  - HP penalty applied
- **Retreat**
  - Mission ends early
  - Reduced HP, no XP gain

The player’s HP is never allowed to drop below a minimum threshold after missions.

---

### 9. Rank Progression
Ranks are automatically updated based on XP:

| XP Range | Rank |
|--------|------|
| 0–149 | Recruit |
| 150–299 | Private |
| 300–449 | Corporal |
| 450–599 | Sergeant |
| 600–749 | Lieutenant |
| 750–899 | Captain |
| 900+ | Major |

Rank updates occur inside the main loop and require no manual input.

---

## 🛠️ Technical Notes

- Written in **basic Python**
- Uses only standard libraries:
  - `random`
  - `sys`
- No functions (`def`) are used
- All logic runs sequentially
- No save system (progress resets on restart)
- Designed for clarity and learning, not optimization

---

## 🚪 Exiting the Program

Selecting **Exit Operation** cleanly terminates the program using `sys.exit()`.

## **ABOUT SPECIAL TASK FORCE 457 "RAZOR"**

**RAZOR** is a fictional elite counter-terrorism unit. Operators execute high-risk, precision missions globally. You are trained to adapt, strategize, and survive.  

- Decisions matter.  
- Lives depend on your choices.  
- Operate with precision.

> **End Transmission**

---
