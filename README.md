Yii2 attachments
================

This is a fork of the [original extension](https://github.com/Nemmo/yii2-attachments) published by [Nemmo](https://github.com/Nemmo). 
See the file ORIGINAL_README.md for details on the original version.

Motivations
-----------

This version addresses two problems found on the original one:

1. if two files with the same binary content are uploaded the hash should be use for preventing duplication of binary data;
2. for security reasons, a user should not be able to retrieve a file just by id (using the hash code in the URL provides a simple way to prevent this).

Use
---

To use this extension, just add 

    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/loristissino/yii2-attachments"            
        }
    ]

in your project's composer.json file.

Since this fork's composer.json file contains 

    "autoload": {
      "psr-4": {
        "nemmo\\attachments\\": "src"
      }
      
you still use nemmo references in your code (for example, `use nemmo\attachments\components\AttachmentsInput;`).
