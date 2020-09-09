The sixth Step
Clone Blockchain NETWORK file and run the First-network 

## Task

1. Clone the basic Network`git clone https://github.com/adhavpavan/BasicNetwork-2.0.git`{{execute}}

2. Go to tab IDE and viewing files in direcrtory "BasicNetwork-2.0"

3. back to terminal Generate Crypto artifactes for organizations by using command below
   `cd BasicNetwork-2.0/artifacts/channel`{{execute}}

4. Edit file create-artifacts.sh by copy code below:
   ```
   # chmod -R 0755 ./crypto-config
   # Delete existing artifacts
   # rm -rf ./crypto-config
   # rm genesis.block mychannel.tx
   # rm -rf ../../channel-artifacts/*

   #Generate Crypto artifactes for organizations
   cryptogen generate --config=./crypto-config.yaml --output=./crypto-config/



   # System channel
   # SYS_CHANNEL="sys-channel"

   # channel name defaults to "mychannel"
   # CHANNEL_NAME="mychannel"

   # echo $CHANNEL_NAME

   # # Generate System Genesis block
   # configtxgen -profile OrdererGenesis -configPath . -channelID $SYS_CHANNEL  -outputBlock ./genesis.block


   # Generate channel configuration block
   # configtxgen -profile BasicChannel -configPath . -outputCreateChannelTx ./mychannel.tx -channelID $CHANNEL_NAME

   # echo "#######    Generating anchor peer update for Org1MSP  ##########"
   # configtxgen -profile BasicChannel -configPath . -outputAnchorPeersUpdate ./Org1MSPanchors.tx -channelID $CHANNEL_NAME -asOrg Org1MSP

   # echo "#######    Generating anchor peer update for Org2MSP  ##########"
   # configtxgen -profile BasicChannel -configPath . -outputAnchorPeersUpdate ./Org2MSPanchors.tx -channelID $CHANNEL_NAME -asOrg Org2MSP
   ``` {{copy}}