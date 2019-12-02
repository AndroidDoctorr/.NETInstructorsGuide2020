## Example Form Lecture Code
### HTML
``` HTML
<!DOCTYPE html> <!-- Step 1 -->
<html lang="en">
<head>
	<title>Forms Example</title> <!-- Step 2 -->
</head>
<body>
	<form> <!-- Step 3 -->
		<div> <!-- Step 6 -->
			<input type="text" /> <!-- Step 4 -->
		</div>
		<div>
			<input type="password" /> <!-- Step 5 -->
		</div>
		<div>
			<button type="submit">Register</button> <!-- Step 7 -->
		</div>
	</form>
</body>
</html>
```

1. Scaffold HTML with **!** snippet
2. Change **title** tag to demonstrate updates in the browser.
3. Add **form** tag by itself and then show updated browser. What changed? Why don't we see anything new? Good opportunity to discuss container tags.
4. Add an **input** tag inside the form tag. Show the new changes.
5. Add a second **input** tag. Now that you have two tags, go ahead and add the **type** attributes to both tags.
6. Now that you have two input tags, add div tags around them to push them to separate lines.
7. Add a button tag and discuss how the submit type would submit the form's value if it had a place to send the information. In this case, it just "resets" the form because there is nothing set up to accept the data.