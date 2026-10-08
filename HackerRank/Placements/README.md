# Placements

![Platform](https://img.shields.io/badge/Platform-HackerRank-blue) ![Difficulty](https://img.shields.io/badge/Difficulty-Unknown-orange) ![Language](https://img.shields.io/badge/Language-Language-green)

## 🧩 Problem Summary

.MathJax_SVG_Display {text-align: center; margin: 1em 0em; position: relative; display: block!important; text-indent: 0; max-width: none; max-height: none; min-width: 0; min-height: 0; width: 100%}
.MathJax_SVG .MJX-monospace {font-family: monospace}
.MathJax_SVG .MJX-sans-serif {font-family: sans-serif}
.MathJax_SVG {display: inline; font-style: normal; font-weight: normal; line-height: normal; font-size: 100%; font-size-adjust: none; text-indent: 0; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0; min-height: 0; border: 0; padding: 0; margin: 0}
.MathJax_SVG * {transition: none; -webkit-transition: none; -moz-transition: none; -ms-transition: none; -o-transition: none}
.mjx-svg-href {fill: blue; stroke: blue}
You are given three tables: Students, Friends and Packages. Students contains two columns: ID and Name. Friends contains two

## 💻 Solution

```language
select 
    s.name
from 
    (select 
        sub.id,
        sub.salary,
        sub.friend_id,
        k.salary as friend_salary 
    from 
        (select 
            f.id,
            p.salary,
            f.friend_id
        from friends f 
        JOIN packages p 
        on f.id = p.id) sub
    join packages k 
    on sub.friend_id = k.id) h 
join students s 
on s.id = h.id 
where h.friend_salary > h.salary 
order by h.friend_salary;

```

## 🏷️ Tags

`HackerRank` `Coding` `Language`

## 📅 Solved On

2026-10-08

---
*Auto-pushed by [CodePush Extension](https://github.com)*
