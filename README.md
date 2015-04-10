# File Name Conventions

A collection of guidelines for writing file names used in web projects.

## Possible characters

### Use dashes as delimiters

- You should use dashes (-) as delimiters.
- Periods are allowed in some cases, such as for languages and conditions.
- Never use spaces or underscores. Spaces are converted to %20 in URLs or can break an URL when shared. Underscores are difficult to see when the file name is displayed as an underlined link. Although the use of underscores does not impact your ranking that much, [Google advices not to use underscores](https://www.youtube.com/watch?v=AQcSFsQyct8).
- Exceptions apply for functional requirements, such as for [Sass partials](http://sass-lang.com/guide#topic-4). A leading underscore informs the Sass compiler a file is only a partial file and should never be generated into a stand alone CSS file.

**Right:**
```
file-name-with-dashes.en.min.html
```

### Do not use special characters

Avoid using non-alphanumeric characters in file names, such as: '*' ':' '\' '/' '<' '>' '|' '"' '!' '?' '[' ']' ';' '=' '+' '&' '£' '$' '€' '%' or ','. These characters can have special meaning in programming languages or can cause problems with different operating systems.

### Use lowercase, never uppercase

We should always consider URLs as case-sensitive according to [W3.org](http://www.w3.org/TR/WD-html40-970708/htmlweb.html). Therefore, use lowercase to reduces errors when typing URLs.

## Write sections of a file name in a consistent order

Sections should be written in this order:

1. Description
2. Number
3. Date
4. Image size, pixel density, target device
5. Version number
6. Status
7. Language code
8. file conditions

**Possible combinations**
```
description-01-2015010~palm-1.0b-draft.en.min.js /* extreme combination */
description.min.js
description.en.html
description-01.jpg
description-02.jpg
description-1024x768@2x.jpg
description~desk@2x.jpg
```

### Write description for developers and users

Don't be afraid to write long informative file names. Few people type a file name manually and most operating systems support [255 characters](http://en.wikipedia.org/wiki/Comparison_of_file_systems). But only add information that makes it easy for users and developers to recognize files from one another at a glance. For the description use information such as:

- type of data
- project name or acronym
- subjects
- people's names
- characteristics
- location

> **Give your images detailed, informative filenames** The filename can give Google clues about the subject matter of the image. Try to make your filename a good description of the subject matter of the image. For example, my-new-black-kitten.jpg is a lot more informative than IMG00023.JPG. Descriptive filenames can also be useful to users: If we're unable to find suitable text in the page on which we found the image, we'll use the filename as the image's snippet in our search results. - [Google, 2015, Image publishing guidelines](https://support.google.com/webmasters/answer/114016?hl=en)

#### Keep people's names compact

Sometimes you want to include the name of a person in the file name, e.g. the author or the person in the photo.

- Write names without word delimiters.
- Only write initials for the first name and write the last name in full. There are two exceptions: (1) when the last name or final file name is very long you may use initials for the last name; (2) when there is already a person with the same combination, you may write the first name in full.
- If people have exactly the same name written in full, you can add a number: firstnamelastname2.

**Right:**
```
bvandebiezen.jpg
shoogenhout.jpg
a-very-long-description-with-name-bvdb.jpg
asmith.jpg
adamsmith.jpg
adamsmith2.jpg
```

### Use two or more digits to distinguish sequential files with the same description

- Start number with a dash as a delimiter.
- Add a zero to single digit numbers, e.g. '01' instead of '1'.
- Numbers may also be placed before the description if needed. A dash will still be used as delimiter with the description.

**Right:**
```
description-01.jpg
description-02.jpg
description-03.jpg
description-04.jpg

01-description.jpg
02-description.jpg
03-description.jpg
04-description.jpg
```

### Keep dates or date ranges compact and start with year

- Write dates without delimiters.
- Always use four digits for years, two digits for months and two digits for days.
- Start with year, then month, and end with day if available: yyyymmdd, yyyymm, or yyyy. This makes sure similar file names are sorted by date when sorted alphabetically.
- Use a double dash to separate two dates describing an interval: yyyy--yyyy. Start with the earliest date.

**Right:**
```
description-20150401.php
description-201504.php
description-2015.php
description-2000--2010.php
```

See ['ISO 8601'](https://en.wikipedia.org/wiki/ISO_8601) for further reading.

### Use special modifiers for image sizes, target devices or media queries, and pixel densities.

Modifiers are inspired by [Apple iOS naming conventions](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/LoadingResources/ImageSoundResources/ImageSoundResources.html#//apple_ref/doc/uid/10000051i-CH7-SW1).

- Order should be: size, target device or media query, pixel density.
- Start image sizes with a dash (-) as delimiter.
- Start media queries with a tilde (~) as delimiter.
- Start pixel density with an at-sign (@) as delimiter.
- When only a width or height is available or applicable, add a 'w' for width or 'h' for height directly after the the amount of pixels.
- When both measurements are available, do not add a 'w' or 'h' and separate the width and height with an 'x'.

**Right:**
```
description@2x.jpg
description~lap.jpg
description~desk.jpg
description~lap@2x.jpg
description-1024w~palm@2x.jpg
description-568h~iphone@2x.jpg
description-1024x768~palm@2x.jpg
```

### Use version numbers if available

- Start version with a dash (-) as delimiter.
- Use periods (.) to separate point releases.
- Always add trailing zeros to major releases, e.g. '2.0' instead of '2'.
- Types, such as 'a' (alpha), 'b' (beta), 'rc1' (release candidate 1) can be added without delimiters.

**Right:**
```
description-0.5.js
description-1.0b.js
description-1.0rc1.js
```

### Add status when needed

- You can optionally add a file status such as 'draft' and 'published'.
- Start status with a dash.

**Right:**
```
description-draft.md
```

### Add language code only when different languages are available

- Use a period to separate the language code from the rest of the file name.
- Use [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes), two-letter codes, for languages.
- Only add languages when different languages are available.

**Right:**
```
description.nl.txt
description.en.txt
```

### Add file conditions just before the file extension

- The file condition should be the last part, just before the file extension.
- Use a period (.) to separate the condition from the rest of the file name.
- Use periods (.) as a delimiter for different conditions.

**Right:**
```
description.min.js
description.custom1234.min.js
```

## Rewrite original file names not following conventions

It is not preferred to keep file names in it's original format if it doesn't match your file name conventions. But in some cases it is easier to keep the file name untouched. Sometimes you want to easily replace a file with a newer one from the original source in the future.
