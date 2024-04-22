**Pre-requisites:**
Install JDK-8
 sudo apt-get remove openjdk*
 sudo apt update
 sudo apt install openjdk-8-jdk openjdk-8-jre


**ASSIGN_1**
Terminal 1
javac Client/*.java  && javac Server/*.java
rmiregistry 5000

Terminal 2
java Server.ServerMain

Terminal 3
Java Client.ClientMain

****Assign_2 (Calculator)****
### Terminal 1
idlj -fall Calc.idl
(if issue occured try this command )
sudo apt install openjdk-8-jdk-headless
sudo apt update

### Terminal 2
javac CalcApp/*.java CalcApp/CalcPackage/*.java CalcClient.java CalcServer.java
orbd -ORBInitialPort 1050 -ORBInitialHost localhost &

### Terminal 3
java -cp .:target/dependency/* CalcServer -ORBInitialPort 1050 -ORBInitialHost localhost

### Terminal 4
java -cp .:target/dependency/* CalcClient -ORBInitialPort 1050 -ORBInitialHost localhost

**ASSIGN_2 (Reverse string)**
###Terminal 1:
idlj -fall ReverseModule.idl
javac *.java ReverseModule/*.java
orbd -ORBInitialPort 1056&
java ReverseServer -ORBInitialPort 1056&

###Terminal 2:
java ReverseClient -ORBInitialPort 1056 -ORBInitialHost localhost

**ASSIGN_3**
Download MPJ from here
https://sourceforge.net/projects/mpjexpress/files/releases/mpj-v0_44.tar.gz/download

export MPJ_HOME=(Copy path from bin of extracted mpj directory)
javac -cp $MPJ_HOME/lib/mpj.jar ArrSum.java
$MPJ_HOME/bin/mpjrun.sh -np 4 ArrSum

**Assignment_3 (Classroom)**
sudo apt update
sudo apt install python3-pip
sudo apt-get install mpich  # for MPICH
pip install mpi4py --upgrade
python3 filename.py

**ASSIGN_4:**
###Terminal 1: (first run this)
python3 server.py

###Terminal 2: (then run this)
python3 client.py

ASSIGN_4 (classroom)
1. sudo apt install openjdk-11-jre-headless
2. java assignment4.java

**ASSIGN_5:**
javac Tring.java
java Tring

**ASSIGN_6:**
javac Bully.java
java Bully

javac Ring.java
java Ring

**ASSIGN_7: **
Step 1: pip install flask
Step 2(terminal 1): python3 app.py
Step 3(terminal 2): python3 distributed_app.py
Step 4: Open  http://localhost:5000/hello for output.

**ASSIGN_9 (Content Beyond Syllabus):**
###Terminal 1:
javac *.java
java Server

###Terminal 2:
java Client
