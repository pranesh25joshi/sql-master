# Interviews

![Platform](https://img.shields.io/badge/Platform-HackerRank-blue) ![Difficulty](https://img.shields.io/badge/Difficulty-Unknown-orange) ![Language](https://img.shields.io/badge/Language-Language-green)

## 🧩 Problem Summary

.MathJax_SVG_Display {text-align: center; margin: 1em 0em; position: relative; display: block!important; text-indent: 0; max-width: none; max-height: none; min-width: 0; min-height: 0; width: 100%}
.MathJax_SVG .MJX-monospace {font-family: monospace}
.MathJax_SVG .MJX-sans-serif {font-family: sans-serif}
.MathJax_SVG {display: inline; font-style: normal; font-weight: normal; line-height: normal; font-size: 100%; font-size-adjust: none; text-indent: 0; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0; min-height: 0; border: 0; padding: 0; margin: 0}
.MathJax_SVG * {transition: none; -webkit-transition: none; -moz-transition: none; -ms-transition: none; -o-transition: none}
.mjx-svg-href {fill: blue; stroke: blue}
Samantha interviews many candidates from different colleges using coding challenges and contests. Write a query to print the

## 💻 Solution

```language
/*
Enter your query here.
*/


SELECT
    colleges.contest_id,
    contests.hacker_id,
    contests.name,
    SUM(sub3.total_submissions) AS total_submissions,
    SUM(sub3.total_accepted_submissions) AS total_accepted_submissions,
    SUM(sub3.total_views) AS total_views,
    SUM(sub3.total_unique_views) AS total_unique_views
FROM
(
    SELECT
        c.challenge_id,
        c.college_id,
        COALESCE(ss.total_submissions,0) AS total_submissions,
        COALESCE(ss.total_accepted_submissions,0) AS total_accepted_submissions,
        COALESCE(vs.total_views,0) AS total_views,
        COALESCE(vs.total_unique_views,0) AS total_unique_views
    FROM challenges c

    LEFT JOIN
```

## 🏷️ Tags

`HackerRank` `Coding` `Language`

## 📅 Solved On

2026-10-13

---
*Auto-pushed by [CodePush Extension](https://github.com)*
