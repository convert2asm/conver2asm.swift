# convert2asm
Utility to convert french schools' staff, students and classes information to a compatible Apple School Manager CSV archive ready for SFTP upload.

Usage: convert2asm format source_directory [password_policy_option]

       format: source files format (siecle+stsweb, ...)
       source_directory: path to the directory containing the files to convert
       [password_policy_option]: optional students password policy (4, 6 or 8). Default is 4 digits.

Example: convert2asm siecle+stsweb ~/XML_EXPORTS/ 6