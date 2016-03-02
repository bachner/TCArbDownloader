# Threat Central ARB Downloader - linux bash script

##Background
This is a solution for those who have the Threat Central Model Import Connector (MIC) for ArcSight ESM installed in the internal network without access to the internet. The MIC though must have access to Arcsight ESM manager.

##Setup
1) Set an API key in the threatcentral.conf file.
2) Specify the location of the threatcentral.conf file in the conf_file field in the arbdownloader file.
3) Add the arbdownloader script to a cron-job to fetch the files every 5 minutes.

##DMZ side
The script should be running from the DMZ with access to threatcentral.io domain on port 443.

##Internal network
Take the arb files from the DMZ and put them in the MIC directory. E.g. C:\Program Files\ArcSightSmartConnectorsTC\current\user\agent\mic\tcmic\tc.
The connector should automatically process the files and update the active-lists in ESM.
