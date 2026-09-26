# Ollivander's Inventory

![Platform](https://img.shields.io/badge/Platform-HackerRank-blue) ![Difficulty](https://img.shields.io/badge/Difficulty-Unknown-orange) ![Language](https://img.shields.io/badge/Language-Language-green)

## 🧩 Problem Summary

.MathJax_SVG_Display {text-align: center; margin: 1em 0em; position: relative; display: block!important; text-indent: 0; max-width: none; max-height: none; min-width: 0; min-height: 0; width: 100%}
.MathJax_SVG .MJX-monospace {font-family: monospace}
.MathJax_SVG .MJX-sans-serif {font-family: sans-serif}
.MathJax_SVG {display: inline; font-style: normal; font-weight: normal; line-height: normal; font-size: 100%; font-size-adjust: none; text-indent: 0; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0; min-height: 0; border: 0; padding: 0; margin: 0}
.MathJax_SVG * {transition: none; -webkit-transition: none; -moz-transition: none; -ms-transition: none; -o-transition: none}
.mjx-svg-href {fill: blue; stroke: blue}
Harry Potter and his friends are at Ollivander's with Ron, finally replacing Charlie's old broken wand. 

Hermione decides t

## 💻 Solution

```language
SELECT
    w.id,
    wp.age,
    w.coins_needed,
    w.power
FROM wands w
JOIN wands_property wp
    ON w.code = wp.code
WHERE wp.is_evil = 0
AND w.coins_needed = (
    SELECT MIN(w1.coins_needed)
    FROM wands w1
    JOIN wands_property wp1
        ON w1.code = wp1.code
    WHERE wp1.is_evil = 0
      AND w1.power = w.power
      AND wp1.age = wp.age
)
ORDER BY
    w.power DESC,
    wp.age DESC;

```

## 🏷️ Tags

`HackerRank` `Coding` `Language`

## 📅 Solved On

2026-09-26

---
*Auto-pushed by [CodePush Extension](https://github.com)*
