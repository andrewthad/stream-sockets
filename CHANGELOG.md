# Revision history for stream-sockets

## 0.6.0.0

* Give slab types a phantom type argument that indicates whether
  or not they operate on pinned byte arrays. This makes it possible
  to provide a `bytestring` interface to `recvmmsg`.
* Upgrade interruptible datagram interface to work with new slabs.

## 0.5.0.0

* Add support for getting back `ECONNREFUSED` when send or receiving
  with datagram sockets.
* Add support for using `Addr` and `ByteString` with datagram sockets.
* Add sendMany for vectored io on a stream socket.
* Correct the implementation of interruptible functions that
  work on datagram sockets.

## 0.4.0.0

* Overhaul the interface. Aggressively use backpack.

## 0.3.1.0

* Add functions for sending strict bytestrings and lazy bytestrings
  over a stream socket (`sendByteArray` and `sendLazyByteArray`).
* Add `receiveByteString` to `Socket.Stream.IPv4`. This is a function
  for receive strict bytestring.
* Add `sendAddr`. This is used in the implementations of both
  `sendByteArray` and `sendLazyByteArray`.

## 0.3.0.0

* Totally redo almost everything. The API is now considered fairly
  stable.

## 0.1.0.0 -- 2019-01-18

* First version. Released on an unsuspecting world.
