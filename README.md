<h1 align="center">Pac-Man in C</h1>

<p align="center">
A classic arcade game recreated from scratch in C using Raylib and compiled to WebAssembly to run directly in the browser.
</p>

<p align="center">
This project began as my first major university programming assignment and evolved into a complete learning experience in low-level programming, software design, and clean code practices.
</p>

---

<h2>Play in the Browser</h2>

<p>
The game runs entirely in the browser through WebAssembly.
</p>

<p>
<strong>Play here:</strong><br>
https://nako1991.github.io/Pacman/
</p>

<p>
<strong>Controls</strong><br>
Arrow Keys / WASD → Move Pac-Man
</p>

---

<h2>Project Motivation</h2>

<p>
This project started from a personal motivation: a lifelong love for videogames.
</p>

<p>
Growing up during the golden age of arcade games, Pac-Man became one of the most iconic and influential titles of my generation. Recreating it from scratch was both a tribute to that era and a way to deeply understand how games actually work internally.
</p>

<p>
Instead of relying on a high-level engine, the entire project was implemented in the C programming language. This decision forced me to confront low-level programming challenges and understand fundamental concepts such as memory management, program structure, and system design.
</p>

---

<h2>What I Learned</h2>

<h3>Low-Level Programming</h3>

<p>
Because the game is written entirely in C, many systems had to be handled manually. During development I worked extensively with:
</p>

<ul>
<li>Memory management</li>
<li>Pointers</li>
<li>Struct design and data ownership</li>
<li>Passing references between functions</li>
<li>Manual matrix management and row/column traversal</li>
<li>Understanding scopes and environments (global variables, local variables, and loop scopes)</li>
<li>Avoiding undefined behavior</li>
<li>Manual array and memory control</li>
</ul>

<p>
Working at this level provided a deep understanding of how programs actually behave in memory and how systems are structured internally.
</p>

---

<h3>Clean Code Principles</h3>

<p>
During the development of this project I also studied several software design principles inspired by the work of Robert C. Martin (Uncle Bob) and the classic book <i>Design Patterns: Elements of Reusable Object-Oriented Software</i>.
</p>

<p>
Although the project is written in C and not in an object-oriented language, many of the architectural ideas from these sources influenced how the systems were structured.
</p>

<p>
Many of those ideas influenced how the project was written. Instead of focusing only on making the game work, I tried to make the code understandable and maintainable.
</p>

<p>
Concepts applied throughout the project include:
</p>

<ul>
<li>Clear and descriptive naming conventions</li>
<li>Separation of responsibilities</li>
<li>Small and modular functions</li>
<li>Readable control flow</li>
<li>Explicit state handling</li>
<li>Code organized from general to specific behavior</li>
</ul>

<p>
Special attention was given to variable and function names. Rather than using short or abstract identifiers, the goal was to make the purpose of each part of the code immediately understandable.
</p>

---

<h2>Game Architecture</h2>

<p>
The project follows a classic game loop architecture separating input, logic, and rendering.
</p>

<pre>
while (gameRunning)
{
    readInput();
    updateGameState();
    renderFrame();
}
</pre>

<p>
The codebase is intentionally structured for readability:
</p>

<ul>
<li>Initialization systems</li>
<li>Main game loop</li>
<li>Input handling</li>
<li>Game state updates</li>
<li>Rendering logic</li>
<li>Game subsystems</li>
</ul>

<p>
This structure makes the project easier to understand and maintain as the codebase grows.
</p>

---

<h2>Gameplay Systems Implemented</h2>

<h3>State Machine</h3>

<p>
The game uses a state-based architecture to control the flow of the application.
</p>

<ul>
<li>Main Menu</li>
<li>Game State</li>
<li>Score Screen</li>
<li>Credits</li>
</ul>

<h3>Collision System</h3>

<p>
Collision handling was implemented manually. Each entity in the game has its own collision detection system, including Pac-Man and the ghosts. These systems determine whether movement is allowed within the map, preventing characters from passing through walls and detecting interactions such as Pac-Man being caught by a ghost.
</p>

<p>
Invisible bumpers and interaction objects are used to control movement and environmental interactions. When a collision occurs, the system determines how the entity should react within the game world.
</p>

<p>
Ghosts also use a simple decision system that behaves like a lightweight artificial intelligence. After encountering obstacles or collisions, they evaluate possible directions and continue navigating the maze, allowing them to pursue or intercept the player while respecting the map layout.
</p>

<p>
Ghost behaviors and interactions were implemented independently rather than copying original Pac-Man logic.
</p>

<h3>Teleportation Tunnel</h3>

<p>
The classic Pac-Man tunnel mechanic was recreated, allowing the player to travel from one side of the map to the other.
</p>

<h3>Score System</h3>

<p>
High scores are stored persistently using a binary file:
</p>

<pre>
pacmanScores.bin
</pre>

<p>
This allows score data to persist between sessions.
</p>

---

<h2>Art and Assets</h2>

<p>
All visual animations were created manually in pixel art. The project includes:
</p>

<ul>
<li>Handmade sprite animations</li>
<li>Custom UI screens</li>
<li>Menus and score displays</li>
<li>Sound effects</li>
</ul>

<p>
Rendering and audio are handled through the Raylib multimedia library.
</p>

---

<h2>Technologies Used</h2>

<ul>
<li>C programming language</li>
<li>Raylib (graphics and audio)</li>
<li>Emscripten</li>
<li>WebAssembly</li>
<li>GitHub Pages</li>
</ul>

---

<h2>Why This Project Matters</h2>

<p>
This project represents the beginning of my journey into programming.
</p>

<p>
It taught me how software is structured, how memory works, how to design readable code, and how to transform an idea into a complete working system.
</p>

<p>
Even a simple arcade game can become a powerful exercise in learning software engineering fundamentals.
</p>

---

<h2>License</h2>

<p>
This project is provided for educational and portfolio purposes.
</p>
