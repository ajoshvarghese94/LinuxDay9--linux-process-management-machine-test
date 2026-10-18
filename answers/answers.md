# Answers: Process Management Machine Test

## 1. Display the currently logged-in user
```bash
whoami
```
Screenshot: `screenshots/task01-whoami.png`

## 2. Display processes running in the current terminal session
```bash
ps
```
Screenshot: `screenshots/task02-ps.png`

## 3. Display all running processes with detailed information
```bash
ps aux
```
Alternative: `ps -ef`

Screenshot: `screenshots/task03-ps-aux.png`

## 4. Find all Bash shell processes
```bash
ps aux | grep bash
ps -ef | grep bash
```
Screenshot: `screenshots/task04-grep-bash.png`

## 5. Install the htop package
```bash
sudo apt install htop
```
Result: htop is already the newest version (3.4.1-5build2).

Screenshot: `screenshots/task05-install-htop.png`

## 6. Launch htop and verify CPU and Memory usage
```bash
htop
```
CPU bars (0 to 3), Mem and Swp usage are visible at the top.

Screenshot: `screenshots/task06-htop.png`

## 7. Create a process that runs for 5 minutes (new terminal)
```bash
sleep 300
```
Screenshot: `screenshots/task07-sleep-300.png`

## 8. Search for the process created in Step 7
```bash
ps -ef | grep sleep
```
Alternative: `ps aux | grep sleep`

Screenshot: `screenshots/task08-search-process.png`

## 9. Identify the PID of the process
```bash
pgrep sleep
```
Screenshot: `screenshots/task09-pgrep.png`

## 10. Open the real-time process monitoring tool
```bash
top
```
Screenshot: `screenshots/task10-top.png`

## 11. Terminate the process using its PID
```bash
pgrep sleep
kill <PID>
```
Screenshot: `screenshots/task11-kill.png`

## 12. Verify the process was terminated
The terminal running `sleep 300` printed `Terminated`, confirming the process was stopped.

Screenshot: `screenshots/task12-terminated.png`

## 13. Create another process that runs for 10 minutes
```bash
sleep 600
```
Screenshot: `screenshots/task13-sleep-600.png`

## 14. Find the PID of the new process
```bash
pgrep sleep
```
Screenshot: `screenshots/task14-pgrep-new.png`

## 15. Forcefully terminate the process
```bash
kill -9 <PID>
```
`-9` sends SIGKILL, which cannot be caught or ignored.

Screenshot: `screenshots/task15-kill-9.png`

## 16. Verify the process is no longer running
```bash
ps -ef | grep sleep
```
Only the `grep` command itself appears, so the `sleep` process is gone.

Screenshot: `screenshots/task16-verify.png`
