0.7

* Fix problems with flow and python3.12 by moving wait_for step into set_package_stream task
* Set ansible_connection=local for localhost

---

0.6

* Increase timeout waiting after installation reboot to accomodate double reboots of systems with Realtek network cards
* Package cpu-microcode replaces devcpu-data

---

0.5

* Various updates
* Quote task names with variables
* Add python virtualenv info
* Add "--no-check-certificate" to wget command

---

0.4

* Update wipe disks section to work with tmux session
* Testing with FreeBSD 14.0 QA images

---

0.3

* Call inventory variable for run.sh filename

---

0.2

* Fixing tmux send-keys duplicate zroot issue
* Save facts locally

---

0.1

* Adding CHANGELOG FILE

---

0.0

* Initiatiating repo
