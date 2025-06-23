# CPP-NanoJourney

![C++17][cpp17-badge] ![CMake][cmake-badge] ![Multithreading][multithreading-badge] ![OpenCV][opencv-badge] ![SDL2][sdl2-badge] ![Memory Management][memory-badge] ![Algorithms][algorithms-badge]

> A comprehensive collection of C++ projects that demonstrates modern C++ features, concurrency, memory management, and graphics programming.

## 🎯 Overview

This repository contains 5 complete C++ projects that demonstrate key concepts in modern C++ development, from fundamental algorithms to advanced concurrency patterns. Each project includes complete build instructions, comprehensive documentation, and visual demonstrations.

---

## 📋 Projects

### 1. Route Planning Project

![A* Pathfinding][astar-badge] ![OpenStreetMap][osm-badge] ![IO2D][io2d-badge]

**A* pathfinding algorithm implementation using OpenStreetMap data with IO2D graphics rendering**

<img src="Route-Planning-Project/map.png" width="600" alt="Route planning visualization showing optimal path calculated using A* algorithm on OpenStreetMap data"/>

#### Key Features
- A* search algorithm implementation for optimal pathfinding
- Real-world OpenStreetMap (OSM) data integration
- Interactive graphics rendering with IO2D library
- Comprehensive unit testing with Google Test
- CMake build system with external dependencies

#### Build & Run
<details>
<summary>🔨 Build & Run Instructions</summary>

```bash
# Build
mkdir build && cd build
cmake .. && make

# Run
./OSM_A_star_search
# Or with custom map file:
./OSM_A_star_search -f ../<your_osm_file.osm>

# Test
./test
```

</details>

#### Screenshots
<details>
<summary>📸 Additional Screenshots</summary>

<img src="Route-Planning-Project/screenshots/build_log.png" width="600" alt="Build process output showing successful compilation of Route Planning Project"/>

<img src="Route-Planning-Project/screenshots/compiled_results.png" width="600" alt="Compiled executable running and displaying route planning interface"/>

<img src="Route-Planning-Project/screenshots/test_OSM_results.png" width="600" alt="Unit test results showing all OpenStreetMap parsing tests passing successfully"/>

</details>

#### Quick Start
```bash
# Clone with submodules
git clone https://github.com/udacity/CppND-Route-Planning-Project.git --recurse-submodules

# Build
mkdir build && cd build
cmake ..
make

# Run
./OSM_A_star_search
# Or with custom map file:
./OSM_A_star_search -f ../<your_osm_file.osm>

# Test
./test
```

**Technologies:** C++17, CMake, IO2D, Google Test, OpenStreetMap API

---

### 2. System Monitor

![Linux][linux-badge] ![ncurses][ncurses-badge] ![OOP][oop-badge]

**Linux system monitor built with ncurses displaying real-time process and system information**

<img src="System-Monitor-/images/monitor.png" width="600" alt="System monitor interface showing real-time CPU usage, memory consumption, and active processes in terminal"/>

#### Key Features
- Object-oriented design with System, Process, and Processor classes
- Real-time Linux system file parsing (/proc filesystem)
- Interactive terminal UI with ncurses library
- Live CPU and memory usage monitoring
- Process information display and management

#### Build & Run
<details>
<summary>🔨 Build & Run Instructions</summary>

```bash
# Build
mkdir build && cd build
cmake .. && make

# Run
./monitor

# Alternative: Use Makefile
make build
./build/monitor
```

</details>

#### Screenshots
<details>
<summary>📸 Additional Screenshots</summary>

<img src="System-Monitor-/images/starting_monitor.png" width="600" alt="System monitor startup screen showing initialization process and loading system information"/>

</details>

#### Quick Start
```bash
# Clone
git clone https://github.com/udacity/CppND-System-Monitor-Project-Updated.git

# Install dependencies
sudo apt install libncurses5-dev libncursesw5-dev

# Build
make build

# Run
./build/monitor

# Development
make format  # Apply ClangFormat styling
make debug   # Build with debugging symbols
make clean   # Clean build artifacts
```

**Technologies:** C++17, ncurses, Linux /proc filesystem, Makefile

---

### 3. Concurrent Traffic Simulation

![Concurrency][concurrency-badge] ![Threading][threading-badge] ![Synchronization][sync-badge]

**Multi-threaded traffic simulation with traffic lights using modern C++ concurrency features**

<img src="Concurrent-Traffic-Simulation/data/traffic_simulation.gif" width="600" alt="Animated traffic simulation showing vehicles navigating intersections with synchronized traffic lights"/>

#### Key Features
- Concurrent programming with std::thread
- Thread synchronization with mutexes and locks
- Message queues for inter-thread communication
- Traffic light state management with std::condition_variable
- OpenCV graphics rendering for real-time visualization
- Thread-safe intersection management

#### Build & Run
<details>
<summary>🔨 Build & Run Instructions</summary>

```bash
# Build
mkdir build && cd build
cmake .. && make

# Run
./traffic_simulation
```

</details>

#### Background Assets
<details>
<summary>🏙️ City Backgrounds</summary>

