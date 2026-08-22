# Weather Observation Station 9

![Platform](https://img.shields.io/badge/Platform-HackerRank-blue) ![Difficulty](https://img.shields.io/badge/Difficulty-Unknown-orange) ![Language](https://img.shields.io/badge/Language-Language-green)

## 🧩 Problem Summary

.MathJax_SVG_Display {text-align: center; margin: 1em 0em; position: relative; display: block!important; text-indent: 0; max-width: none; max-height: none; min-width: 0; min-height: 0; width: 100%}
.MathJax_SVG .MJX-monospace {font-family: monospace}
.MathJax_SVG .MJX-sans-serif {font-family: sans-serif}
.MathJax_SVG {display: inline; font-style: normal; font-weight: normal; line-height: normal; font-size: 100%; font-size-adjust: none; text-indent: 0; text-align: left; text-transform: none; letter-spacing: normal; word-spacing: normal; word-wrap: normal; white-space: nowrap; float: none; direction: ltr; max-width: none; max-height: none; min-width: 0; min-height: 0; border: 0; padding: 0; margin: 0}
.MathJax_SVG * {transition: none; -webkit-transition: none; -moz-transition: none; -ms-transition: none; -o-transition: none}
.mjx-svg-href {fill: blue; stroke: blue}
Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.Input Format.

## 💻 Solution

```language
/*
Enter your query here.
*/
select distinct city from station where lower(city) not like "a%"
and lower(city) not like "e%"
and lower(city) not like "i%"
and lower(city) not like "o%"
and lower(city) not like "u%";

```

## 🏷️ Tags

`HackerRank` `Coding` `Language`

## 📅 Solved On

2026-08-22

---
*Auto-pushed by [CodePush Extension](https://github.com)*
