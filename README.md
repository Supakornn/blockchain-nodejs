# Blockchain-nodejs

# Install
```
npm install
```

# Example
```js
class Block {
    constructor(
        index,
        timestamp,
        transaction,
        precedingHash = ''
    ) {
        this.index = index;
        this.timestamp = timestamp;
        this.transaction = transaction;
        this.precedingHash = precedingHash;
        this.hash = this.computeHash();
    }

    computeHash() {
        return sha256(
            this.index +
            this.precedingHash + 
            this.timestamp + 
            JSON.stringify(this.transaction)
        ).toString();
    }
}
```
