GetEdgesInOut
'''''''''''''

.. function:: GetEdgesInOut (NIdV)

A graph method that returns the number of reciprocal edges between the nodes in *NIdV* and the number of edges between the nodes in *NIdV* and the rest of the graph.

Parameters:

- *NIdV*: Python list or :class:`TIntV`, a vector of ints
    A vector of node ids.

Return value:

- list: [ int, int ]
    The list contains two elements: the first element gives the number of reciprocal edges between the nodes in *NIdV*, and the second element gives the number of edges between the nodes in *NIdV* and the rest of the graph.

The following example shows how to use :func:`GetEdgesInOut` with
:class:`TNGraph`, :class:`TUNGraph`, and :class:`TNEANet`::

    import snap

    Nodes = []
    for nodeId in range(10):
        Nodes.append(nodeId)

    Graph = snap.GenRndGnm(snap.TNGraph, 100, 1000)
    results = Graph.GetEdgesInOut(Nodes)
    print("EdgesIn: %s EdgesOut: %s" % (results[0], results[1]))

    UGraph = snap.GenRndGnm(snap.TUNGraph, 100, 1000)
    results = UGraph.GetEdgesInOut(Nodes)
    print("EdgesIn: %s EdgesOut: %s" % (results[0], results[1]))

    Network = snap.GenRndGnm(snap.TNEANet, 100, 1000)
    results = Network.GetEdgesInOut(Nodes)
    print("EdgesIn: %s EdgesOut: %s" % (results[0], results[1]))

