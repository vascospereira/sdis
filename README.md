# README #

## To COMPILE in UNIX: ##

 * using a terminal, navigate to the project's root folder (SDIS-01)	
 * cd to "scripts" subfolder and enter "chmod 755 compile.sh"	
 * followed by "./compile.sh"

## To COMPILE in WINDOWS: ##

 * through Command Prompt, navigate to root project Folder (SDIS-01)	
 * cd to "scripts" subfolder and enter "Compile.bat"	

## To START a Peer in UNIX: ##

 * navigate to the project's "src" folder (SDIS-01/src)
 * through the terminal type: "rmiregistry &" to start the RMI registry process
 * in the same terminal, or other pointing to the same directory, type:	
		"java Peer.Peer <protocolVersion> <serverID> <accessPoint> <MC>:<MCPort> <MCB>:<MCBPort> <MCR>:<MCRestore>"
	example: java Peer.Peer 1.0 1 remote 224.0.0.3:3333 224.0.0.3:4444 224.0.0.3:5555

## To START a Peer in WINDOWS: ##

 * open Comand Prompt, navigate to project's "src" folder (SDIS-01\src)
 * enter "start rmiregistry" to start the RMI registry process
 * in the same Command Prompt, or other pointing to the same directory, type:	
		"java Peer.Peer <protocolVersion> <serverID> <accessPoint> <MC>:<MCPort> <MCB>:<MCBPort> <MCR>:<MCRestore>"
	example: java Peer.Peer 1.0 1 remote 224.0.0.3:3333 224.0.0.3:4444 224.0.0.3:5555

## To RUN the TestApp in UNIX: ##

 * navigate to the project's "src" folder (SDIS-01/src)
 * through the terminal type:
		"java TestApp <peer_access_point> BACKUP <filepath> <replication_degree>" or
		"java TestApp <peer_access_point> RESTORE <filepath>" or
		"java TestApp <peer_access_point> DELETE <filepath>" or
		"java TestApp <peer_access_point> RECLAIM <space>" or
		"java TestApp <peer_access_point> STATE" 
	backup example: java TestApp remote backup ../testfiles/nature.jpg 1
    
## To RUN the TestApp in WINDOWS: ##

 * open Comand Prompt, navigate to project's "src" folder (SDIS-01\src)
 * through the Comand Prompt type:
		"java TestApp <peer_access_point> BACKUP <filepath> <replication_degree>" or
		"java TestApp <peer_access_point> RESTORE <filepath>" or
		"java TestApp <peer_access_point> DELETE <filepath>" or
		"java TestApp <peer_access_point> RECLAIM <space>" or
		"java TestApp <peer_access_point> STATE" 
	backup example: java TestApp remote backup ..\testfiles\nature.jpg 1

## DESCRIPTION of local files created by the peer application: ##

	In "servers" folder (SDIS-01 -> servers), each peer createas a new folder, which the name is the Peer own identifier, creates also a:
 * BACKUP folder: Saves every backup initiated by other peers.
 * LOCAL folder: Saves every information related to local initiated backups.
 * RESTORE folder: Saves every restored file.
