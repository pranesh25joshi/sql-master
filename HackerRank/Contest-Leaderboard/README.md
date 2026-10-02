# Contest Leaderboard

![Platform](https://img.shields.io/badge/Platform-HackerRank-blue) ![Difficulty](https://img.shields.io/badge/Difficulty-Unknown-orange) ![Language](https://img.shields.io/badge/Language-Language-green)

## 🧩 Problem Summary

.MathJax_SVG_Display {text-align: center; margin: 1em 0em; position: relative; display: block!important; text-indent: 0; max-width: none; max-height: none; min-width: 0; min-height: 0; width: 100%}
.MathJax_SVG .MJX-monospace {font-family: monospace}
.MathJax_SVG .MJX-sans-serif {font-family: sans-serif}
.MathJax_SVG {display: inline; font-style: normal; font-weight: normal; line-height: normal; font-size: 100%; font-size-adjust: none; text-indent: 0; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0; min-height: 0; border: 0; padding: 0; margin: 0}
.MathJax_SVG * {transition: none; -webkit-transition: none; -moz-transition: none; -ms-transition: none; -o-transition: none}
.mjx-svg-href {fill: blue; stroke: blue}
You did such a great job helping Julia with her last coding contest challenge that she wants you to work on this one, too! 


## 💻 Solution

```language
    name, 
    sum(max_score) as total_score
from
    (select 
        name,
        hacker_id,
        challenge_id,
        max(score) as max_score
    from 
        (select 
            h.name,
            s.submission_id,
            s.hacker_id,
            s.challenge_id,
            s.score
        from 
            hackers h 
        join submissions s 
        on h.hacker_id = s.hacker_id) as sub
    group by name, hacker_id, challenge_id ) t 
    hacker_id, 
*/
select 
Enter your query here.
/*
```

## 🏷️ Tags

`HackerRank` `Coding` `Language`

## 📅 Solved On

2026-10-02

---
*Auto-pushed by [CodePush Extension](https://github.com)*
