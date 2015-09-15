# MinecraftPlusProtocol

####What is plus protocol?
It is additional way for communicate ( client <-> server or client <-> proxy <-> server)

####How it works?
The most important thing is the client (or proxy) has to send "+" at end of host field in [Handshake](http://wiki.vg/Protocol#Handshake) packet.

#####What next?
Server without plus protocol:
* If server doesn't support plus protocol nothing will happen.

Server with plus protocol:
 * Server knows that he can send custom packets to client.
 * Wait for player Login packet
 * Response with special packet (someting like IHasPlusProtocolToo, it could contains some data about the server)
 * Now both sides know about the plus protocol

I think one addional packet like [Plugin_Message](http://wiki.vg/Protocol#Plugin_Message) could be enought for all things :relaxed: (May only increase max size of packet)

Any question or suggestion?
Just create an issue :wink:
