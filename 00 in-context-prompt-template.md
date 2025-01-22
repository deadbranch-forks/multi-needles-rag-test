# Characteristics

| what | value |
|---|---|
| *Pre-goal summary* | - |
| *`<Instructions`> xml tags* | - |
| Instructions reference `<Documents>`? | - |
| *`<Document>` xml tags* | - |

# Prompt Template
```md
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

| document | score | Notes |
|---|---|---|
| 104k | 3/4 | *#2 incorrect* |
| **97k** | **4/4** | **success.** |

## Result text

### 104k

>1. The best place to have lunch in Lukovit is the **"Konservenata" restaurant**.
>
>2. ~~Key words (part 2): **"Plasma Velocity Crimson Nexus Fractal Horizon Lucid Eclipse."**~~
>
>3. Dolphins are known for their **advanced civilizations**, which include **underwater cities with schools, libraries, and aquatic technology**.
>
>4. Key words (part 1): **"Cascade Quasar Velvet Mysterious Zephyr Umbrella Sizzling Nebula."**

### 97k

>1. The best place to have lunch in Lukovit is the "Konservenata" restaurant.
>
>2. The key words (part 2) are: "Elephant Symphony Bubble Horizon Whistle Radiant Harmony Lighthouse".
>
>3. Dolphins are known for their advanced civilizations, including complex underwater cities, schools, libraries, and aquatic technology.
>
>4. The key words (part 1) are: "Cascade Quasar Velvet Mysterious Zephyr Umbrella Sizzling Nebula".
