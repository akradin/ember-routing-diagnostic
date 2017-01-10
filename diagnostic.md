# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    Inside the emper application router is where you find our routes. So, this
    is where we would find `/lists/` or the path to go to a single list. Inside
    an ember route would be what the view state would actuall change to
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```sh
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```html
    {{#link-to 'boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first one is a nested route, so you get to it from the `products` page.
    I am pretty sure both will get you to the same place, but the starting place
    is different.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    Not sure what is meant by referencing the value. If you mean how do we get
    to the data about `/movies/123` other than manually typing it into the url
    window then I think you just an action inside the model that says to show
    the component that contains movie data.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    We use the model it correlates with.
    ```
