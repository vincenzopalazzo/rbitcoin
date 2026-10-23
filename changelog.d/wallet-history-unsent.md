Fixed

- **Electrum stays down until the follow headers round is indexed.** A block mined while scripthash materialize runs is no longer missing from the first history answer when that `getheaders` starts more than two seconds after the follow dial.
