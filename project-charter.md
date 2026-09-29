# Team charter and project roadmap

## Team

Team Name: The Croquetones

| No. | Full name | Group | GitHub username |
| --- | --------- | ----- | --------------- |
| 1.  | Oscar Marín Castro | Exchange | @Oscar21-prog |
| 2.  | Víctor Jesús Castañeda Morales | Exchange | @vicctoor18 |
| 3.  | Jaime de Luiz García | Exchange | @jaimedeluiz |
| 4.  | Jaime Eráns Rodríguez | Exchange | @jaimeerans12 |
| 5.  | Carmelo Fabio Occhipinti | Exchange | @occhicf |

The whole team will participate in seminars on Tuesdays (starting at 14:00).

## Team's goal

- Achieve a high grade in the project (aiming for 9/10 or higher).
- Build a working and reliable software tool that solves OptiCharge's scheduling problem and improves charger usage.
- Follow good software engineering practices (clean code, clear commits, tests, and active code reviews).
- Ensure equal participation and a fair learning experience for all team members.

## Shared norms and way of working

- **Roles & Tasks:** 
  - All team members will write code, create tests, and review each other's work.
  - We will rotate the "team lead" role every two weeks to organize issues on GitHub and track active tasks.
- **Communication:**
  - We use Discord/Slack for regular updates, technical discussions, and links.
  - We use WhatsApp for quick notices or urgent messages.
  - We will hold a weekly meeting (about 20–30 minutes) to review progress and plan the next sprint.
  - Expected response time on weekdays is within 24 hours.
- **Workload & Contribution:** 
  - We all commit to equal contribution (target: 20% each).
  - All work will be tracked using GitHub Issues and Pull Requests to maintain full visibility.
  - If a team member falls behind, we will discuss it in the weekly meeting and reassign tasks so they can catch up the following week.
- **Quality & Workflow:** 
  - Nobody pushes code directly to `main`.
  - Every change requires a Pull Request (PR) with at least one approval from another teammate before merging.
  - Automated tests must pass before merging.
  - If a reviewer requests changes, the author will address them within 48 hours.

## Project scope

We are building a command-line and reporting tool called **OptiCharge**. The tool takes daily charging requests and station constraints (charger types, station power limits, and hourly electricity tariffs) and creates an optimized 1-hour charging schedule that maximizes the number of satisfied vehicles compared to the standard First-Come-First-Served (FCFS) strategy.

**In scope:**
- Reading and validating input files (cars, chargers, limits, prices).
- Baseline FCFS scheduling engine for benchmark comparison.
- Smart scheduling algorithm to maximize satisfied vehicles while respecting all power limits.
- Plain-text operator sheet with clear hourly plug/unplug instructions.
- Visual summary dashboard (`report.html`) and automated performance comparison.
- Synthetic scenario generator script to test busy and quiet days.
- Optional cost-aware optimization to favor cheaper electricity hours when possible.

**Out of scope:**
- Payment processing and billing systems.
- Live telemetry or real-time GPS tracking.

## Milestones

| No. | Target date | Description |
| --- | ----------- | ----------- |
| 1.  | 2026-10-06  | **Input validation & summary tool:** A working CLI tool that reads and validates station configuration and vehicle requests from files, reports friendly error messages for bad data, and outputs a summary of total energy demand for the operator. |
| 2.  | 2026-10-27  | **Baseline FCFS & initial optimizer (Mid-course Demo):** Complete working FCFS baseline scheduler that calculates benchmark metrics, alongside the first working version of our smart optimization algorithm, ready for the mid-course presentation. |
| 3.  | 2026-11-17  | **Operator task sheet & performance comparison:** Generate the step-by-step text instruction file for the station operator (which car to plug/unplug each hour) and produce an automated comparison table showing OptiCharge gains over FCFS. |
| 4.  | 2026-12-01  | **Interactive HTML report & cost optimization:** Standalone `report.html` file to inspect schedules and charger usage visually, with cost-aware scheduling to lower electricity expenses during off-peak hours. |
| 5.  | 2026-12-15  | **Scenario generator, full testing & final demo prep:** Test data generator script (to easily test quiet vs. heavy traffic days), full end-to-end test verification, final documentation, and preparation for the final course presentation on 2026-12-22. |
