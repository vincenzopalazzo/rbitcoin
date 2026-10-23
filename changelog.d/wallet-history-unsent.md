Fixed

- **Electrum stays down until the follow headers round is indexed.** A block mined while scripthash materialize runs is no longer missing from the first history answer. The bind waits until that `getheaders` has been applied and the scripthash head covers the tip, not merely until the message is counted or two seconds have passed.
