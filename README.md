# sat6-rex-patching

Script to schedule remote execution jobs for installing available errata and reboot after updates that require reboot. 

Example usage:

Copy the script to your Satellite server (if you want to run it from another server, you have to change the URL in the code from "localhost" to your Satellite hostname).

Read the help text so see what information you need to provide:

./sat6-rex-patching.py --help

First run without "--apply" to see that the resulting jobs looks OK:

./sat6-rex-patching.py --username admin --password redhat --organization My_Org --host-collection Test --apply-time "2017-11-11 11:11:11" --reboot-time "2017-11-12 11:11:11"

Then run with "--apply" to actually schedule the jobs:

./sat6-rex-patching.py --username admin --password redhat --organization My_Org --host-collection Test --apply-time "2017-11-11 11:11:11" --reboot-time "2017-11-12 11:11:11" --apply
