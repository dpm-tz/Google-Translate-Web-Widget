<p>This is a simple website that supports multiple languages using Google Translate.</p>
        <h6>To use the <b>Google Translate Web Widget</b> for free, you can embed the widget on your website to enable automatic translation of your entire site into various languages. Here's a step-by-step guide on how to integrate the widget<br><br><br>

<strong>1. Generate the Google Translate Widget Code</strong><br>
Google provides a simple code snippet that you can embed into your HTML file to enable the translation widget.<br><br>

Follow these steps:<br>

1. Visit the [Google Translate Website Widget page](https://translate.google.com/manager/website/).<br>
2. Sign in with your Google account (if you're not already signed in).<br>
3. Once logged in, you’ll be prompted to add a website.<br>
        <ol>
   - Enter your website URL.<br>
   - Choose the original language of your site (e.g., English).<br>
   - Select the languages you want to offer for translation.<br>
        </ol><br><br>
4. Google will then generate a code snippet for you to place in your website's HTML.<br><br>

2. Embed the Widget in Your HTML<br>

Once you have the code snippet, embed it into your website. Typically, you'll want to place it in the `<body>` section of your HTML, ideally somewhere near the top of your page.<br>

<br><br>

HTML Example with Google Translate Widget:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website with Google Translate</title>
</head>
<body>

    <!-- Google Translate Element -->
    <div id="google_translate_element"></div>

    <!-- Your website content -->
    <h1>Welcome to My Website</h1>
    <p>This is a simple website that supports multiple languages using Google Translate.</p>

    <!-- Google Translate Script -->
    <script type="text/javascript">
        function googleTranslateElementInit() {
            new google.translate.TranslateElement({
                pageLanguage: 'en',
                includedLanguages: 'fr,sw,es,de', // Add the language codes you want
                layout: google.translate.TranslateElement.InlineLayout.SIMPLE
            }, 'google_translate_element');
        }
    </script>

    <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>

</body>
</html>
```

Explanation:<br>
1. Google Translate Element: <br>
   - The `<div id="google_translate_element"></div>` is where the translation dropdown will appear.<br><br>
   
2. Script Initialization: <br>
   - The `googleTranslateElementInit` function initializes the Google Translate element, specifying the default page language (`en` for English) and the additional languages you want to support. You can customize the languages in the `includedLanguages` parameter (for example, `fr` for French, `sw` for Swahili, `es` for Spanish, `de` for German).<br><br>
   
3. Script Source: <br>
   - The `translate_a/element.js?cb=googleTranslateElementInit` script dynamically loads the Google Translate API and activates it on your page.<br><br>

3. Customize the Language Selection
In the `includedLanguages` section, you can specify the languages you want to offer by adding their respective language codes. For example:
- `en` = English
- `fr` = French
- `sw` = Swahili
- `es` = Spanish
- `de` = German

If you want to allow all languages, you can remove the `includedLanguages` field to show the full dropdown list.

### 4. **Styling the Widget**
You can style the widget to match your website’s design. Here’s a basic CSS example to style the dropdown:

```css
/* Style the Google Translate dropdown */
#google_translate_element {
    margin: 20px;
}

.goog-te-banner-frame {
    display: none !important;
}

.goog-logo-link {
    display: none !important;
}

.goog-te-gadget {
    font-size: 14px;
    font-family: Arial, sans-serif;
}
```

5. Testing Your Website<br>
Once you've embedded the widget, open your website in a browser and you should see the Google Translate dropdown at the top of the page. When users select a different language from the dropdown, Google Translate will automatically translate the content of your site.

Limitations:<br>
- Quality of Translation: Machine translation may not always be perfect, so it may require review for critical content.<br>
- SEO: Google Translate doesn’t impact the actual text on your website in the source code, so search engines will still index the original language.<br>
- Client-Side Translation: The widget works on the client-side, so the original content remains in your base language in the source code.<br>

Conclusion:<br>
The Google Translate Web Widget is an easy and free solution to enable translation on your website without dealing with API integrations. It’s useful for quickly making your site accessible to a global audience. However, for more control and professional-level translations, you may want to look into paid translation APIs.
    </h6></div>

    <!-- Google Translate Script -->
    <script type="text/javascript">
        function googleTranslateElementInit() {
            new google.translate.TranslateElement({
                pageLanguage: 'en',
                includedLanguages: 'fr,sw,es,de', // Add the language codes you want
                layout: google.translate.TranslateElement.InlineLayout.SIMPLE
            }, 'google_translate_element');
        }
    </script>

<!--     <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
 -->
    <!-- Custom Script for Menu -->
    <script>
        function toggleMenu() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.classList.toggle('active');
        }
    </script>
</body>
</html>
