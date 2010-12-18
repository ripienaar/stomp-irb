What is it?
===========

An Interactive Ruby shell for STOMP

How to use it?
==============

Start it supplying user, password, stomp host and port - see the <em>--help</em> information for details.

<pre>
$ stomp-irb -s stomp --port 6163
Interactive Ruby shell for STOMP

Type 'help' for usage instructions

>> subscribe :topic, "foo.bar"
Current Subscriptions:
    /topic/foo.bar

=> nil
>> topic "foo.bar", "hello"
=> nil
&lt;&lt;stomp&gt;&gt; hello

>> recv_callback {|f| puts "Received: #{f.body} from #{f.headers["destination"]}"}
>> topic "foo.bar", "hello"
=> nil
&lt;&lt;stomp&gt;&gt hello
Received: hello from /topic/foo.bar
</pre>

License?
========

Apache 2.0

Contact?
========

R.I.Pienaar <rip@devco.net>
