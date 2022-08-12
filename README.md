# Full-stack Interview Practical

## Instructions

We've set up this new Laravel project to act as the back-end. A "products" table *migration* and Product *model* have been added already.

Please refer to [https://laravel.com/docs/9.x/installation](https://laravel.com/docs/9.x/installation) for more details on setting up a Laravel project. If you're stuck, feel free to also let us know, and we'll help you out!

Please clone this repository, and perform the tasks below.

## Notes

- You can perform the tasks in any order.
- Use VueJS v3's composition API, and use NPM to install packages.
- Please make the layout look respectable (you can use CDNs to bring in 3rd party CSS frameworks if you like - Tailwind is a bonus).
- Feel free to add any other niceties for the *user experience*.
- ***Please commit your changes and send us a .zip copy (including the .git directory).***



## Front-end

- Create a basic form for adding a new product. Include an input field &amp; submit button. A product needs a name and a field for tags.
- In the tags field, the user can enter tag-names separated by commas. The new product will be linked to these tags.
- When submitted, save the new product to the database via an API call.
- List all products below the form, including their tags, via an API call.
- Have a search field that filters the listed entries.
- New products should appear below the input form after submitting.



## Back-end

- Create a new Tag model, and add the relevant relationships to and from the Product (many-to-many).
- Create migrations for Tags and a pivot table to link them to the Products.
- Add Web routing:
    - To load the home page initially.
- Add API routing:
    - To retrieve a list of products.
    - To save a new product.
    - To delete a product.
- When saving a new product:
    - Please add validation to make sure the product's name is not empty, and is unique.
    - Take the tags string and split it by commas. Create a tag for each save it:
        - But only if it's unique.
        - Link the product to each one (whether the tags were new or existed from before).
