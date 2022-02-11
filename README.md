# Blockchain-nodejs
I'm trying to lern Blockchain

# Install
```
npm install
```

# Package
1. crypto-js
2. express
3. nodemon

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
