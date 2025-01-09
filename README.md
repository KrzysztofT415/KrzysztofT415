## Hi there fellow coder 👋

<img align="right" alt="GIF" src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExZmEwODE4MmQ2OTE3M2VjOGRjMDVhNmIyMDI2NmM3OGI0M2VkYjVmYyZjdD1n/scZPhLqaVOM1qG4lT9/giphy.gif" style="width: 20vw"/>

I'm Chris 🙌, I am a PhD student at Wroclaw University of Science and Technology 💻, 
<br />
I finished specialization of Cryptography and Computer Security 🔒 in the field of Algorithmic Computer Science.
<br />
My PhD is focused on Security of Machine Learning Training Processes. 🤖
<br />
<br />
I have made several repositories for university assignments and few of my personal interests.
<br />
<br />
I'm happy to share it with you and I'd be glad if any of my work will help you accomplish your exercises. But of course don't copy it blindly, make sure you understand them! 😊
<br />
<br />
Stay positive! 👾 👾 👾
<br />
<br />
<a href="https://www.linkedin.com/in/krzysztoftalalaj/">
<img align="left" alt="err" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@8.7.0/icons/linkedin.svg" />
</a>
<a href="https://krzysztoft415.github.io/">
<img align="left" alt="err" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@8.7.0/icons/webflow.svg" />
</a>
<br />

## My "all-time favourite" lines of code [01.02.21]:
That's where my passion for programming have started. 😎
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
