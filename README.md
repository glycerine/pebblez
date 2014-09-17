pebblez
=======

pebblez is using protocol buffers over zeromq. This is a lego technology: snap together two pieces of existing, well-engineered technology.

See the Golang and R demonstration project here:

[https://github.com/mailgun/pebblezgo](https://github.com/mailgun/pebblezgo)

A Letter on Why Pebblez rocks
=================

N.B. All Flintstones references appreciated. :D

What I like about protobuf over zeromq is that it is SO DARN UNIVERSAL.

Sure the next generation tech (capnproto over nanomsg) will be more scalable and has more features (see my [gozbus repo](https://github.com/glycerine/gozbus) for example), but the language support (e.g. in gogoprotobuf) is freaking amazing. 

*AND* this is the biggie: It works in R (yeeeeesssss!!), as the [pebblezgo project](https://github.com/mailgun/pebblezgo) demonstrates.

And it is not just for R, because *everybody* and their dog has a pebblez transport available!

If you are looking for language support:

The starting list of zeromq bindings: http://zeromq.org/bindings:_start

The starting list of protobuf bindings: https://github.com/google/protobuf/wiki/Third-Party-Add-ons

but specifically:

* R : install.packages(c("rzmq","RProtoBuf"))

* golang (demonstrated in [pebblezgo](https://github.com/mailgun/pebblezgo))

* lua/luajit ( https://github.com/Neopallium/lua-zmq  +  https://github.com/Neopallium/lua-pb )

* python (pip install pyzmq / protocol buffer support shipped from google in the protobuf package)

* java (yes)

* c++ (yes)

* php (the universe should forbid anyone ever use php ever again, but yes)

* javascript (on node, yes. on browser, can be gatewayed: https://github.com/dcodeIO/ProtoBuf.js + http://stackoverflow.com/questions/8145060/zeromq-in-javascript-client )

Bonus: gogoprotobuf adds the JSON annotations to your structs automatically, making exporting your messages to JSON completely trivial.

* ruby (somebody wrote a gateway; http://avalanche123.com/blog/2012/02/25/interacting-with-zeromq-from-the-browser/  and https://github.com/progrium/nullmq/tree/master/demos/presence )


Hence: No need for crappy/impossible to maintain/impossible to refactor/slow dynamic-typing ever again. Type strong schema for everyone!  Plus evolve-able protocols (add/deprecate fields over time).

Additional Guidance on how to switch on messages:

* [Tagging messages during pub/sub](http://www.dotkam.com/2011/09/09/zeromq-and-google-protocol-buffers/)

* [Identifying different event messages with a union](https://developers.google.com/protocol-buffers/docs/techniques#union)



Kindest regards,

Jason


p.s. Plus there is a security wrapper available too, http://curvezmq.org/. SWEET!!

p.p.s. Obviously my next project with this technology must be called [BamBam](https://github.com/glycerine/bambam) &lt;/flintstones reference&gt;
