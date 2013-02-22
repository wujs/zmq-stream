# ZMQStream

A set of stream-based Node bindings for ZeroMQ. The API is modeled after the [streams2](http://blog.nodejs.org/2012/12/20/streams2/) API.

## Differences from Streams2

Since [ZeroMQ is Not a Neutral Carrier](http://zguide.zeromq.org/page:all#-MQ-is-Not-a-Neutral-Carrier), the streams2 Duplex API ZMQStream uses is by _message_, not by byte. While the Duplex API is carried over in spirit, _do not_ try to read and write as if they're bytestreams, nor should you `pipe` a bytestream into or out of a ZMQStream Socket.

## Examples

In lieu of more verbose API documentation, I'll refer you to the (far from perfect) examples (sink, vent, router, and dealer) in the `examples` directory.

## License

Copyright (C) 2013 Michael Schoonmaker (michael.r.schoonmaker@gmail.com)

This project is free software released under the MIT/X11 license:

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
