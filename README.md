# File_Sharing_with_XML-RPC
A peer-to-peer file-sharing program that uses XML_RPC.

# What it does:
• Each node must keep track of a set of known nodes, from which it can ask for help.
It must be possible for a node to introduce itself to another node (and thereby be
included in this set).<p>

• Asks a node for a file (by supplying a file name). If the node has
the file in question, it should return it; otherwise, it should ask each of its neighbors
in turn for the same file (and they, in turn, may ask their neighbors). If one of these
nodes has the file, it is returned.<p>

• To avoid loops (A asking B, which in turn asks A) and to avoid overly long chains of
neighbors asking neighbors (A asking B asking C . . . asking Z), it must be possible
to supply a history when querying a node. This history is just a list of which nodes
have participated in the query up until this point. By not asking nodes already in the
history, you avoid loops, and by limiting the length of the history, you avoid overly
long query chains.<p>

• There must be some way of connecting to a node and identifying yourself as a
trusted party. By doing so, you should be given access to functionality that is not
available to untrusted parties (such as other nodes in the peer-to-peer network).
This functionality may include asking the node to download and store a file from the
other peers in the network (through a query).<p>

• Has a user interface that lets you connect to a node (as a trusted
party) and make it download files. It should be easy to extend and, for that matter,
replace this interface.<p>
  
# What i learned:
• xmlrpc.client module
• xmlrpc.server module
• threading module,
• urllib.parse module.


