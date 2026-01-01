# BENCHMARK WITH DELTA SYSTEM [STANDALONE]

<div align="center">
<img src="https://github.com/user-attachments/assets/33f3f877-478f-487e-911a-56d6cb62ff96" width="206px" />
<img src="https://github.com/user-attachments/assets/7b175e5d-f4c0-45c5-a28d-0d61c5a036e8" width="500px" />
</div>

## DESCRIPTION

Benchmark is a comprehensive vehicle performance testing tool for FiveM servers. This standalone resource provides real-time performance metrics for any vehicle in the game, allowing players to measure acceleration, top speed, and distance times with precision and style.

The benchmark displays a sleek, customizable UI that shows critical performance data including 0-60 MPH times, quarter-mile runs, top speed, and much more. Perfect for car enthusiasts, racing servers, vehicle developers, and anyone who wants to compare vehicle performance with accurate metrics.

**Inspired in [GTAWiseGuy](https://www.twitch.tv/gtawiseguy) benchtime script**

## GET NOW

* [DOWNLOAD](https://dking.tebex.io/package/6745605)

## KEY FEATURES

- 🚀 **Comprehensive Performance Metrics**:
  - Speed benchmarks (0-60 MPH, 0-100 MPH, 0-120 MPH, etc.)
  - Distance benchmarks (⅛ Mile, ¼ Mile, ½ Mile, 1 Mile, etc.)
  - Top speed measurement
  - Average times for all metrics

- ⚙️ **Fully Customizable**:
  - Configurable speed and distance benchmarks
  - Adjustable UI position and scale
  - Customizable commands and key bindings
  - Support for both Imperial (MPH/Miles) and Metric (KPH/Kilometers) units

- 🎮 **User-Friendly Interface**:
  - Clean, modern UI design
  - Real-time updates
  - Vehicle name and class display
  - Color-coded status indicators

- 🔧 **Advanced Functionality**:
  - Pause/resume benchmark testing
  - Reset functionality
  - Persistent settings between sessions

- **Versatile Commands**:
  - `/benchmark` - Toggle the benchmark display
  - `/movebenchmark` - Reposition the UI with drag-and-drop
  - `/resetbench` - Reset all benchmark data
  - `/pausebench` - Pause/resume the current benchmark
  - `/togglespeed` - Switch between MPH and KPH
  - `/toggledistance` - Switch between Miles and Kilometers
  - `/benchdelta` - Delta System
  - `/saverun` - Save the current run

## DELTA SYSTEM

The Delta System provides an easy way to save benchmark runs and compare two runs side-by-side, showing precise differences in performance metrics. It is designed for players and vehicle tuners to quickly see what changed between runs (improvements or regressions) without inspecting raw numbers.

- What it does:
  - Save a run locally (temporary ID) or persist it to the server database.
  - Select any saved run as **BASE** and another as **COMPARE**.
  - Automatically calculate deltas for: overall score, top speed, total time, each configured speed benchmark (e.g. 0–60), and distance benchmarks (¼ mile, ½ mile, etc.).
  - Display signed differences (e.g. +0.35s or −0.12s) with color-coded indicators (green for faster, red for slower).

- Workflow:
  1. Open the Runs UI (`/benchruns` or configured keybind).
  2. Save your current run (use the "SAVE CURRENT RUN" button or the command `/saverun`).
  3. Choose one run as **BASE** and another as **COMPARE**.
  4. The differences will be displayed in the **DELTA** column.

- Why it’s useful:
  - Quickly compare tuning changes, setups, or modifications between runs.
  - Provides a clear numeric and visual way to validate improvements.

## HOW IT WORKS

1. **Start the Benchmark**: Use the `/benchmark` command to display the UI
2. **Position the UI**: Use `/movebenchmark` to drag the UI to your preferred position
3. **Begin Testing**: Simply drive forward to automatically start the benchmark
4. **View Results**: Watch in real-time as the benchmark records your vehicle's performance
5. **Compare Results**: The benchmark keeps track of your recent times, showing averages for comparison

The benchmark automatically detects when you start moving forward and begins timing. It records when you hit specific speed thresholds and distance markers, providing accurate measurements of your vehicle's performance capabilities.

When you stop the vehicle, the benchmark saves your results and displays averages from your recent runs, allowing you to compare performance across multiple tests.

## TECHNICAL DETAILS

- **Standalone Resource**: No dependencies required
- **Persistent Storage**: Saves user preferences using FiveM's KVP system
- **Customizable Configuration**: Extensive options in the config.lua file

## INSTALLATION

1. Download the script
2. Place it in your resources folder
3. Add `ensure dking_benchmark` to your server.cfg
4. Start the resource

## CONFIGURATION

The script is highly configurable through the `config.lua` file:

- Add or modify speed benchmarks
- Customize distance measurements
- Set default units (Imperial or Metric)
- Configure commands
- Adjust notifications
- Set key bindings for quick use
<details>
  <summary><h2 style="display: inline;">Image</h2></summary>

  <div align="left">
    <img src="https://github.com/user-attachments/assets/7e2984fd-8e43-41d2-b2c5-f1dd4fd3f427" width="600px" />
  </div>
</details>

## PREVIEW

* [YouTube](https://youtu.be/TGAf2khOruE)

<details>
  <summary><h2 style="display: inline;">Delta System</h2></summary>

  <div align="left">
    <img src="https://github.com/user-attachments/assets/ce481b2f-30d5-4d56-aca2-61950ea4d0f6" width="700px" />
    <img src="https://github.com/user-attachments/assets/27f2601f-6605-48f5-9e05-ae3a3c064b08" width="700px" />
    <img src="https://github.com/user-attachments/assets/7b175e5d-f4c0-45c5-a28d-0d61c5a036e8" width="700px" />
  </div>
</details>

## DEPENDENCIES

* [ox_lib](https://github.com/overextended/ox_lib) (Optional, used only for notifications)
* [oxmysql](https://github.com/overextended/oxmysql)

## SUPPORT

* ### [Discord](https://discord.gg/Rw6vjcXspG)

## CHANGELOGS

<details>
  <summary><h2 style="display: inline;">Expand</h2></summary>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.0.2</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Fixed distance and speed unit conversion.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.0.3</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Added translation system;</li>
      <li>Command and notify configs moved to separate files;</li>
      <li>Minor changes and improvements to the benchmark UI;</li>
      <li>Added the Delta System, to save and compare the runs made in the benchmark.</li>
    </ul>
  </details>

  <details>
    <summary style="margin-left: 20px;"><h3 style="display: inline;">1.0.4</h3></summary>
    <ul style="margin-left: 20px;">
      <li>Added the <code>/autopause</code> command, now it is possible to set a speed, time, or distance for the benchmark to pause automatically;</li>
      <li>Changes in the database.</li>
    </ul>
  </details>
</details>

## COPYRIGHT

### BY [DKING](https://github.com/Dking07) 2026 ©