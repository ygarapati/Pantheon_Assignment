# Pantheon
# Project Summary
This project compares the performance of TCP BBR, PCC-Allegro, and QUIC Cubic congestion control protocols using the Pantheon framework under varied network scenarios.
# System Requirements:
Ubuntu/Linux OS
Python 2.7.18
# Steps To Install And Run Pantheon:
# Step 1: Install Pantheon
git clone https://github.com/StanfordSNR/pantheon.git
# Step 2: Install Dependencies
src/experiments/setup.py --install-deps --all
# Step 3: Install MahiMahi
$ git clone https://github.com/ravinet/mahimahi
$ cd mahimahi
$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
# Step 4: Setup
src/experiments/setup.py --setup --all
# Step 5: Run Pantheon
src/experiments/test.py local --all
# Step 6: Analyzing The Test Result
src/analysis/analyze.py --data-dir DIR
A Report and Log File Will Be Created With the Scheme Name as we give In Place Of DIR.
# Step 7: Running a single congestion control scheme
src/wrappers/<cc>.py receiver port
src/wrappers/<cc>.py sender port
Needed to be run in different windows.
Generate Plots And Graphs that are found in Data and Pantheon_Report.Pdf

