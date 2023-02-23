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

### Knowing what kind of selectors you're working with will help you gasp one of the more confusing aspects of CSS ```specificity ``` keeping specificity low increases the reusability of your CSS rules. 

### A selector such ``` #menu > .pop-open ``` means that you can use the ``` .pop-open ``` pattern when it's a direct descendent of ``` #menu ``` , even if there are similar interactions elsewhere in your ptoject.

### You can find all examples in:
    Attrbutes and Combinators Folder
<br>

# Pseudo-Classes and Pseudo-Elements

<br>

### Most of the new selector addedin CSS3 and CC4 are not attributes selectors at all. They're pseudo-classes and pseudo-atributes

### Though you've probably used pseudo-classes and pseudo-elements in your CSS, you not have thought about what they are or how they differ from each other.

## Pseudo-Classes

- Let us style objects based on information - such as their state - that's distinct from the documetn tree or that can't be expressed using simple selectors
- For example, an element can only have a hover or focus state once the user interacts with it.
- With the ```:hover``` and ``` :focus ``` pseudo-classes ,we can define styles or those state.
-Otherwise, we'd have to rely on scripting to add and remove class names

## Pseudo-Elements

- pseudo elements on the otehr hand, let us style elements that aren't directly present int hte document tree.
- HTML doesen't define a ``` firstletter ``` element, se we need another way to select it.
- The ``` ::firt-letter ``` pseudo-element gives us that capability

<br>

```
Beware of Universal Selection: 🤔

➡️  Using pseudo-classes and pseudo-elements without a simples selector is the equivalent them with the univeral selector.

➡️ For a selector such as:

:not([type=radio])

➡️ every element that lacks a type attribute adn value of radio will match including <html> and <body>

➡️ To prevent this, use 

:not()

➡️ as a part of a compound selector, such as with a class name or element as in:

p:not(.error)

➡️ In the same way, using class names, IDs and attributes selectors on their own applies them universally.

➡️ For example: .warning and [type=radio] are the same as:

*.warning and *[type=radio] 
```

### You can find all examples in the:
    Pseudo-Clases e Pseudo-Elements Folder