RPC simple example

developer@ubuntu:~/temp/rpc$ rpcgen rpcprog.x -a
developer@ubuntu:~/temp/rpc$ ls
Makefile.rpcprog  rpcprog_client.c  rpcprog_clnt.c  rpcprog.h  rpcprog_server.c  rpcprog_svc.c  rpcprog.x
developer@ubuntu:~/temp/rpc$ make -f Makefile.rpcprog
cc -g    -c -o rpcprog_clnt.o rpcprog_clnt.c
cc -g    -c -o rpcprog_client.o rpcprog_client.c
cc -g     -o rpcprog_client  rpcprog_clnt.o rpcprog_client.o -lnsl
cc -g    -c -o rpcprog_svc.o rpcprog_svc.c
cc -g    -c -o rpcprog_server.o rpcprog_server.c
cc -g     -o rpcprog_server  rpcprog_svc.o rpcprog_server.o -lnsl
developer@ubuntu:~/temp/rpc$ ls
Makefile.rpcprog  rpcprog_client.c  rpcprog_clnt.c  rpcprog.h       rpcprog_server.c  rpcprog_svc.c  rpcprog.x
rpcprog_client    rpcprog_client.o  rpcprog_clnt.o  rpcprog_server  rpcprog_server.o  rpcprog_svc.o
developer@ubuntu:~/temp/rpc$
