# FormGenerator

## Hello:

This is a simple form generator jQuery plugin. It consists of three parts:
* The generator
* A data structure in JSON-Format
* A HTML templates

It work's with **Insert tags** like `{{name}}`:
| Name             | Tag             | Description       |
| ---------------- | :-------------: | ----------------: |
| tag              | {{tag}}         |                   |
| content          | {{content}}     |                   |
| name             | {{name}}        |                   |
| label            | {{label}}       |                   |
| type             | {{type}}        |                   |
| placeholder      | {{placeholder}} |                   |
| value            | {{value}}       |                   |
| min              | {{min     }}    |                   |
| max              | {{max     }}    |                   |
| step             | {{step    }}    |                   |
| pattern          | {{pattern}}     |                   |
| description      | {{description}} |                   |
| id               | {{id}}          |                   |
| classes          | {{classes}}     |                   |
| required         | {{required}}    |                   |
| tabindex         | {{tabindex}}    |                   |

## Usage
### Step 1:
Make an **empty form in the HTML-Code** of your page, select it with jQuery and start the function `formGenerator()`.

```html
<html>
  ...
  <form id="generated"></form>
  ...
</html>
```
```javascript
  $("#generated").formGenerator();
```
### Step 2:
Create a **JSON-File** like this:
```json
{
  "formFields": [
    {
      "tag": "",
      "content": "",
      "name": "",
      "label": "",
      "type": "",
      "placeholder": "",
      "value": "",
      "min": "",
      "max": "",
      "step": "",
      "pattern": "",
      "description": "",
      "id": "",
      "classes": "",
      "required": "",
      "tabindex": ""
    },
    ...
  ]
}
```
Each entry in the formFields array aggregates a form field.

### Step 3:
Create the **HTML template** with the insert tags like this:
```html 
  <div class="{{classes}}"> 
    <label for="{{id}}">{{label}}</label>
    <{{tag}} name="{{name}}" type="{{type}}" placeholder="{{placeholder}}" value="{{value}}" min="{{min}}" max="{{max}}" step="{{step}}" pattern="{{pattern}}" id="{{id}} tabindex="{{tabindex}}" {{required}}">{{content}}</{{tag}}>
    <input>
    <span>{{description}}</span>
  </div>
```

