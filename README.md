# artwork_ingest_script
This bash script can be used by time-based media conservators and video preservation professionals. It will prompt the user to ingest digital video files and verify file fixity. This script is only compatible with MacOS.

How to download and set up:
1. Download ingest_automation.sh from this repository and save it anywhere.
2. In a MacOS terminal type: run chmod u+x
3. Then drag and drop the ingest_automation.sh file you downloaded into terminal and press enter. It should look like: thealy1 ~ % run chmod u+x /Users/thealy1/Downloads/ingest_automation.sh
4. Then, type: ./Users/thealy1/Downloads/ingest_automation.sh
5. It is ready to go for its first ingest!
6. When you want to use the script in the future, just drag and drop the ingest_automation.sh into a terminal window and it will begin.


This script can be modified for to fit custom workflow needs. The workflow used in this script is as follows:

1. Asks the user for the accession number, artist's name, and title.
2. Asks the user to drag the path for the artwork folder. This is where documentation associated with the artwork lives.
3. Subdirectories are created in the artwork folder: "Acquisition and Registration" "Artist Interaction" "Conservation" "Installation Reports and Exhibition Info" "Photo and Video Documentation" "Research" "Technical Info and Specs". This will allow for organization of complex documentation. If there is existing documentation in the artwork folder, it will not remove those files and they can be moved into the subdirectory as appropriate. It copies templates including "ActivityLog.doc" that serves as a log detailing all interventions and research conducted on the artwork and its components throughout its life; and CataloguingWorksheet.xlsx that will assist in the creation of components in collection cataloguing systems.
4. Asks the user to drag the path for the artist-provided drive. This can be a flash drive, external hard drive, CD, DVD, or Blu-Ray. 
5. Asks the user to drag the path for the digital repository. This is where artwork video files and other artwork assets live.
6. Files from the artist drive are transferred to the digital repository preserving the contents' file structure of the artist drive.
7. Metadata is captured and written to the Artwork folder > Conservation > Condition Reports folder. This includes mediainfo reports and framemd5s that capture the checksum for each frame of video. This may take a while to capture.
8. Checksums are verified between the artist drive contents and digital repository contents. If the script verifies that the md5 checksums match, it will write the checksum to the Artwork folder > Conservation > Condition Reports folder.
