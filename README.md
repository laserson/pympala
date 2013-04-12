pympala
=======

Python client to Cloudera Impala


Installation
------------

Uses setuptools/distribute.

Requires `thrift>=0.9`.

Currently:

    git clone git://github.com/laserson/pympala.git
    cd pympala
    python setup.py install

Eventually:

    pip install pympala


Usage
-----

    import impala
    client = impala.ImpalaBeeswaxClient('host:port')
    client.connect()
    results = client.execute(query)

Note that `query` gets parsed by `impalad`, not the `impala-shell`, so do not do
things like add semicolons to the end of the query.
