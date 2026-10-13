# CyberStory : CrackStation Wordlist — Linux Command-Line Guide

Note:  This is my personal experience just share for your reference|||  

A beginner-friendly guide to inspecting, validating, and reading large GZIP-compressed text files using Linux terminal commands.

This project documents how to work with the CrackStation human-only wordlist on Kali Linux and other Linux distributions.The guide covers: 
Identifying compressed file formats
Reading large text files without opening the entire file in a text editor
Extracting GZIP archives
Checking file integrity
Understanding basic Linux command-line operations


Use responsibly: Wordlists should only be used for authorized security testing, password auditing, and cybersecurity education.

🛠️ Requirements
Kali Linux or another Linux distribution
Terminal access
gzip, file, head, and zcat
Sufficient disk space for the compressed and extracted files

Step 1 -- Navigate to Downloads:
cd ~/Downloads
ls -lh

ls -lh crackstation-human-only.txt.gz***

Step 2 -- Identify the File Type 
file crackstation-human-only.txt.gz

✅ Step 3 — Validate the GZIP Archive
gzip -t crackstation-human-only.txt.gz
echo $? 

👀 Step 4 — Read Data Without Extracting

zcat crackstation-human-only.txt.gz | head -n 10                ==Display the first 10 lines:
zcat crackstation-human-only.txt.gz | head -n 100               ==Display the first 100 lines:
zcat crackstation-human-only.txt.gz | head -n 1000              ==Display the first 1000 lines:
zcat crackstation-human-only.txt.gz | head -n 10000             ==Display the first 1000 lines:  


⚠️ Important Notes

.gz is a GZIP format, not a ZIP archive. Use gzip or gunzip, not unzip.
Avoid opening very large text files directly in a graphical editor.
A successful GZIP integrity test does not verify the file's origin or authenticity.
Compare a cryptographic checksum with a trusted, independently published checksum when available.
Never use password dictionaries to access accounts or systems without authorization.

🔗 References: official page you can downloads file from this official website
CrackStation: [https://crackstation.net/     ](https://crackstation.net/crackstation-wordlist-password-cracking-dictionary.htm)      


📚 Learning Purpose
This repository is intended for Linux command-line learning and authorized cybersecurity practice.
It documents file-handling commands rather than distributing the original wordlist.



<img width="1786" height="921" alt="CrackStationPassw" src="https://github.com/user-attachments/assets/2d6a0c94-f068-4ca6-9f3e-354c388f1728" />




