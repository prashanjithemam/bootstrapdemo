# Rows

>  We use rows to create horizontal groups of columns. Rows must be placed within a ‘container’ or ‘container-fluid’ for proper alignment and padding.

Example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Bootstrap Example</title>
	<meta charset="utf-8">
	<meta name="viewport"
		content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href=
"https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
	<script src=
"https://ajax.googleapis.com/ajax/libs/jquery/3.4.0/jquery.min.js">
	</script>
	<script src=
"https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js">
	</script>
	<script src=
"https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js">
	</script>
</head>
<body>
	<header>
		<div class="container">
			<h1 style="color: green"> Rows Example</h1>
			<strong>
				An Example 
			</strong>
		</div>
	</header>
	<div class="container">
		<div class="row">
			<div class="bg bg-primary w-100">
				First row
			</div>
		</div>
		<div class="row">
			<div class="bg bg-success w-100">
				Second row
			</div>
		</div>
		<div class="row">
			<div class="bg bg-primary w-100">
				Third row
			</div>
		</div>
		<div class="row">
			<div class="bg bg-success w-100">
				Fourth row
			</div>
		</div>
		<div class="row">
			<div class="bg bg-primary w-100">
				Fifth row
			</div>
		</div>
	</div>
</body>
</html>
```

## Output
![row_example]()