<img src="Concurrent-Traffic-Simulation/data/nyc.jpg" width="300" alt="New York City street intersection background for traffic simulation"/> <img src="Concurrent-Traffic-Simulation/data/paris.jpg" width="300" alt="Paris street intersection background for traffic simulation"/>

</details>

#### Quick Start
```bash
# Build
mkdir build && cd build
cmake .. && make

# Run
./traffic_simulation
```

#### Technical Implementation
- TrafficLight class with red/green phases (4-6 second random intervals)
- MessageQueue with thread-safe send/receive operations
- Vehicle blocking mechanism until green light signal
- Concurrent traffic light cycling across multiple intersections

**Technologies:** C++17, std::thread, std::mutex, std::condition_variable, OpenCV, CMake

---

### 4. Memory Management Chatbot

![Smart Pointers][smart-pointers-badge] ![Move Semantics][move-semantics-badge] ![RAII][raii-badge]

**Interactive chatbot demonstrating C++ memory management concepts with smart pointers and move semantics**

<img src="Memory-Management-Chatbot/images/chatbot_demo.gif" width="600" alt="Animated demonstration of chatbot interface showing interactive conversation about C++ memory management concepts"/>

#### Key Features
- Smart pointer implementation (unique_ptr, shared_ptr)
- Rule of Five compliance and move semantics
- RAII (Resource Acquisition Is Initialization) patterns
- wxWidgets GUI framework integration
- Knowledge graph data structure for conversation flow
- Memory leak elimination and proper ownership management

#### Build & Run
<details>
<summary>🔨 Build & Run Instructions</summary>

```bash
# Build
mkdir build && cd build
cmake .. && make

# Run
./membot
```

</details>

#### Screenshots
<details>
<summary>💭 Chatbot Interface</summary>

<img src="Memory-Management-Chatbot/images/chatbot_demo.png" width="600" alt="Chatbot interface showing conversation window with memory management Q&A session"/>

<img src="Memory-Management-Chatbot/images/chatbot.png" width="300" alt="Chatbot avatar icon used in the GUI interface"/> <img src="Memory-Management-Chatbot/images/user.png" width="300" alt="User avatar icon used in the GUI interface"/>

</details>

#### Quick Start
```bash
# Build
mkdir build && cd build
cmake .. && make

# Run
./membot
```

#### Technical Implementation
- Exclusive ownership management with smart pointers
- Rule of Five compliance for ChatBot class
- Efficient object transfer using move semantics
- Complete memory leak elimination
- Advanced pointer ownership patterns

**Technologies:** C++17, wxWidgets, Smart Pointers, Move Semantics, CMake

---

### 5. Enhanced Snake Game (Capstone)

![Game Development][gamedev-badge] ![File I/O][fileio-badge] ![Real-time][realtime-badge]

**Modern C++ Snake game featuring multithreading, file I/O, and leaderboard system**

<img src="Snake-Game/snake_game.gif" width="600" alt="Animated Snake game showing gameplay with snake moving, eating food, growing longer, and score tracking"/>

#### Key Features
- Multithreaded programming with std::thread
- Thread synchronization (mutex, condition_variable, unique_lock)
- Persistent high score system with file I/O
- STL containers and algorithms for game logic
- SDL2 graphics and real-time game loop
- RAII thread management and proper cleanup

#### Build & Run
<details>
<summary>🔨 Build & Run Instructions</summary>

```bash
# Build
mkdir build && cd build
cmake .. && make

# Run
./SnakeGameApp
```

</details>

#### Quick Start
```bash
# Build
mkdir build && cd build
cmake ..
make

# Run
./SnakeGameApp
```

#### Features Implemented
- Player name input and validation system
- High score persistence to `highscores.txt`
- Top 5 leaderboard display with sorting
- BonusSpawner running on background thread
- Thread-safe bonus feature toggling
- Concurrent game mechanics with proper cleanup

**Technologies:** C++17, SDL2, std::thread, File I/O, STL, CMake

---

## 🛠️ Technologies & Skills Demonstrated

### Core C++ Concepts
![C++17][cpp17-badge] ![OOP][oop-badge] ![STL][stl-badge] ![Templates][templates-badge]

### Memory Management
![Smart Pointers][smart-pointers-badge] ![Move Semantics][move-semantics-badge] ![RAII][raii-badge] ![Memory Management][memory-badge]

### Concurrency & Threading
![Multithreading][multithreading-badge] ![Concurrency][concurrency-badge] ![Threading][threading-badge] ![Synchronization][sync-badge]

### Graphics & UI
![SDL2][sdl2-badge] ![OpenCV][opencv-badge] ![wxWidgets][wxwidgets-badge] ![ncurses][ncurses-badge] ![IO2D][io2d-badge]

### Tools & Build Systems
![CMake][cmake-badge] ![Google Test][gtest-badge] ![Git][git-badge] ![Linux][linux-badge]

### Algorithms & Data Structures
![Algorithms][algorithms-badge] ![A* Pathfinding][astar-badge] ![Data Structures][datastructures-badge]

---

## 📊 Project Statistics

