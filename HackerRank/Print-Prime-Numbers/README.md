# Print Prime Numbers

![Platform](https://img.shields.io/badge/Platform-HackerRank-blue) ![Difficulty](https://img.shields.io/badge/Difficulty-Unknown-orange) ![Language](https://img.shields.io/badge/Language-Language-green)

## 🧩 Problem Summary

.MathJax_SVG_Display {text-align: center; margin: 1em 0em; position: relative; display: block!important; text-indent: 0; max-width: none; max-height: none; min-width: 0; min-height: 0; width: 100%}
.MathJax_SVG .MJX-monospace {font-family: monospace}
.MathJax_SVG .MJX-sans-serif {font-family: sans-serif}
.MathJax_SVG {display: inline; font-style: normal; font-weight: normal; line-height: normal; font-size: 100%; font-size-adjust: none; text-indent: 0; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0; min-height: 0; border: 0; padding: 0; margin: 0}
.MathJax_SVG * {transition: none; -webkit-transition: none; -moz-transition: none; -ms-transition: none; -o-transition: none}
.mjx-svg-href {fill: blue; stroke: blue}
Write a query to print all prime numbers less than or equal to . Print your result on a single line, and use the ampersand (

## 💻 Solution

```language
/*
Enter your query here.
*/
WITH RECURSIVE numbers AS (
    SELECT 2 AS n
    UNION ALL
    SELECT n + 1
    FROM numbers
    WHERE n < 1000
)
SELECT GROUP_CONCAT(n SEPARATOR '&')
FROM numbers num
WHERE NOT EXISTS (
    SELECT 1
    FROM numbers d
    WHERE d.n BETWEEN 2 AND FLOOR(SQRT(num.n))
      AND MOD(num.n, d.n) = 0
);

```

## 🏷️ Tags

`HackerRank` `Coding` `Language`

## 📅 Solved On

2026-10-16

---
*Auto-pushed by [CodePush Extension](https://github.com)*
