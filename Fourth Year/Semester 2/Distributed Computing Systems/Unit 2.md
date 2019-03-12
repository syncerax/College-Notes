# Distributed Computing Systems

## Unit 2: Communication and Coordination

### Remote Procedure Call

- **In a nutshell**, the idea is to allow programs to call procedures that are stored on different machines.
- When a process on **machine A** calls a procedure located on **machine B**, the process on machine A is blocked and the procedure is executed on machine B.
- Information can be transported from the caller to the callee in the form of **parameters** and can come back in the form of the **return value** of the procedure.
- **No message passing is visible** to the programmer.
- A **remote procedure call should** look as much as possible as a local one. In other words, we want the RPC to **be transparent** - the calling procedure should not be aware that the called procedure is executing on a different machine.

#### Basic RPC Operation

1. The client process calls the client stub in the normal way.
2. The client stub creates a message with the parameters and calls the local OS.
3. The local OS sends the message to the remote OS.
4. The remote OS gives the message to the server stub.
5. The server stub unpacks the message and calls the remote procedure.
6. The remote procedure returns results to the server stub.
7. The server stub packs the result in a message and calls the remote OS.
8. The remote OS sends the message to the local OS.
9. The local OS gives the message to the client stub.
10. The client stub unpacks the message and returns the result to the client process.

### Network Virtualization - Overlay Networks

- A growing range of applications co-exist in the Internet, like video streaming applications, gaming applications, social media platforms.
- It would be impractical to redefine the Internet communication protocols for each different type of application.
- This has led to an interest in Network Virtualization.
- Network Virtualization deals with the construction of many different application-specific virtual networks over an existing network (like the Internet) without changing the characteristics of the existing underlying network.
- Just like computer networks have addressing schemes, protocols and routing algorithms, virtual networks can have addressing schemes, routing algorithms and protocols, but redefined to suit the needs of the application.