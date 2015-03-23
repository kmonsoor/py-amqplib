Implements a simple non-threaded Python client library for AMQP 0-8, tested with [RabbitMQ](http://www.rabbitmq.com/).

The initial need was for something that could be used in an embedded Python environment, in which case reliance on threading would probably cause trouble.  A quick connection time was desirable too.  [QPID](http://cwiki.apache.org/qpid/) takes a while to parse the AMQP spec file, but this module relies on a skeleton generated statically from the 0-8 spec file and fleshed it out by hand.

Also features SSL support (tested against RabbitMQ behind a Stunnel), Python 3.x compatibility (via 2to3 being invoked automatically by setup.py), and IPv6 support

If you need something that can better handle asynchronous messaging, [txAMQP](http://launchpad.net/txamqp) for Twisted Python, [Pika](https://github.com/pika), or [Haigha](https://github.com/agoragames/haigha) may be what you're looking for.  The Celery Project has a [fork](http://amqp.readthedocs.org/) of py-amqplib they're maintaining with some nice improvements.

Check out [Rabbits and Warrens](http://blogs.digitar.com/jjww/2009/01/rabbits-and-warrens/) for a nice writeup of AMQP that uses amqplib for the examples.

Packaged on
  * [Debian](http://packages.debian.org/search?keywords=amqplib)
  * [FreeBSD](http://www.freshports.org/net/py-amqplib/)
  * [RepoForge](https://github.com/repoforge/rpms/tree/master/specs/python-amqplib)
  * [Ubuntu](http://packages.ubuntu.com/search?suite=all&searchon=names&keywords=amqplib)