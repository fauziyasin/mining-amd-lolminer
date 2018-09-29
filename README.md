# AMD Mining using lolMiner
lolMiner is a multi algorithm Equihash miner with focus on AMD GPUs (OpenCL based). Nvidia cards are also supported, however it is advised to use lolMiner with AMDs only. We did not create lolMiner, credit should be given to Lolliedieb on Bitcoin Talk Forum. The full ongoing discussion on LolMiner, including support help can be found on the [lolMiner original bitcoin talk post](https://bitcointalk.org/index.php?topic=4724735.0).

The following will walk you through how to setup lolMiner on Ubuntu 18.04 systems.

## Prerequisites

Your system should have the appropriate AMD drivers for your card. Not sure if you have the right drivers? Please refer to the [AMD driver site](https://www.amd.com/en/support), to locate your driver.

It is also assumed that you are running Ubuntu 18.04. While this is not a requirement to run lolMiner, the steps on this tutorial were done on this version of Linux. Please feel free to run lolMiner on the version of linux that you are currently running and let us know if you experience any issues. 

## Installing lolMiner

Start by downloading the latest release of lolMiner under the release tab of this github.

Depending on your operating system, choose the correct build

Decompress the the bundled file to reveal the folder inside

The binary for lolMiner can be found inside the folder. 


## Configuring lolMiner

lolMiner works by referencing profiles that have been added to the user_config.json file. To mine on a bithereum pool, update the parameters to the correct pool details. 

For example, if you would like to mine on bithereum testnet, update the parameters to the following (replace YOUR_BITHEREUM_ADDRESS with the bithereum address you would like to receive your mining rewards).

```JSON
	"BTH" :
	{
		"COIN" : "BTH",
		"POOLS" : [
			{
		 	  "POOL" : "testnet-pool.bithereum.network",
		 	  "PORT" : "3333",
		 	  "USER" : "YOUR_BITHEREUM_ADDRESS.lolMiner",
		 	  "PASS" : "x"
		  }
	  ]
	}
```

## Running lolMiner 

The run_miner_with_restart.sh and run_miner.sh are both used to start lolMiner. Crack open either file and make sure that what follows PROFILE= matches the profile within the user_config.json file that you would like to use. 

Make sure that run_miner_with_restart.sh or run_miner.sh are executable. You can make them excuable by running 
```shell
$ chmod +x run_miner.sh
$ chmod +x run_miner_with_restart.sh
```
