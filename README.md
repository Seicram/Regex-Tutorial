# Tutorial: Understanding the "Email Validation" Regular Expression

## Introduction

Welcome to this tutorial on understanding the "Email Validation" regular expression. In this tutorial, we will explore the components of a regular expression that can be used to validate email addresses. Regular expressions, often referred to as regex, are powerful tools for pattern matching and data validation. The email validation regex we will be discussing in this tutorial is widely used and provides a basic level of validation for most common email address formats.

## Summary

The regular expression we will be examining is as follows:
This regex is designed to match and validate email addresses. It checks for the correct format of an email address, including the presence of an "@" symbol, a domain name, and a valid top-level domain (TLD). Let's break down each component of this regex and understand what it does.

## Table of Contents

1. [Matching the Username Part](#section-1-matching-the-username-part)
2. [Matching the Domain Part](#section-2-matching-the-domain-part)
3. [Matching the Top-Level Domain](#section-3-matching-the-top-level-domain)
4. [Putting It All Together](#section-4-putting-it-all-together)
5. [Other Regex Examples to Explore](#section-5-other-regex-examples-to-explore)
6. [About the Author](#section-6-about-the-author)

## Section 1: Matching the Username Part

The username part of an email address is the portion before the "@" symbol. It can consist of alphanumeric characters, underscores, periods, and hyphens. The regex component for matching the username part is `[\w.-]+`. This component performs the following tasks:

- `[\w.-]` is a character class that matches any word character (letters, numbers, and underscores), a period, or a hyphen.
- The `+` quantifier ensures that the username part consists of one or more characters from the character class.

Example:
In the above example, the regex matches the username part "john.doe".

## Section 2: Matching the Domain Part

The domain part of an email address is the portion after the "@" symbol but before the TLD. It can consist of alphanumeric characters and hyphens. The regex component for matching the domain part is `([\w-]+\.)+`. This component performs the following tasks:

- `[\w-]` is a character class that matches any word character (letters, numbers, and underscores) or a hyphen.
- `+` quantifier ensures that the domain part consists of one or more characters from the character class.
- `\.` matches the dot (.) symbol literally, ensuring that it separates each subdomain within the domain part.
- `([\w-]+\.)+` allows for multiple subdomains separated by dots.

Example:
In the above example, the regex matches the domain part "example.domain".

## Section 3: Matching the Top-Level Domain

The top-level domain (TLD) is the last part of the domain and represents the highest level in the domain naming system. It usually consists of two to four characters, such as .com, .net, or .org. The regex component for matching the TLD is `[\w-]{2,4}`. This component performs the following tasks:

- `[\w-]` is a character class that matches any word character (letters, numbers, and underscores) or a hyphen.
- `{2,4}` specifies the allowed length of the TLD, allowing for TLDs with a minimum length of 2 and a maximum length of 4.

Example:
In the above example, the regex matches the TLD "com".

## Section 4: Putting It All Together

Now that we have understood each component, let's combine them to validate the entire email address. The complete regex is `^[\w.-]+@([\w-]+\.)+[\w-]{2,4}$`. Let's analyze the full regex:

- `^` asserts the start of the string.
- `[\w.-]+` matches the username part.
- `@` matches the "@" symbol literally.
- `([\w-]+\.)+` matches the domain part.
- `[\w-]{2,4}` matches the TLD.
- `$` asserts the end of the string.

Example:
In the above example, the regex matches the entire email address "<john.doe@example.domain.com>".

## Section 5: Other Regex Examples to Explore

Here are some other regex examples that you can explore to expand your knowledge and understanding of regular expressions:

- Matching a URL:  `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`

- Validating a Password:  `^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[a-zA-Z\d]{8,}$`

- Extracting Phone Numbers:  `^\+\d{1,3} \(\d{3}\) \d{3}-\d{4}$`

- Finding Dates in a Text:  `^(0?[1-9]|1[0-2])\/(0?[1-9]|[12]\d|3[01])\/(19|20)\d{2}$`

- Parsing HTML Tags:  `<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)`

Feel free to research and experiment with these regex examples to further enhance your regex skills.

## Section 6: About the Author

This tutorial was written by Marcies Smith. You can find more projects and resources on the author's [GitHub profile](https://github.com/Seicram/Regex-Tutorial).

Congratulations! You have successfully learned about the components of the "Email Validation" regular expression. Regular expressions are incredibly versatile and can be used for various types of pattern matching and validation. Experiment with different patterns and explore more advanced features to enhance your understanding of regex.
