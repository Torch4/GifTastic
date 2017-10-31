# GifTastic

This app utilizes the Giphy API to access specific gifs. There are are a pre-set of buttons, each button grabs gifs based on the label of the button. If you'd like to add a button, you can by typing in your subject material and pressing submit. Each time you press the button it will generate 10 gifs based on that topic.

Overview

This app uses the GIPHY API to make a dynamic web page that populates with gifs.

How It Works

An array of strings saved to a variable called topics holds the initial search queries displayed as buttons on the page.

For each string in the array, a button is appended to the topics-display in the HTML.

When the user clicks on a button, an AJAX request to the GIPHY API retrieves the top 10 search results using the specified query.

GIPHY parameters used:
q (search query)
limit ( =10 )
rating ( PG )
Search results will initially be displayed as a static image (still source URL provided by GIPHY API). When the user clicks one of the still GIPHY images, the gif's src attribute is replaced with the animated source URL. If the user clicks the gif again, it returns to its still state..

Rating is displayed under each gif (PG, G, so on).

This data is provided by the GIPHY API.
A search form on the page takes the value from user input and adds it into the topics array (the buttons are re-rendered on the page when a new search term is added).

If the user attempts to submit an empty string or a string consisting only of whitespace, or if the user enters a term that is already included in the topics array, the page will alert the user ( Enter a new search term! ).
