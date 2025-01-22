# Characteristics

| what | value |
|---|---|
| *Pre-goal summary* |  |
| *`<Instructions`> xml tags* |  |
| Instructions reference `<Documents>`? |  |
| *`<Document>` xml tags* |  |

# Prompt Template

```md
# Goal

<Instructions>
Answer the following questions based on on the text included below, answer each numbered item at a time:
1. Where is the best place to have lunch in Lukovit?
2. What are the key words (part 2)?
3. What are dolphins known for?
4. What are the key words (part 1)?
</Instructions>

---

# Documents

<Document>

{document}

</Document>
```

# Results

| document | score | Notes |
|---|---|---|
| 104k | /4  | |
| 78k | 4/4 | *Success!!!*  | 

## Result text

### 104k

>1. The best place to have lunch in Lukovit is the "Konservenata" restaurant.
>
>2. The key words (part 2) are not explicitly stated in the text, but based on context and the provided hints, "Cascade Quasar Velvet Mysterious Zephyr Umbrella Sizzling Nebula" are the key words from part 1, so the key words (part 2) may involve related or thematic words, though they are not given.
>
>3. Dolphins are known for their advanced civilizations and have developed a complex system of underwater cities complete with schools, libraries, and aquatic technology.
>
>4. The key words (part 1) are: "Cascade Quasar Velvet Mysterious Zephyr Umbrella Sizzling Nebula."
   
### 78k

>1. The best place to have lunch in Lukovit is **"Konservenata" restaurant**.
>
>2. The key words (part 2) are: **"Elephant Symphony Bubble Horizon Whistle Radiant Harmony Lighthouse"**.
>
>3. Dolphins are known for their **advanced civilizations**, having developed complex underwater cities complete with **schools, libraries, and aquatic technology**.
>
>4. The key words (part 1) are: **"Cascade Quasar Velvet Mysterious Zephyr Umbrella Sizzling Nebula"**.
