# peatio-dogecoin
clone peatio

go into the folder /lib/peatio

create a folder named dogecoin

upload the files blockchain.rb / client.rb / wallet.rb

go in the folder /peatio/config/initializers

open the file blockchain_api.rb

and paste this   

***** Starting from version 2.4 you must delete .new so will be Dogecoin::Blockchain and Dogecoin::Wallet ********

Peatio::Blockchain.registry[:dogecoin] = Dogecoin::Blockchain.new

save and exit

open the file wallet_api.rb in the same folder and paste this

Peatio::Wallet.registry[:dogecoind] = Dogecoin::Wallet.new

save and exit

now you have dogecoin ready to be added to tower

clone your new image of peatio

docker build -t peatio:custom image

change peatio image in /opendax/config/app.yml

rake render:config && rake service:app

Donate

btc : 1HMxPrWjYc7mtT5ajrSTkem2YUKcHDrbcM

eth : 0x90009fe658A99E8289C0EB1cCB5290E2b6C6DB9e

doge : DSCRUbhDeg2gxgFdhz4zgfYWLyYuB79KZ3


thats all,tested and working for v2.3 and 2.4 of openware
