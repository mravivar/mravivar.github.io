
## vs code - copilot
- cmd + I : chat to copilot

- { and enter : to show suggestion  
- ctrl + enter : to show multiple suggestions on a new page  
- tab : to accept the suggestion  
- cmd + -> : to partially accept sugggestion  
- alt + ] : to show next suggestion  
- alt + [ : to show previous suggestion  

- enable or disable copilot : by clicking copilot icon at the botton right

- to create unit tests: select the code and press cmd + I and ask to write unit test for the function. preview and apply

## Different ways to use github copilot
1. open copilot chat and use @terminal and ask questions
2. write pull request summaries from github ui
3. generate commit messages from vs code 
4. get help in the (vscode) terminal with github copilot in the cli
    - brew install gh
5. Talk to your repositories on GitHub.com
    - select code snippet and ask copilot chat to 'explain' 
6. fix code inline
7. bulk close 1000+ github issues
8. generate documentation for your code
9. get help with error messages in your terminal
10. debug your github actions workflow

__________


## Markdown syntax
- to try and check markdown [https://dillinger.io/](https://dillinger.io/)

- internal link
  {% raw %}
  ```
  e.g.
  [Keyboard Shortcuts]({% link _posts/2024-01-23-keyboard-shortcuts.md %})
  ```
  {% endraw %}  

- external link
  {% raw %}
  ```
  syntax:
  [name](url)
  e.g.
  [localhost](http://localhost:4000)
  ```
  {% endraw %}
- images
  {% raw %}
  ```
  e.g.
  ![image](/assets/images/k8s-architecture.png)
  or
  ![k8s-architecture](/assets/images/k8s-architecture.png)
  or
  <img src="/assets/images/k8s-architecture.png" alt="">
  ```
  {% endraw %}

- table
  {% raw %}
  ```
  | Tables   |      Are      |  Cool |
  |----------|:-------------:|------:|
  | col 1 is |  left-aligned | $1600 |
  | col 2 is |    centered   |   $12 |
  | col 3 is | right-aligned |    $1 |
  ```
  {% endraw %}

  output:

  | Tables   |      Are      |  Cool |
  |----------|:-------------:|------:|
  | col 1 is |  left-aligned | $1600 |
  | col 2 is |    centered   |   $12 |
  | col 3 is | right-aligned |    $1 |









