Fixed

- **Electrum stays down until the follow headers rounds are applied.** Each follow dial publishes a round when the handshake finishes. The bind waits until those rounds are applied or the peer will not send getheaders, the header tip is not ahead of the block tip, and the scripthash head covers that tip. A headers message that is not one of those rounds does not open it.
