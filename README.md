# Email extraction with some filters using Python
 This repo is a python script which extracts email providing various filters to users

Libraries used:
1. imaplib
2. email
3. os
4. datetime
5. mimetypes

This repo contains how to extract emails from given gmail by providing username and password. Now this script extracts mail from gmail server but you can generalize this script by looking at other mail server that imap provides by visiting https://www.systoolsgroup.com/imap/.

Make sure to check https://myaccount.google.com/lesssecureapps?pli=1.

I have introduced 4 filters namely:
1. getInfoAll - this will save all the information from the specified folder ('inbox' in our case).
2. getInfoDate - this will save all the information from the specified folder ('inbox' in our case) from the date that we specify.
3. getInfoFrom - this will save all the information from the specified folder ('inbox' in our case) from the sender gmail that we specify.
4. getInfoDateSender - this will save all the information from the specified folder ('inbox' in our case) from the sender gmail and date we specify.

Here we have used imap to retrieve information from mail server.
content_disposition helps us to decide whether mail has any attachment attached with it.
 content_type is used to know content type of the mail.
 In order to understand this I highly recommend to open a mail with some attachment with it in "show original option" in gmail.
 os.getcwd() is used to return current working directory or you can specify specific directory of your choice.
I am creating "exceed+counter" as name of directory if length subject length is more than 30, you can go with any other method.
I have defined "textfile.txt" for all mails to download other information about mail. In each text file i am saving following information - [to, from, date, subject, body]. You can add more info according to your requirements.
 #NOTE: while using subject name of the mail as directory to download the information be sure to check the length of the path since windows has some limit on the path length.
 
 #Be sure to check encoding type that your system support and modify that accordingly.
 
 #UPDATE: We can also permit only some specific file formats to download by using mimetype module. Here i have allowed only pdf, jpg, png and doc file. We can modify according to your own requirement.

Feel free to suggest improvements and ask queries by making a pull request.
