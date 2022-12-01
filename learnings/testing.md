# Testing

## 1. We can test the functionality of our app

```js
test("addTask() should clear the input field", () => {
  addButton.click();
  const result = `"${input.value}"`;
  const expected = '""';
  equal(result, expected);
});
```

## 2. We can check that passing a given input into our tests returns the expected output

```js
const equal = (actual, expected, message) => {
  actual === expected
    ? console.info("Pass: " + (message || `Expected ${expected} and received ${actual}`))
    : console.error("Fail: " + (message || `Expected ${expected} but received ${actual} instead`));
};
```

## 3. We can write tests to mimic the behaviour of a user performing different actions

```js
test("completeTask() should move the task to the bottom of the list", () => {
  const completeButton = task.querySelector(".complete-button");
  completeButton.click();
  const result = taskList.lastChild.id;
  const expected = "task-1";
  equal(result, expected);
};
```

## JS

## 4. We can write testable, modular functions

```js
function addTask(task) {
	task = input.value;
	const listItem = createListItem(task);
	taskList.append(listItem);
	input.value = "";
}
```

## 5. We can write functions that add, remove or modify DOM nodes

```js
const deleteTask = (task) => task.remove();

const completeTask = (task) => {
  task.classList.toggle("completed");
  taskList.append(task);
};

const urgentTask = (task) => {
  task.classList.toggle("urgent");
  taskList.prepend(task);
};
```

## 6. We can apply event listeners to HTML form elements

```js
addButton.addEventListener("click", (e) => {
	e.preventDefault();
	input.value === "" ? input.focus() : addTask();
});
```

## 7. We can use scope to control what variables are accessible inside functions and blocks

```js
function buttonFactory({ classList, text, func }) {
  const button = document.createElement("button");

  // <- Assign id and text to the button ->
  button.innerText = text;
  button.classList.add(classList);

  // <- Execute function on the button's parent element ->
  button.addEventListener("click", (e) => func(e.target.parentElement));
  return button;
}
```

## Design

## 8. We can use CSS grid to create complex layouts

## 9. We can use CSS grid to make layouts that adapt to the viewport size
