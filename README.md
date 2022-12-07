# DevOps-Assignment-Answer
 
Question 2) Write a one liner to get the list of users in the alphabetical order from the /etc/passwd file whose UID is greater than 100.
  * View users alphabetically
  * cut -d: -f1  /etc/passwd | sort
                
Question 3) How to check cron job particular user.
  * crontab -u username -l
        or
  * crontab -ul <username<username>>

Question 4) How to fix  if $PATH is lost, and its output is blank?

  * The default path is
  * /home/_username_/bin:/usr/local/bin:/usr/bin:/bin:/usr/bin/X11:/usr/games 

Question 5) Write a single  dockerfile to get below outputs when I run the corresponding docker run commands:
  A. command : docker run -it <image>
      Output: Hello world
  B. Command: docker run -it <image> John
     Output: Hello John
     
  Create a Dockerfile
  1. we will create a directory named MyDockerImages with the command:
  * mkdir MyDockerImages
  2. Move into that directory and create a new empty file (Dockerfile) in it by typing:
  * cd MyDockerImages
  * touch Dockerfile
  3. we opened the file using Nano:
  * nano Dockerfile
  4. Then, add the following content:
  * FROM ubuntu
  *  MAINTAINER sofija
  * RUN apt-get update
  * CMD ["echo", "Hello World"]
  5. we can check the content of the file by using the cat command:
  * cat Dockerfile
  
Question 7) Write a command to delete 10 days older log files
 * find /path/to/files* -mtime +10 -exec rm {} \\;
