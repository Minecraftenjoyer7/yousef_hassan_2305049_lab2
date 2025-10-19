-- How to set up and run the project locally:
  i copied the files sent on teams and run {npm i} to download all needed packages. then i ran nodemon vun-server.js and the server ran locally 
  
-- How to populate .env from .env.example:
  cp use.env .env
  (did the .env since this is my file name)

-- Exact steps to reproduce the vulnerable demo and the hardened demo:
  i created a GET request in postman that sends request to http://localhost:1234/admin with the authorization of bearer token
  and depending on the token i sniffed or generated from the bruteforce as seen in the video i added it to the baerer 

-- How to capture traffic with Wireshark:
  since i am running on localhost so i sniffed traffic going through the loopback interface. and then since i only needed the http traffic i filtered by http

-- Notes on assumptions and limitations:
1) Assumptions
       this guide assumes you run everything on your own computer or a lab vm and that you control the node process and the database
       it assumes users db already has a user you can login with and that you can change server files and restart it when needed
       also it expects you have node and sqlite3 installed and some basic comfort with the command line

2) Limitations
      all the tests here are only local. real production setups are way more complicated (https, load balancers, key rotation, lots of microservices, ....)
      the forging or bruteforce demos are just for learning and small scale only they don’t show how to do large automated attacks 
