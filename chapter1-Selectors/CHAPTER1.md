# Chapter 1 Selectors 

## Understanding selectors is key to write maintainable, scalable CSS

## TYPES OF SELECTORS
### selectors can be grouped int four basic types:

- 1 - Simple
- 2 - Compound
- 3 - Combinator
- 4 - Complex

### 1 Simples Selectors:

- The universal selector ``` * ```, that help you with the global styles of your page

- The element selector like ``` p, h1, h2 ```, that invoque the classes directly

- The pseudo-elements selectors such as ``` ::first-letter ```

- Attributes selectors such as ``` [hidden] ```

- The class selectors such ``` .message-error ``` 

- And ID selector as ``` #masterhead ```  also fall into this category.


## 2 - Compound Selectors

- Such as ``` p:last-child , message.error ``` , are a sequence of simple selector that reflect a set os simultaneous conditions to meet when applying rules to an element. In other words,  ``` message.error ``` will match with ``` <div class="message error"> and not with <div class="message"> or <div class="error"> ```

## 3 - Combinator

- Combinator Selectors express a relationship between elements. there are four: 
    - the descendent combinator, as in artilce ``` article p ```

    - the child combinator (>), as in  ``` .sidebar > h2 ```

    - the adjacent sibling combinator (+), as in ``` ul + p ```

    - the geral sibling combinator (~), as in ``` p ~ figure ```

## 4 - Complex

- Lastly, there are complex selector, Complex selector consist of one or more compound selectors separated by a combinator. 

    - The selector ``` ul:not(.quare) > a[rel=external] ``` is an example of a complex selector.

### Selector can be grouped int what's known as a <em>selector list</em> by separating them with a comma. selector lists apply styles to elements that match any of the selectors in the list for example:

```
article, div{ padding: 5px;}
``` 

### add 20 pixels of padding to both elements.

<br>

## Conclusion:

### Knowing what kind of selectors you're working with will help you gasp one of the more confusing aspects of CSS ```specificity ``` keeping specificity low increases the reusability of your CSS rules. 

### A selector such ``` #menu > .pop-open ``` means that you can use the ``` .pop-open ``` pattern when it's a direct descendent of ``` #menu ``` , even if there are similar interactions elsewhere in your ptoject.

<br>
<br>

## 💻 Well, now that you know whats is as selector and how many types exits, go to <a hrref="./style.css">Styles.css</a>  to find the code examples,  have fun.