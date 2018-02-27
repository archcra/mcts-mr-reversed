# mcts-mr-reversed
MonteCarlo Tree Search with Map Reduced reversed version


Inspired by this project: https://github.com/rubenfonseca/map_crowd_reduce, and based on this MCTS project: https://github.com/OMerkel/UCThello. 

This is a Node.js Express App. Reverse version means that all the map functions are distributed to the clients: browser clients. And with socket.io, sets up the real-time communication between clients and server. Instead of put the reduce function on the clients as the rubenfonseca project does, I plan to put the reduce function on the server.

The MCTS real tree will be put on the server, and sync to each client with socket.io. The sync will be carried after some batch of interations(trials). The imaginary tree, used by the simulation step of MCTS, will be used on the clients.


As an example, Finding-Change will be the first task, which described as follows:
There are many cash with denomination of only these three kind: 1,9,10; To change the money of sum N, what is the strategy to get the changes cash most less?
For example: to change money with N=2, the change will be 1,1;
to change money with N=9, the change will be one 9, not nine 1s.
to change money with N=18, the change will be double 9s, not 10, 1,1,1,1,1,1,1,1. Got it?

The following is the Chinese version:
已知需要找给顾客的零钱金额为N，当前钱币的面值种类为1,9,10三种，求找给顾客尽量少的钱币数的找零方法。给出程序算法设计思路。

