# Linux Process Management: Machine Test

DevOps Linux Fundamentals machine test on process management, completed on Ubuntu (WSL).

## Repository Structure
```
.
├── README.md
├── answers/
│   └── answers.md        # commands used for all 16 tasks
└── screenshots/          # one screenshot per task (task01 ... task16)
```

## Tasks Covered
| # | Task | Command |
|---|------|---------|
| 1 | Display logged-in user | `whoami` |
| 2 | Processes in current terminal | `ps` |
| 3 | All processes, detailed | `ps aux` / `ps -ef` |
| 4 | Find Bash processes | `ps aux \| grep bash` |
| 5 | Install htop | `sudo apt install htop` |
| 6 | Launch htop | `htop` |
| 7 | Create a 5-minute process | `sleep 300` |
| 8 | Search for the process | `ps -ef \| grep sleep` |
| 9 | Identify the PID | `pgrep sleep` |
| 10 | Real-time monitoring | `top` |
| 11 | Terminate using PID | `kill <PID>` |
| 12 | Verify termination | shell prints `Terminated` |
| 13 | Create a 10-minute process | `sleep 600` |
| 14 | Find the new PID | `pgrep sleep` |
| 15 | Forcefully terminate | `kill -9 <PID>` |
| 16 | Verify it's gone | `ps -ef \| grep sleep` |

## Environment
- Ubuntu on WSL (Windows Subsystem for Linux)
- User: `Ajosh`

## Note
Screenshots were captured in different terminal sessions, so PID values differ between some screenshots. The commands and results are the same.

Full command list: [answers/answers.md](answers/answers.md)
