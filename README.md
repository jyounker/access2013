access2013
==========

Access 2013 How-To

As per Access 2013 [Presentation][9]


1.  Download and install [CouchDB][1]

2.  Download and install [ElasticSearch][2]

3.  [You have Python, right?]  Download and install Python's [pymarc][8],
    [couchdb][7]

4.  Get some MARC Records (use your own, or get some [here][3])

5.  Download [marc2couchdb.py script][4] [you have Python, right?]

    1.  Make sure CoucbDB is running

    2.  Create a database in CouchDB

    3.  Modify script to point to your MARC file and to your CouchDB db

    4.  Run 'python marc2couchdb.py'

    5.  Wait a longish time

6.  Download [configure_elastic.sh][5] script

    1.  Make sure elasticsearch is running (tip:  run 'bin/elasticsearch -f'
        wherever you put the elasticsearch dir)

    2.  Uncomment the second line of configure_elastic.sh if this is the first
        time running the script

    3.  run './configure_elastic.sh'

    4.  This'll take a while, but you can hit it with facetview (below) while it
        indexes

7.  Download [facetview][6]

    1.  Modify index.html or simple.html to point to your instance of
        ElasticSearch (most likely
        'http://localhost:9200/your_dbname_here/_search?')

8.  Navigate to your facetview/index.html or facetview/simple.html file (no
    webserver needed)

[1]: <https://couchdb.apache.org/>

[2]: <http://www.elasticsearch.org/download/>

[3]: <https://archive.org/details/ol_data>

[4]: <https://github.com/jyounker/dcat/blob/master/import/marc2couchdb.py>

[5]: <https://github.com/jyounker/dcat/blob/master/configure_elastic.sh>

[6]: <https://github.com/jyounker/facetview>

[7]: <https://pypi.python.org/pypi/CouchDB>

[8]: <https://pypi.python.org/pypi/pymarc>

[9]: <https://rawgithub.com/jyounker/reveal.js/master/index.html>
