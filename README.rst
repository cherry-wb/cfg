Control Flow Graph
------------------

Spurred by a `StackOverflow question`_, I decided to write something that 
would attempt to generate a Control Flow Graph without creating visuals. This 
will simply return an object which you can traverse.

I'm still deciding on the API. So far I'm thinking

::

    from cfg import parse

    graph = parse(file='filename.py')

    graph.walk('path')  # returns an iterator for one path

Or more succinctly

::

    from cfg import walk

    walk(file='filename.py', path='path')  # returns an iterator like above


.. links
.. _StackOverflow question:
    http://stackoverflow.com/questions/14226773/compute-ingestible-control-flow-graph-from-source-code
