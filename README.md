##  Purpose and Scope

This repository contains an **interactive educational web application** that demonstrates **neural network backpropagation algorithms** through step-by-step visualization.

The application is designed as an **embedded demo** within the **Google for Developers platform**, providing an immersive learning experience for understanding:

-  Forward propagation  
-  Backpropagation  
-  Gradient descent

The codebase implements a **scroll-driven educational interface** where users progress through theoretical concepts while observing **real-time neural network computations and visualizations**.

>  For subsystem details, see:
> - **System Architecture**
> - **Core Systems**
> - **Platform Integration**

---

##  High-Level System Architecture

The application follows a **layered architecture** with clear separation between:

- **Platform Integration**  
  Embedding into external platforms like Google for Developers

- **Educational Content**  
  Narrative and instructional modules aligned with neural network concepts

- **Interactive Visualization Systems**  
  Real-time rendering of neural computations, weights, and gradients

---

###  Sources:

- `index.html`: lines 1–197

<img width="1371" height="811" alt="image" src="https://github.com/user-attachments/assets/5e4ff88f-244b-42f8-a68c-43e414d9ad83" />

##  Platform Integration Architecture

>  **Sources:**  
> - `index.html`: lines 10–26  
> - `index.html`: lines 37–47  
> - `index.html`: lines 192–193

The application integrates deeply with the **Google for Developers ecosystem** through several communication and rendering APIs.

###  Platform Integration Components

- **PostMessage API**  
  Used for bidirectional communication between the embedded iframe and the parent platform, enabling state sync, scroll control, and event handling.

- **Scroll-Driven Animation System**  
  Integrates with the parent page's scroll events to drive transitions in visualizations, enabling dynamic educational flow.

- **Responsive Canvas Rendering**  
  Leverages the platform's container dimensions to resize and scale the visualization canvas for consistent UX across devices.

- **Theme Synchronization**  
  Automatically applies light/dark modes based on the parent platform's current theme, ensuring visual consistency.

<img width="1395" height="807" alt="image" src="https://github.com/user-attachments/assets/1e8c110e-6789-4685-8c9a-2cafb0d06834" />

## Core Application Components

>  **Sources:**  
> - `index.html`: lines 10–19  
> - `index.html`: lines 21–24  
> - `index.html`: lines 41–47  
> - `index.html`: lines 53–59

The **framebox system** enables seamless communication between the **embedded demo** and the **parent devsite platform**, handling:

-  URL navigation  
-  Window sizing  
-  Event propagation

---

###  Core Module Dependencies

The demo application consists of several **interconnected JavaScript modules**, each responsible for a specific part of the educational experience:

| Module/File           | Role                                               |
|------------------------|----------------------------------------------------|
| `framebox.js`          | Handles messaging and sizing between iframe and devsite |
| `scroll-manager.js`    | Manages scroll-driven navigation and progress tracking |
| `nn-visualizer.js`     | Renders neural network states, activations, and weights |
| `gradient-engine.js`   | Performs gradient descent and backpropagation computations |
| `theme-sync.js`        | Synchronizes theme with Google devsite (light/dark) modes |

Each module contributes to a **unified educational flow**, enabling responsive, real-time updates and synchronized platform behavior.

<img width="1097" height="814" alt="image" src="https://github.com/user-attachments/assets/0b0a8aea-4b5f-483b-9aef-4b26388c9104" />

## 🧾 Educational Content Flow

>  **Sources:**  
> - `index.html`: lines 39–40  
> - `index.html`: lines 50–51  
> - `index.html`: lines 174–184  
> - `index.html`: lines 185–189  
> - `index.html`: lines 192–193

The `#container` `<div>` houses two main areas:

- `#sections` – Contains the **scroll-driven educational content**  
- `#vis` – Contains **interactive visualizations**

The `#mainsvg` element serves as the **primary drawing canvas**, rendering real-time neural network computations.

---

###  Educational Progression Structure

The application implements a **structured learning progression** through key mathematical and AI concepts:

1. **Forward Propagation**  
   Introduces activation flows and weighted sums

2. **Loss Calculation**  
   Demonstrates how errors are computed from predictions

3. **Backpropagation**  
   Breaks down the mathematical operations involved in weight updates

4. **Gradient Descent**  
   Shows step-wise updates to model parameters to minimize loss

Each section is visually and interactively tied to the previous, enabling learners to **see and feel** the impact of each computational step in context.


<img width="598" height="811" alt="image" src="https://github.com/user-attachments/assets/e518fc66-27e9-48a9-9e2c-243ac904051d" />

##  Section Structure and Rendering

>  **Sources:**  
> - `index.html`: lines 61–172  
> - `index.html`: lines 53–59  
> - `index.html`: lines 103, 109, 115  

Each educational unit is implemented as a `<section>` element that includes:

-  **Mathematical formulas rendered via MathJax**  
-  **Interactive visualizations triggered by scroll events**

The visualization system dynamically responds to scroll position, animating algorithms like **forward propagation**, **backpropagation**, and **gradient descent** in real time as the user moves through the content.

---

##  File Organization Structure

> **Sources:**  
> - `js/info.txt`: lines 1–2  
> - `css/info.txt`: lines 1–2  
> - `fonts/info.txt`: lines 1–2  

The codebase follows a **modular organization pattern** with clear separation by asset type:

| Directory | Purpose               | Key Files                                               |
|-----------|------------------------|----------------------------------------------------------|
| `/`       | Main entry point       | `index.html`                                             |
| `js/`     | JavaScript modules     | `X1ZpE2knmQQr.js`, `PTr3COWozeDa.js`, `adfGW7b8EEfI.js`, `ElIMwTHpiMyF.js` |
| `css/`    | Styling systems        | `lyFGJAff2iSE.css`, `7tPClckhfMqx.css`                   |
| `fonts/`  | Typography assets      | `.woff2` font files                                      |

>  **Note:**  
> JavaScript files use **obfuscated naming conventions**, likely for **optimization and caching** within the Google for Developers platform infrastructure.


