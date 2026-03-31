# Inconveniences

## Description
This is a page where i list all the inconveniences i encounter during this project, so i can journal them and how i overcame them. It seemed like a smart thing to do but it's kind of experimental now (i don't even know if this is the right place to keep the file).

### Inconvenience 1: Failed connection between web server and database server
- **Issue**: After setting up the web server and database server, I couldn't connect to the database from the web server.I suggested that the issue might stem from NAcLs or the security group rules.
- **Cause**: An outbound rule was missing in the public subnet's NACL, which was blocking the traffic from the web server to the database server.
- **Solution**: I added the rule 90 to allow outbound traffic to private subnet
- **Lesson**: Traffic must be allowed in both directions for communication to work.