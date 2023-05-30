# Running a job on the IDA cluster

Ensure all files are available on sebastiansvol1claim/lighton on sebastians@idagpu-head.dcs.gla.ac.uk 
Use FileZilla or SCP to copy any remaining files.
Change the group of all files and folders that are accessed from within a container
chgrp nfsnobody ~/<username>vol1claim/

open a browser window and navigate to
https://console.ida.dcs.gla.ac.uk/k8s/ns/sebastiansproject/jobs
Click "Create Job" and copy the content of JOB.yaml from here into the text field. Click "Create" to initiate and run the job.