- **Total Projects:** 5
- **Lines of Code:** 2,500+
- **Media Assets:** 11 (5 primary demos + 6 supporting images)
- **Build Systems:** CMake, Makefile
- **External Libraries:** 8+ (SDL2, OpenCV, wxWidgets, ncurses, IO2D, Google Test)
- **C++ Features:** Smart Pointers, Move Semantics, Threading, Templates, STL

---

## 🚀 Getting Started

### Prerequisites
```bash
# Ubuntu/Debian
sudo apt update
sudo apt install build-essential cmake git
sudo apt install libsdl2-dev libopencv-dev libwxgtk3.0-gtk3-dev
sudo apt install libncurses5-dev libncursesw5-dev

# Clone repository
git clone <repository-url>
cd CPP-NanoJourney
```

### Build All Projects
```bash
# Each project has its own build instructions
# See individual project sections above for specific commands
```

---

## 📚 Learning Outcomes

This portfolio demonstrates mastery of:

- **Object-Oriented Programming** - Proper class design, inheritance, and polymorphism
- **Memory Management** - Smart pointers, RAII, and leak prevention
- **Concurrency** - Thread synchronization, message passing, and parallel processing
- **Data Structures & Algorithms** - A* pathfinding, STL containers, and algorithmic thinking
- **Graphics Programming** - Real-time rendering, event handling, and UI design
- **File I/O & Persistence** - Data serialization, file handling, and state management
- **Build Systems** - CMake configuration, dependency management, and cross-platform builds
- **Testing** - Unit testing, integration testing, and verification strategies

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<!-- Badge Definitions -->
[cpp17-badge]: https://img.shields.io/badge/C%2B%2B-17-blue.svg?style=flat&logo=c%2B%2B
[cmake-badge]: https://img.shields.io/badge/CMake-3.11%2B-064F8C.svg?style=flat&logo=cmake
[multithreading-badge]: https://img.shields.io/badge/Multithreading-std%3A%3Athread-green.svg?style=flat
[opencv-badge]: https://img.shields.io/badge/OpenCV-4.1%2B-5C3EE8.svg?style=flat&logo=opencv
[sdl2-badge]: https://img.shields.io/badge/SDL2-2.0%2B-1F5F99.svg?style=flat
[memory-badge]: https://img.shields.io/badge/Memory%20Management-Smart%20Pointers-orange.svg?style=flat
[algorithms-badge]: https://img.shields.io/badge/Algorithms-A%2A%20%7C%20Pathfinding-red.svg?style=flat
[astar-badge]: https://img.shields.io/badge/A%2A-Pathfinding-FF6B6B.svg?style=flat
[osm-badge]: https://img.shields.io/badge/OpenStreetMap-OSM%20Data-7EBC6F.svg?style=flat
[io2d-badge]: https://img.shields.io/badge/IO2D-Graphics-4ECDC4.svg?style=flat
[linux-badge]: https://img.shields.io/badge/Linux-System%20Programming-FCC624.svg?style=flat&logo=linux
[ncurses-badge]: https://img.shields.io/badge/ncurses-Terminal%20UI-000000.svg?style=flat
[oop-badge]: https://img.shields.io/badge/OOP-Object%20Oriented-purple.svg?style=flat
[concurrency-badge]: https://img.shields.io/badge/Concurrency-Parallel%20Processing-brightgreen.svg?style=flat
[threading-badge]: https://img.shields.io/badge/Threading-std%3A%3Athread-blue.svg?style=flat
[sync-badge]: https://img.shields.io/badge/Synchronization-Mutex%20%7C%20CV-yellow.svg?style=flat
[smart-pointers-badge]: https://img.shields.io/badge/Smart%20Pointers-unique__ptr%20%7C%20shared__ptr-orange.svg?style=flat
[move-semantics-badge]: https://img.shields.io/badge/Move%20Semantics-C%2B%2B11%2B-red.svg?style=flat
[raii-badge]: https://img.shields.io/badge/RAII-Resource%20Management-green.svg?style=flat
[gamedev-badge]: https://img.shields.io/badge/Game%20Dev-SDL2%20%7C%20Real--time-9B59B6.svg?style=flat
[fileio-badge]: https://img.shields.io/badge/File%20I%2FO-Persistence-3F51B5.svg?style=flat
[realtime-badge]: https://img.shields.io/badge/Real--time-Game%20Loop-FF5722.svg?style=flat
[stl-badge]: https://img.shields.io/badge/STL-Standard%20Library-607D8B.svg?style=flat
[templates-badge]: https://img.shields.io/badge/Templates-Generic%20Programming-8BC34A.svg?style=flat
[wxwidgets-badge]: https://img.shields.io/badge/wxWidgets-GUI%20Framework-2196F3.svg?style=flat
[gtest-badge]: https://img.shields.io/badge/Google%20Test-Unit%20Testing-4CAF50.svg?style=flat
[git-badge]: https://img.shields.io/badge/Git-Version%20Control-F05032.svg?style=flat&logo=git
[datastructures-badge]: https://img.shields.io/badge/Data%20Structures-STL%20Containers-795548.svg?style=flat
