## Setting up my Git Repository

1. Instructions to set up my local folder to GitHub.

    ``` BASH

    echo "# colmaracademy" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/Liyyy9/colmaracademy.git
    git remote -v
    git push -u origin main
    
    ```
2. In the event that the URL repo is set wrongly, use the following command to set the correct url:

    ```

    git remote set-url origin https://github.com/thinktinker/colmaracademy.git
    git remote -v
    git push

    ```

## CSS Explanation

### 1. RESETTING AT THE START OF THE CSS CODE
``` CSS
* {
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
}
```
#### Explanation: 

- * Selector: Targets every element on the page.

- margin: 0px: Sets the space outside of every element to zero, removing default margins that browsers might apply.

- padding: 0px: Sets the space inside every element to zero, removing default padding.

- box-sizing: border-box: Ensures that the width and height you set for an element include its padding and border. This means if you set an element to be 100px wide, it will be 100px wide including any padding and borders, making layout and sizing more predictable.

So, this CSS rule is useful for creating a consistent starting point for styling by eliminating extra space and making size calculations straightforward.


### 2. MEDIA QUERY

#### Media Query 
```
@media screen and (max-width: 40rem) {
  /* CSS rules here */
}
```
What it does: This applies the styles inside it only when the screen width is 40rem (about 640px) or smaller.

#### Inside the Media Query

#### .mobile-nav:
```
.mobile-nav {
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 4rem;
}
```
Makes .mobile-nav visible: It uses Flexbox to center items and distribute space evenly. It also sets a height of 4rem for this element.


#### .desktop-nav:
```
.desktop-nav {
  display: none;
}
```

Hides .desktop-nav: It removes .desktop-nav from view when the screen is 40rem or less.

#### Summary
When the screen is small (640px or less), the .mobile-nav becomes visible and is styled to fit well, while the .desktop-nav is hidden.