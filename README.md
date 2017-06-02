# convert2asm
Utility to convert french schools' staff, students and classes information to a compatible Apple School Manager CSV archive ready for SFTP upload.

Usage: convert2asm format source_directory [password_policy_option] [--parse-emails] [--split-classes-by-topic] [--disable-classes-prefix]

       format: source files format (siecle+stsweb, itop, anonymous, ...)
       source_directory: path to the directory containing the files to convert
       [password_policy_option]: optional students password policy (4, 6 or 8). Default is 4 digits.
       [--parse-emails]: parse staff & students emails if available. Emails are ignored by default.
       [--split-classes-by-topic]: create one Apple School Manager class per topic teached in the class (ex: "class 1 - Maths", "class 1 - Biology", ...).
       [--disable-classes-prefix]: stop prefixing classes by their location name.

Example: convert2asm siecle+stsweb ~/XML_EXPORTS/ 6 --parse-emails

Example: convert2asm itop ~/CSV_ITOP_EXPORTS/ 4

Example: convert2asm anonymous ~/ANONYMOUS_TEMPLATES/
