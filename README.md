# Testing TodoMVC using playwright

## Description

-   Testing Website - https://todomvc.com/examples/vanillajs/
-   Testing framework - https://playwright.dev

Testing will be done inside a devContainer using VSCode to avoid platform specific setup

-   Docker - https://www.docker.com/
-   Visual Studio Code Dev Containers extension - https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers
- Chrome extension - https://chromewebstore.google.com/detail/playwright-crx/jambeljnbnfbkcpnoiaedcabbgmnnlcd
## Set up

Create a `json` file in:

```json
#./devcontainer/devcontainer.json
{
    "name": "Playwright Testing",
    "image": "mcr.microsoft.com/playwright:v1.40.0-jammy",
    "forwardPorts": [9323],
    "postCreateCommand": "npm install"
  }

```

```js
test.describe('New Todo', () => {
	test('should allow me to add todo items', undefined)
	test('should clear text input field when an item is added', undefined)
	test('should append new items to the bottom of the list', undefined)
	test('should show #main and #footer when items added', undefined)
})

test.describe('Mark all as completed', () => {
	test('should allow me to mark all items as completed', undefined)
	test('should allow me to clear the complete state of all items', undefined)
	test(
		'complete all checkbox should update state when items are completed / cleared',
		undefined
	)
})

test.describe('Item', () => {
	test('should allow me to mark items as complete', undefined)
	test('should allow me to un-mark items as complete', undefined)
	test('should allow me to edit an item', undefined)
})

test.describe('Editing', () => {
	test('should hide other controls when editing', undefined)
	test('should save edits on blur', undefined)
	test('should trim entered text', undefined)
	test('should remove the item if an empty text string was entered', async ({
		page,
	}) => {})
	test('should cancel edits on escape', undefined)
})

test.describe('Counter', () => {
	test('should display the current number of todo items', undefined)
})

test.describe('Clear completed button', () => {
	test('should display the correct text', undefined)
	test('should remove completed items when clicked', undefined)
	test(
		'should be hidden when there are no items that are completed',
		undefined
	)
})

test.describe('Persistence', () => {
	test('should persist its data', undefined)
})

test.describe('Routing', () => {
	test('should allow me to display active items', undefined)
	test('should respect the back button', undefined)
	test('should allow me to display all items', undefined)
	test('should highlight the currently applied filter', undefined)
})
```

// test commit
