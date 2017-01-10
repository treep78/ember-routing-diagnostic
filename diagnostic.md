# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    An ember app router interperets a url to determine which ember route to display. An ember route acts like a view determining which content will be displayed when is routed to.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember generate route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{link-to 'campus.boston' campus}}Link{{/link-to}}
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
      The first route specifically specifies that the product route is contained within the products foler. In THe second example this is not necessarily the case. The use of a function in the first exmple means that product is automatically under products where as in the second example they are on the same level.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
      Possibly as movie.id or this.id
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
      with this.data.
    ```
