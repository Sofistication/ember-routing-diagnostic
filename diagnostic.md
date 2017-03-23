# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The Ember Application Router is in charge of mapping URLs to view states of the app. Ember Routes are used to define what model, actions, and probably other things we haven't covered are apllicable to the given view state of the app.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```sh
    ember generate route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus/boston'}}Some informative text about this link{{/link-to}}
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
    The first and most obvious difference between the two definitions is that the first one is nested and the other is not. Another difference is that because of the nesting or lack thereof, transitions might not work in the way we expect, as we saw yesterday.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```js
    someFunction([otherArgs,] params.movie_id)
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    {{model.insideBaconBraces}}
    ```
