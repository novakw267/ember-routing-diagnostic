# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    <!-- The router is the file that the file path for each view state and creates the name for the URL to reach those states. The route file define the actions available on that view state and defines what data will display upon loading that view. -->
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    <!-- ember generate route campus/boston -->
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    <!-- Link-to is what we use to define a connection between two different files.
    For example in the campus file {{link-to "boston"}}Boston{{/link-to}} would take you to the Boston page. {{link-to "campus"}}Return the main page{{/link-to}} if i put this on the boston page it would take me back to campus.-->
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
    <!-- The first one is defining the nested routes in two lines versus defining the whole path and ID in one line. I am honestly not sure what another major difference is, my only guess would be that maybe the second one would be more limited in how it can be referenced? -->
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    <!-- model(params) {
    return this.get('store').findRecord('list', params.movie_id);
  } I am not sure if you were asking for something like this. I know this was what we used to call the List ID in the list route in order for the create and destroy functions to work correctly. ,-->
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    <!-- I assume this is done through defining what the model is, and creating a link to the functions definied in the route. This way we can call the action on the data avaiable.  -->
    ```
