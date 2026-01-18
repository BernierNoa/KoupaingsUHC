# ⚔️ KoupaingsUHC - Custom Humoristic Minecraft Game Mode

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spigot](https://img.shields.io/badge/API-Spigot_1.8-FFCA28?style=for-the-badge&logo=minecraft&logoColor=black)
![License](https://img.shields.io/badge/License-Private-red?style=for-the-badge)

## 🎮 Overview

**KoupaingsUHC** is a fully custom Minecraft plugin designed to run automated **Ultra Hardcore (UHC)** matches. It features a complex role-playing mechanic inspired by my friend references, specifically tailored for a private gaming event.

This project demonstrates advanced usage of **Object-Oriented Programming (OOP)** to manage game states, player interactions, and ability polymorphism.

## ✨ Key Features

* **Complex Role System:** Over 15 unique roles distributed across 3 factions (Gentils, Méchants, Solos).
* **Custom Abilities:** Each role has programmed active and passive abilities (cooldowns, effects, damage modifiers).
* **GUI Management:** Interactive inventory menus (`CompoMenu`) for game configuration and team selection.
* **Game Loop Automation:** Automated timer handling, border shrinking, and win condition checking.
* **Command System:** Custom administrative commands (`/kp`) to manage the game flow.

## ⚙️ Software Architecture

The project is built on a robust Java structure focusing on scalability and maintainability:

### 1. Polymorphism & Inheritance
To manage the diversity of roles without code duplication, the project uses a strong inheritance model:
* **Interface/Abstract:** A base `Roles` definition handles common attributes (HP, name, description).
* **Implementation:** `RolesImpl` contains the core logic shared by most roles.
* **Specialization:** Specific classes (e.g., `Alecsix.java`, `Skyrouf.java`, `Black_Star.java`) override methods to implement unique gameplay mechanics.

```java
// Example of the structure logic
public class Alecsix extends RolesImpl {
    @Override
    public void onDayStart() {
        // Specific logic for this character
    }
}
