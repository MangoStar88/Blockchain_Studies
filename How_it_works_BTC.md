## How it works - Bitcoin

### How a transaction be sent
Before to understanding how bitcoin is and how it works
Let's review how will you do if you want to send amount of money to someone?
first, you need to tell a banker you want to create a bank account for your own
second,The bank will depand you demand, to make the transaction be done
third,you need to confirm the money already send to the one you made transaction, there always the bank will give you a feedback.
Of course, there are a lot of complicated operations involved, including making sure you have enough money in your own account 
and how the bank keeps your money safe. Let's ignore that because everyone is familiar with how to do transactions in a bank.
Do you find something? The process may be conclued as three steps.
Create & Make Transaction & Confirm

### How to make a bitcoin transaction
OK. Let's start from how to make a transaction by using bitcoin
then I will introduce you other things about btc
First,Create
How to create your bitcoin account?
Remember, you are in a decentralised world now
No one will help you to do these
You need all by yourself
OK. How will you suppose to do?
It's quite easy
just to finding a coin and toss it for 256 times and record them as 1 or 0
ok, you have the binary digits of random privatekey
you can use it in a bitcoin wallet
or you also can use your computer to generate the publickey and address next
all you need to know is what the mathmatical fomular it is 
when you have the privatekey for your own
To using the Elliptical Curve Digital Signature Algorithm to generate the publickey
The public key is used to receive funds, and the private key is used to sign transactions to spend the funds
then the public key is used the hashing function to generate address
Ok, now, you have privatekey and publickey and address, which means you created an account of bitcoin
Next, you want to make a transaction to someone
how?
Let' continue.
you may got an address from someone
cause you already know how to create an account
maybe you can teach others to generate their own
then you need somewhere there can type the address in
where?
a wallet
you need to download a version of wallet on bitcoin offical website
then you can type person's address and send it
Third,Confirm the transaction
Not liking the centralized bank will give a feedback to you
All the transaction is packaged by miners
The common consensus is after 6 blocks or 60 minutes
you payment will be satefy send to the receiver
and you can put you transaction ID on the bitcoin explorer to check the status

### How it works
I will make a simple introduction here. 
If you wanna know more about it I recommanded you to read the whitepaper.(search it on google or find it
in my repository>Blockchain_Studies/Study_Materials)
A person named satoshi nakamoto published a whitepaper named 'bitcoin:a peer to peer network electronic cash system' in 2008, when Lehman bankrupted.
In this whitepaper, satoshi provided a solution for decentralize tradement.
There are three roles in this system.
Payer, receiver and miner.
payer for generate a payment or create a transaction.
receiver for receive the payment or transaction.
miner for package the payment and boardcast to the whole peers.
Payer and Receiver is not difficult to understand.
Let's explain more for the miner and how a tansaction is sent successfully.
Now, imagines you are a coin, the payer wanna send you to the receiver.
1st,when the payment is been created, you will be boardcast to the network
which means, all nodes knows you want to go to the receiver's address
there,each nodes collects transactions to a block.
you will be packaged to a block by a miner
then, you will see the miner is to finding a random number(nounce) for this block.
then, after 10 minutes you miner failed. the other miner find this.
but he is not easy to quit. he continue to finding the random number.
after another 10 minutes, he win!
the block you are in, is boardcasting to the whole network.
then, other miners will put their blocks behind you
you will see this chain become longer and longer
and after 60 minutes, the receiver checked your block transactions on the explorer
and you are his officially.
that's how it actually works in a simple example.

### What the techbologies behind the transaction
- SHA-256 

 Secure Hashing Algorithm,is the hash function and mining algorithm of the Bitcoin protocol
 
- ECDSA

Elliptical Curve Digital Signature Algorithm, it is for privatekey to generate a publickey, the algorithm is a one-way process,
which means you cannot use it convert publickey to privatekey. it is irreversible

- K=k*G

it is the formula for publickey generating.K is the resulting publickey, k is stand for privatekey,
G is a constant point called the generator point

- RIPEMD

the RACE Integrity Primitives Evaluation Message Digest, A Bitcoin address is a rip160 hash of a sha256 hash of the public key

- A=RIPEMD160(SHA256(K))

it is the formula for generating an address.
where K is the public key and A is the resulting bitcoin address.
Bitcoin addresses are derived from a public key using a one-way function.

- Base58Check

Bitcoin addresses are almost always encoded as “Base58Check” 
which uses 58 characters (a Base58 number system) and a checksum to help human readability, avoid ambiguity, 
and protect against errors in address transcription and entry. 
Base58Check is also used in many other ways in bitcoin, whenever there is a need for a user to read and correctly transcribe a number, 
such as a bitcoin address, a private key, an encrypted key, or a script hash. 
In the next section we will examine the mechanics of Base58Check encoding and decoding and the resulting representations. 


