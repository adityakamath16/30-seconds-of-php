---
title:  firstStringBetween
tags: string,beginner
---

Returns the first string there is between the strings from the parameter `$start` and `$end`.

- Use `trim()` and `strstr()` to find the string contained between `$start` and `$end`.

```php
function firstStringBetween($haystack, $start, $end)
{
  return trim(strstr(strstr($haystack, $start), $end, true), $start . $end);
}
```

```php
firstStringBetween('This is a [custom] string', '[', ']'); // custom
```
