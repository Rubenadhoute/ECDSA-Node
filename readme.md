## ECDSA Node

Using a client and server to facilitate transfers between different addresses. Since there is just a single server on the back-end handling transfers, this is clearly very centralized.

I am interested in implementing Public Key Cryptography. By using Elliptic Curve Digital Signatures we can make it so the server only allows transfers that have been signed for by the person who owns the associated address.
 
### Key Learnings

- Public Key Cryptography

- Ethereum Cryptography library 


### Step to reproduce

1. Follow instructions below for initial setup

2. Check that balance is initialized for each private key via UI 

3. Run hash_and_sign script on a separate command

4. Enter transaction data into UI and try to transact via server

5. The server will recover the public key from the transaction signature and allow the transaction if it matches the original public key associated with it.




### Initial setup

#### Client

The client folder contains a [react app](https://reactjs.org/) using [vite](https://vitejs.dev/). To get started, follow these steps:

1. Open up a terminal in the `/client` folder
2. Run `npm install` to install all the depedencies
3. Run `npm run dev` to start the application 
4. Now you should be able to visit the app at http://127.0.0.1:5173/

#### Server

The server folder contains a node.js server using [express](https://expressjs.com/). To run the server, follow these steps:

1. Open a terminal within the `/server` folder 
2. Run `npm install` to install all the depedencies 
3. Run `node index` to start the server 
