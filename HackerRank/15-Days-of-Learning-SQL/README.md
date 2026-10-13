# 15 Days of Learning SQL

![Platform](https://img.shields.io/badge/Platform-HackerRank-blue) ![Difficulty](https://img.shields.io/badge/Difficulty-Unknown-orange) ![Language](https://img.shields.io/badge/Language-Language-green)

## 🧩 Problem Summary

.MathJax_SVG_Display {text-align: center; margin: 1em 0em; position: relative; display: block!important; text-indent: 0; max-width: none; max-height: none; min-width: 0; min-height: 0; width: 100%}
.MathJax_SVG .MJX-monospace {font-family: monospace}
.MathJax_SVG .MJX-sans-serif {font-family: sans-serif}
.MathJax_SVG {display: inline; font-style: normal; font-weight: normal; line-height: normal; font-size: 100%; font-size-adjust: none; text-indent: 0; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0; min-height: 0; border: 0; padding: 0; margin: 0}
.MathJax_SVG * {transition: none; -webkit-transition: none; -moz-transition: none; -ms-transition: none; -o-transition: none}
.mjx-svg-href {fill: blue; stroke: blue}
Julia conducted a  days of learning SQL contest. The start date of the contest was March 01, 2016 and the end date was March

## 💻 Solution

```language
        FROM
        (
            SELECT
                submission_date,
                hacker_id,
                COUNT(*) AS cnt
            FROM submissions
            GROUP BY submission_date, hacker_id
        ) t2
        GROUP BY submission_date
    ) t3

    ON t1.submission_date = t3.submission_date
    AND t1.cnt = t3.max_cnt

    GROUP BY t1.submission_date
) t

ON d.submission_date = t.submission_date

JOIN hackers h
ON t.hacker_id = h.hacker_id

ORDER BY d.submission_date;

```

## 🏷️ Tags

`HackerRank` `Coding` `Language`

## 📅 Solved On

2026-10-13

---
*Auto-pushed by [CodePush Extension](https://github.com)*
