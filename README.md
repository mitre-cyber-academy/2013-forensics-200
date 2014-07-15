Name: Grains of Salt

Description: Another day, another beach. This time, you have to find the
remnants of a file that's been split up around the operating system. If only
you could <flag> someone down, you could get help <find>ing them. 
At least in this <ctf> challenge the <password>s are pretty straightforward.


How to Solve: Participants are provided with a VM which has parts of the flag
littered about a minimal Debian install. They are left without a GUI and with
no convinient slocate database with which to search. Instead, they need to 
craft a regex and use the find command to locate the pieces of the flag.
All but one of these are in files named with some variation of the string
flag (like xmlflagst, FlAg, flag.sh, etc.) sprinkled throughout the operating
system. From the root directory, as root, the following find command should
retrieve all of the real files, plus a few bogus ones:

find / -name *[l,L][a,A][g,G]*

By running (or reading) each of the files/scripts, 10/11 pieces of the flag
can be retrieved. The 11th flag piece isn't in a flag-labeled file, but 
mentioned in the motd, which requires the user to actually boot the machine,
rather than just mounting it. 

What to distribute:
[ctf_mach.tar.gz](https://drive.google.com/file/d/0B48Lv30KB1seV3M2Mm9seFhZazg/edit?usp=sharing) - This is a zip'd and tar'd version of the VM.

Flag: MCA-F1461015
