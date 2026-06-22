
---
# <div align="center">*__CSS Lessons__*<div>
---
## **Lessons by @ezsnippet – IG [Neeraj Wallia Sensei]**

### *__Shortcuts__*
1. HTML Boiler plate code, press : `!`+`Tab`

### *__Concepts__*
1. [CSS Introduction](#1-what-is-web-development)



---
### 1. CSS Intorduction

- CSS stands for `C`ascading `S`tyle `S`heets.
- There one type of CSS called `Inline CSS`, which is declared inside the line or tags. 
- SO there are 3 types of CSS : 
    1. Internal CSS
    2. External CSS : 
    - Its like creating a separe file with `.css` extention.
    - This is used often as the code looks much cleaner.
    3. Inline CSS : 
    - Here we use it say inside a `<p>` tag.
    - For inline inside the tag we need to give a *`Attribute`* called *`Style`*, which had *`Properties`* like color, etc. Ex: 
        ```html
        <p style="color:blue">
            The Audi R8 is a mid-engine, 2-seater sports car, which uses Audi's trademark quattro permanent all-wheel drive system.<br>
            It was introduced by the German car manufacturer Audi AG in 2006.Production ended in the first quarter of 2024. <br>
        </p>
        ```
    - you can also give color like the following : 
        ```html
        <p stylle="color:rgb(224, 13, 154)"> </p>
        ```
    - If you wanna give multiple properties, then they are separated by semicolon `;`.
        ```html
        <p stylle="color:rgb(224, 13, 154) ; font-size:18px"> </p>
        ```
    - output in the HTML, copy the below & check it out : 
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>CSS Introduction</title>
    </head>
    <body>
        <!--Say we have a paragraph-->
        <p style="color:rgb(224, 13, 154) ; font-size: 18px;">
            The Audi R8 is a mid-engine, 2-seater sports car, which uses Audi's trademark quattro permanent all-wheel drive system.<br>
            It was introduced by the German car manufacturer Audi AG in 2006.Production ended in the first quarter of 2024. <br>
            <br>
        </p>
        <p style="color:rgb(1, 54, 54) ; font-size: 20px;">
            The car is exclusively designed, developed, and manufactured by Audi AG's private subsidiary company manufacturing high performance automotive parts<br>
            Audi Sport GmbH (formerly quattro GmbH), and was inspired by the Lamborghini Gallardo albeit the second generation is built using the Huracán platform.<br>
            The fundamental construction of the R8 is based on the Audi Space Frame,and uses an aluminium monocoque which is built using space frame principles.<br>
        </p>
        
    </body>
    </html>
    ```

### 2. Block & Inline elements. (Day 18)

- So far when we use default tags like `h1`, they have their default property. 
- `Block Element` : 
    - In simple words, block elements creates a block which is that it takes up complete space, when you give 2 block elements in the same line you will notice in the browswer they take up separate lines. Eg : 
        - eg : 
        ```html
        <h1>Heading 1</h1>
        <h1>Heading 1</h1>
        ```
- `Inline Element` : 
    - Inline element does not create a new line.
    - Eg : 
    ```html
    <a>Click Here</a>    
    <a>Click Here</a>
    ```
- This is important to know because, in the future when we make layouts we need to know which is `block element` & which is a `inline element`

- We use `<div>` to make block elements & `<spam>` to make inline elements.