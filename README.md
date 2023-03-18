## Hi there fellow coder 👋

<img align="right" alt="GIF" src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExZmEwODE4MmQ2OTE3M2VjOGRjMDVhNmIyMDI2NmM3OGI0M2VkYjVmYyZjdD1n/scZPhLqaVOM1qG4lT9/giphy.gif" />

I'm Krzysiek Tałałaj 🙌, I am a fourth-year student of Algorithmic Computer Science 💻, 
<br />
with specialization in Cryptography and Computer Security 🔒.
<br />
<br />
I have made several repositories for uni assignments, if anything could help you accomplish your exercises<br /> - feel free to copy paste, I don't mind. 😶‍🌫️
<br />
<br />
Be positive and stay healthy! 👾 👾 👾
<br />
<br />
<a href="https://www.linkedin.com/in/krzysztoftalalaj/">
<img align="left" alt="err" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@8.7.0/icons/linkedin.svg" />
</a>
<a href="https://krzysztoft415.github.io/">
<img align="left" alt="err" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@8.7.0/icons/webflow.svg" />
</a>
<br />

## My all-time favourite lines of code [01.02.21]:
Were written almost 3 years ago, after around 8 months me being into CS ❤️.\
It is called over class having set of polymorphic objects `ArrayList<T>` and filters it by casting onto filter class `searchedClass`.\
That's where my love for programming begun.
```java
public <T extends GameRule> ArrayList<T> getRulesOfType(Class<T> searchedClass) {
    ArrayList<T> rules = new ArrayList<>();
    for (GameRule rule : this.getRules()) {
        if (searchedClass.isInstance(rule)) {
            T ruleCast = searchedClass.cast(rule);
            rules.add(ruleCast);
        }
    }
    return rules;
}
```

## My recent lines of code [15.03.23]:
I had to implement md5 algorithm in any language, so I did it in js 😁.\
It uses pretty fun feature `Buffer`, which makes swapping little-endian to big-endian notation really easy.\
You can just call `buffer.swap32()` 🥳.
```javascript
let hashArray = new Uint32Array(4)
hashArray[0] = ivBuffer.readUInt32BE(0)
hashArray[1] = ivBuffer.readUInt32BE(4)
hashArray[2] = ivBuffer.readUInt32BE(8)
hashArray[3] = ivBuffer.readUInt32BE(12)

for (let j = 0; j < processedBuffer.length; j += 64) {
    let W = new Uint32Array(hashArray)
    // Just md5 stuff ahead
    for (let i = 0; i < 64; i++) {
        let [F, g] = [0, 0]
       
        // Rounds
        if (i <= 15) [F, g] = [(W[1] & W[2]) | (~W[1] & W[3]), i]
        else if (i <= 31) [F, g] = [(W[3] & W[1]) | (~W[3] & W[2]), (5 * i + 1) % 16]
        else if (i <= 47) [F, g] = [W[1] ^ W[2] ^ W[3], (3 * i + 5) % 16]
        else [F, g] = [W[2] ^ (W[1] | ~W[3]), (7 * i) % 16]
        
        F += W[0] + K[i] + processedBuffer.readUInt32LE(j + g * 4)
        let rot = (F << s[i]) | (F >>> (32 - s[i]))
        ;[W[0], W[1], W[2], W[3]] = [W[3], W[1] + rot, W[1], W[2]]
    }
    // Append to current hashState
    hashArray[0] += W[0] //A
    hashArray[1] += W[1] //B
    hashArray[2] += W[2] //C
    hashArray[3] += W[3] //D
}

return Buffer.from(hashArray.buffer).swap32().toString('hex') // Converting to BE notation.
```
