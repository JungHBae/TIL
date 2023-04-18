## General css  

**shadow related, hover transitions**  

```css
.shadow {
  box-shadow: 0 2px 4px rgba(0,0,0,0.15),
              0 4px 8px rgba(0,0,0,0.15),
              0 8px 16px rgba(0,0,0,0.15),
              0 16px 32px rgba(0,0,0,0.15);
  transition: all 0.3s ease-in-out;
}

.shadow:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.2),
              0 8px 16px rgba(0,0,0,0.2),
              0 16px 32px rgba(0,0,0,0.2),
              0 32px 64px rgba(0,0,0,0.2);
}
``` 
**Jumping Scrollbar**  
html { margin-left: calc(100vw - 100%); }  
  
## Scss  
**Import**
common.scss > style.scss, can pass variables

> @import ""

**Variables**  

```css
$something: #125121

div {
  color: $something;
}
```  

**Nesting**  

```scss
something{
  width: 100px;
  height: 100px;
  
  &:hover{
    color: white
  }
}
```

## Validation

number to string >  

```javascript
const num = 1234567.89;
const options = { style: 'currency', currency: 'USD', minimumFractionDigits: 2 };
const str = num.toLocaleString('en-US', options);
console.log(str); // "$1,234,567.89"
```  
