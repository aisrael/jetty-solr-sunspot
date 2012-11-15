This repository packages a ready to run solr server with standard example schema distributed with Solr.
It uses jetty 8 server forthe application container.

To start the Solr server, just run

    bin/jetty.sh run

That same script can be copied to /etc/init.d (on Red Hat/CentOS) as a service script

    cp bin/jetty.sh /etc/init.d/jetty
    service jetty start|stop|check

To configure Jetty options, the easiest is to create /etc/default/jetty. For example:

    JETTY_HOME=/opt/local/jetty
    JETTY_PORT=8983
    JETTY_LOGS=/var/log/jetty

To load some data into the index:

    cd exampledocs
    ./post.sh *.xml

Packaged Versions:
Solr : 3.6.1
Jetty: 8.1.7.v20120910
