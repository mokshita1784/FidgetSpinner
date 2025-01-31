
## **1. Introduction**

### **1.1 Purpose**
This document provides the Software Requirements Specification (SRS) for the **Fidget Spinner Game**. The game allows users to control a spinning object (fidget spinner) on the screen, enhancing user engagement with soothing effects. It includes features like spin speed control, collision detection, and scoring mechanisms to enhance the gaming experience.

### **1.2 Scope**
The game will be developed using Python and the **pygame** library. The project will allow users to interact with a virtual fidget spinner, simulate real-life physics, and use keyboard inputs for controlling the spinner’s speed.

### **1.3 Definitions, Acronyms, and Abbreviations**
- **Fidget Spinner**: A toy consisting of a central bearing and multiple arms that spin around the center.
- **pygame**: A Python library used to create video games.
- **FPS (Frames Per Second)**: A measure of how many frames the game renders per second, affecting smoothness.

---

## **2. Overall Description**

### **2.1 Product Perspective**
The **Fidget Spinner Game** will be a standalone desktop application that users can run on their personal computers. It will require Python and pygame for execution. The game will feature a simple user interface (UI), smooth animations, and controls to interact with the spinner.

### **2.2 Product Features**
- **Spinner Animation**: A central spinner with rotating arms in different colors.
- **Speed Control**: The ability to increase or decrease the spinner’s speed using keyboard inputs.
- **Score Tracking**: Display of the score that increases over time.
- **Collision Detection**: Handling of spinner interactions with boundaries or other objects (if applicable).

### **2.3 User Classes and Characteristics**
- **Casual Users**: Individuals who want a fun and relaxing experience playing the game.
- **Users with ADHD/Autism**: People who might benefit from the soothing nature of the game and use it for stress relief.

### **2.4 Operating Environment**
- The game will be developed for **Windows**, **Mac OS**, and **Linux** operating systems. It will require Python 3.x and pygame to be installed.

---

## **3. System Features**

### **3.1 Game Mechanics**
#### **3.1.1 Spinner Movement**
- The spinner consists of three arms, each with a dot.
- The spinner rotates around the center, with each arm turning 120 degrees after drawing.
- The spinner's rotation angle is based on the `state['turn']` variable.

#### **3.1.2 Speed Control**
- The user can increase the spinner’s speed by pressing the **spacebar** key.
- The spinner will gradually slow down over time.

#### **3.1.3 Score and Lives System**
- The user earns a point for each frame where the spinner continues spinning.
- The user loses a life if the spinner collides with an obstacle or the boundaries of the screen.
- The game ends when the player has no lives left.

### **3.2 Collision Detection**
- If the spinner collides with predefined screen boundaries (left, right, top, or bottom), the game checks if it should reset or decrease lives.
- A method `is_collision()` is used to check if the spinner hits any obstacles.

---

## **4. External Interface Requirements**

### **4.1 User Interfaces**
- **Main Game Window**: A window that will contain the spinner and the background. The spinner will have arms and dots in red, green, and blue colors.
- **Controls**: The user can press the **spacebar** to change the speed of the spinner.

### **4.2 Hardware Interfaces**
- The game does not require specific hardware other than a computer with a keyboard and display.

### **4.3 Software Interfaces**
- The game will use **Python 3.x** for implementation.
- The **pygame** library will be used to render graphics, handle events, and control animation.

---

## **5. System Features**

### **5.1 Game Setup**
- The game will initialize a window of size **420x420** pixels.
- The spinner will be drawn with **width 20** for the arms.
- The game will begin with the spinner stationary and will gradually begin spinning.

### **5.2 Animation**
- The spinner will rotate continuously until the player presses the **spacebar**.
- The game will update every **20 milliseconds** to show smooth animation.

---

## **6. Non-Functional Requirements**

### **6.1 Performance Requirements**
- The game should maintain a smooth animation at **30 frames per second (FPS)**.

### **6.2 Reliability**
- The game must run reliably without crashes or memory leaks.
- User input, such as pressing the **spacebar**, should be responded to within **500ms**.

### **6.3 Usability**
- The game should be easy to play with simple keyboard controls.
- The user should be able to play without needing instructions.

---

## **7. Design Constraints**
- The game will be developed using **pygame** and **Python 3.x**.
- The game should work across multiple platforms (Windows, Mac, Linux) as long as Python and pygame are installed.
- The spinner’s speed control should be manageable and responsive.

---

## **8. Other Requirements**

### **8.1 Installation Requirements**
- Users need to have **Python 3.x** and **pygame** installed.
- The game can be run from a terminal or an IDE like **VS Code** or **PyCharm**.
