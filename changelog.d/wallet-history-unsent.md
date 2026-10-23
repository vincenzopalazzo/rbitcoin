Fixed

- **Electrum stays down until the follow headers round is applied.** The bind waits until each initial `getheaders` sent after the follow dials has been applied, the header tip is not ahead of the block tip, and the scripthash head covers that tip. A headers message that is not one of those sends does not open it, and neither does a two-second timeout.
