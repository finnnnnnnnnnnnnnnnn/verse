# Verse
## data transfer and updates
Data will be transfered based on the QUIC transport protocol. The QUIC transport has several benefits; unlive TCP, QUIC does not suffer from head-of-line blocking issues, and unlike UDP QUIC is able to send reliable packets. In order to acheive realtime collaboration in the 3D space, mesh updates must be handled, but resending the entire mesh each time for a change is wasteful, so the delta between the existing version of the mesh and the updated one must be calculated and sent. This creates a data agnostic way of sending changes, removing the need for specific commands to be defined.

## USD
Scene data will be stored in the USD format. This enables easy interface with other 3D applications, as the format is widely utilized. Verse will essentially function as a library for realtime collboration on USD data. Ideally, verse code will be able to be generated from USD directly, enabling easily keeping the library up to date with USD updates.

## auth
\#todo

## TODO
 - Create PoC of generating the library based on [usd-rs](https://github.com/luke-titley/usd-rs)
 - Update [usd-rs](https://github.com/luke-titley/usd-rs) to support the entire USD API
 - Build authentication and other elements of the library
