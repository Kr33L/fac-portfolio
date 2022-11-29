# HTTP

## 1. We can write code that executes asynchronously

```js
fetch(`${API}${KEY}&limit=18`)
  .then(getResponse)
  .then(getImages)
  .catch(catchErrors);
 ```

## 2. We can use callbacks to access values that aren’t available synchronously

```js
function getBreeds(data) {
  data.filter ((image) => { image?.url != null }) // not sure if this is necessary
  data.map ((breed) => {
      const option = document.createElement("option");
      option.value = breed.id;
      option.textContent = breed.name;
      breedSelector.appendChild(option);
    });
}
```

## 3. We can use promises to access values that aren’t available synchronously



## 4. We can use the fetch method to make HTTP requests and receive responses

```js
function getResponse(response) {
  if (!response.ok) throw new Error(response.status);
  console.log(response);
  return response.json();
}
```

## 5. We can configure the options argument of the fetch method to make GET and POST requests

To configure options argument of the fetch method:

```js
fetch(`${API}${KEY}&limit=18`, {
  method: 'GET', //GET, POST, PUT, DELETE
  })
  .then(getResponse)
  .then(getImages)
  .catch(catchErrors);
 ```

## 6. We can use the map array method to create a new array containing new values

```js
function getBreeds(data) {
  data.filter ((image) => { image?.url != null }) // not sure if this is necessary
  data.map ((breed) => {
      const option = document.createElement("option");
      option.value = breed.id;
      option.textContent = breed.name;
      breedSelector.appendChild(option);
    });
}
```

## 7. We can use the filter array method to create a new array with certain values removed

```js
data.filter ((image) => { image?.url != null })
```

## DOM
## 8. We can access DOM nodes using a variety of selectors

```js
const breedSelector = document.querySelector("#breed--selector");
const grid = document.querySelector("#grid");
```

## 9. We can add and remove DOM nodes to change the content on the page

```js
const option = document.createElement("option");
option.value = breed.id;
option.textContent = breed.name;
breedSelector.appendChild(option);
```

## 10. We can toggle the classes applied to DOM nodes to change their CSS properties

```js
img.classList.add("grid--image");
gridCell.classList.add("grid--item");
```

## Design

## 11. We can use consistent layout and spacing

```css
.grid {
  display: grid;
  grid-auto-flow: dense;
  justify-content: center;
  justify-items: center;
  grid-template-columns: repeat(auto-fit, minmax(150px, 300px));
  grid-template-rows: repeat(auto, 1fr);
  border-radius: 10px;
  min-width: 150px;
  margin: 10px;
}
```

## 12. We can follow a spacing guideline to give our app a consistent feel

## Developer Toolkit

## 13. We can debug client side JS in our web browser

## 14.We can use console.log() to help us debug our code

```js
if (!response.ok) {
    throw new Error(response.status);
  }
  console.log(response);
```
