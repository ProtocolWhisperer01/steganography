# Steganography

---

This is an overview of what steganography is and techniques used in CTFs :smiley:.

1. Determine the file type

	file [filename]
	
2. View all the strings in the file

	- strings [filename]
	- strings -t x -n 7 [filename]
# use -n 7 for strings of length 7+, and -t x to view- their position in the file

3. Determine the metadata

	exiftool -a -u -g1 [filename]
	
4. Check for embedded files or zipped files
	
	binwalk -e [filename]

5.  Look for optional/correct broken chunks	

	pngcheck -vtp7f [filename]
	
# v is for verbose, t and 7 display tEXt chunks, p displays contents of some other optional chunks and f forces continuation after major errors are encountered. 


6. Images can be hidden in colour/bit panes.

	Use this site... https://stegonline.georgeom.net/upload
	
