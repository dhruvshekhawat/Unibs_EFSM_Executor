# Unibs_ns3_modified-files

Follow the steps given below in order to complete the executor implementation in ns-3.

1. Perform all the steps given on http://ns3help.blogspot.it/2014/05/installing-ns3-in-ubuntu-1210.html 
to install ns-3.19.
2. After properly installing ns-3.19, replace the following files from your ns-3 package with the files given in this repository-
- tcp-socket-base.h (in ns-allinone-3.19/ns-3.19/build/ns3 and ns-allinone-3.19/ns-3.19/src/internet/model)
- tcp-socket-base.cc (in ns-allinone-3.19/ns-3.19/src/internet/model)
- tcp-l4-protocol.h (in ns-allinone-3.19/ns-3.19/build/ns3 and ns-allinone-3.19/ns-3.19/src/internet/model)
- tcp-l4-protocol.cc (in ns-allinone-3.19/ns-3.19/src/internet/model)
- tcp-tahoe.h (in ns-allinone-3.19/ns-3.19/build/ns3 and ns-allinone-3.19/ns-3.19/src/internet/model)
- tcp-tahoe.cc (in ns-allinone-3.19/ns-3.19/src/internet/model)
- tcp-socket.h (in ns-allinone-3.19/ns-3.19/build/ns3 and ns-allinone-3.19/ns-3.19/src/internet/model)
- tcp-socket.cc (in ns-allinone-3.19/ns-3.19/src/internet/model)
- ns3module.h (in ns-allinone-3.19/ns-3.19/build/src/internet/bindings)
- ns3module.cc (in ns-allinone-3.19/ns-3.19/build/src/internet/bindings)
3. After having replaced these files, copy the sequence-number.h file (from ns-allinone-3.19/ns-3.19/build/ns3) into the ns-allinone-3.19/ns-3.19/src/internet/model directory.
4. Add the state-machine-var.h file in ns-allinone-3.19/ns-3.19/build/ns3 and ns-allinone-3.19/ns-3.19/src/internet/model.
5. Copy the libxml folder into the ns-allinone-3.19/ns-3.19/build directory.
6. Copy the fifth.cc file into the scratch folder.
7. Wherever you place your state_machine and cwnd_evolution XML files, change the path location (to find and parse them) accordingly in the tcp-l4-protocol.cc
and the tcp-tahoe.cc files. 
8. ./waf
9. If ns-3 builds successfully, it is done.
