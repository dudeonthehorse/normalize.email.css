# normalize.email.css

CSS resets for HTML emails

It's just a little css library for best default email compatibility. You can use it with your favourite email framework and self-coded templates.

## What does it do?

- Preserves useful defaults for most email clients
- Makes native platform font styling
- Corrects some popular bugs
- Explains what code does using comments

Please let me know if comments not informative and must be detailed

## Contents

- normalize.css - must be inlined to your newsletter in production
- extra.css - must be placed between `<style>` tags in `<head>` of your newsletter in production
- outlook.css - must be placed between `<style>` tags with conditional comment in `<head>` of your newsletter in production. Check out example.html to learn correct code

## Example

``` html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- normalize.css contents must be inlined to newsletter -->
    <link href="normalize.css" rel="stylesheet">
    <link href="extra.css" rel="stylesheet">
    <style>
        /* Put extra.css contents here */
    </style>
    <!--[if (gte mso 9)|(IE)]>
        <link href="outlook.css" rel="stylesheet">
        /* Put outlook.css contents here */
    <![endif]-->
    <!-- Left title element empty to prevent viewing this text in subject line on Android 4 email clients -->
    <title></title>
</head>

<body class="body">
    <div class="webkit">
        <!-- An example of bulletproof container with limited row length -->
        <table width="100%" border="0" cellpadding="0" cellspacing="0">
            <tr>
                <!-- Add here this element -->
                <!-- <th></th> -->
                <!-- to align container to center -->
                <th width="500" align="left">
                    <!-- Content here -->
                    <!-- You can use any HTML code which you prefer -->
                </th>
                <th></th>
            </tr>
        </table>
    </div>
</body>

</html>

```

## Conclusion

CSS Normalization gives developers a safe starting point at which to know styles are the same across browsers. For projects where an element inventory is not looked after regularly or, perhaps if there are very very few styles, CSS Normalize can guarantee normality of elements before any custom styling is done
