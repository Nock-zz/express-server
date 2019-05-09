## Express Server

See https://hackernoon.com/set-up-ssl-in-nodejs-and-express-using-openssl-f2529eab5bb f.or fuller information

### Setup Steps
Install express with npm i express.

Set up server.js --- see server.js file for information
create the https certificate openssl exception with the command line:

    openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 3650

Create the .p12 certificate file with the following command:

    openssl pkcs12 -export -out cert.p12 -inkey key.pem -in cert.pem

### Update Chrome/Brave certificate exceptions
Import the .p12 file under Edit > Preferences --> Manage certificates --> Your certificates import
add the cert.p12 and enter the password.
