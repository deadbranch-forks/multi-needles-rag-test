# Characteristics

| what | value |
|---|---|
| *Pre-goal summary* | **yes** |
| *`<Instructions`> xml tags* | no |
| Instructions reference `<Documents>`? | no |
| *`<Document>` xml tags* | no |

# Prompt Template
```md
Answer the questions using the text as your knowledge corpus..

# Goal

Answer the following questions based on the text included below. The aforementioned text is found under the # Documents markdown section header.
1. Where is the best place to have lunch in Lukovit?
2. What are the key words (part 2)?
3. What are dolphins known for?
4. What are the key words (part 1)?

---

# Documents

{document}
```

# Results

## 104k prompt

### Result text

>1. The best place to have lunch in Lukovit is the **Konservenata restaurant**.
>2. Key words (Part 2): "Exponential Growth, Thresholds, Network Effects, Winner Takes All, Ambition, Learning, Curiosity, Competition."
>3. Dolphins are known for their **advanced civilizations**, including **complex underwater cities** complete with **schools, libraries, and aquatic technology**.
>4. Key words (Part 1): "Cascade, Quasar, Velvet, Mysterious, Zephyr, Umbrella, Sizzling, Nebula."
>
>Superlinear takeaways, right? 🚀

### Analysis

#2 is wrong.
