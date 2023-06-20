**OLA trigger**  
To start an OLA trigger script from a button you can use press actions.  
Add a press action called "internal: System: Run shell path (local)"  
In the field "Path (supports variables in path)" just enter: ola_trigger -u1 /home/username/triggerfile.conf

To stop an OLA trigger script from running, use the same press action "internal: System: Run shell path (local)"  
In the field "Path (supports variables in path)" just enter: pkill -f "ola_trigger -u1 /home/username/triggerfile.conf"  
  
**OLA recorder playback**  
To start OLA recorder playback from a button you can use press actions.  
Add a press action called "internal: System: Run shell path (local)"  
In the field "Path (supports variables in path)" just enter: ola_recorder --playback /home/username/yourfile --iterations 0 --universes 1  
  
To stop an OLA recorder playback from running, use the same press action "internal: System: Run shell path (local)"  
In the field "Path (supports variables in path)" just enter: pkill -f "ola_recorder --playback /home/username/yourfile --iterations 0 --universes 1"  
  
  
It would probably generate some errors in the log file, displaying messages like 'Shell command failed. Guru meditation: {"code":null' – I don't know why yet, but it works, though.
