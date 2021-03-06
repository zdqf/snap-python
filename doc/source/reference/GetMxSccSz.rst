GetMxSccSz
''''''''''

.. function:: GetMxSccSz()

A graph method that returns the fraction of nodes in the largest strongly connected component of a graph.

Parameters:

- None
 
Return value:

- float
     The fraction of nodes in the largest strongly connected component of a graph.


The following code shows how to calculate the relative size of the maximum strongly connected component for nodes in
:class:`TNGraph`, :class:`TUNGraph`, and :class:`TNEANet`::

  import snap

  Graph = snap.GenRndGnm(snap.TNGraph, 20, 10)
  print('Relative size of SCC in Directed Graph:', Graph.GetMxSccSz())

  UGraph = snap.GenRndGnm(snap.TUNGraph, 20, 10)
  print('Relative size of Size SCC in Undirected Graph:', UGraph.GetMxSccSz())

  Network = snap.GenRndGnm(snap.TNEANet, 20, 10)
  print('Relative size of SCC in Network:', Network.GetMxSccSz())

