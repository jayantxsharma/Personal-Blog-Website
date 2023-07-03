# Personal-Blog-WebsiteIt imports the required modules: express, body-parser, ejs, and mongoose.

It defines some static content for the home page (homeStartingContent), about page (aboutContent), and contact page (contactContent).

The Express application is created and assigned to the app variable.

The view engine is set to EJS using app.set('view engine', 'ejs'). This means that the application will use EJS templates to render HTML.

The application uses body-parser middleware to parse incoming request bodies.

The application serves static files from the "public" directory using express.static.

It connects to a MongoDB database using mongoose.connect.

A Mongoose schema is defined for blog posts with title and content fields.

A Mongoose model is created using the schema, named "Post".

The application defines a route for the home page ("/") that fetches all posts from the database and renders the "home" template, passing the fetched posts as data.

The application defines a route for the compose page ("/compose") that renders the "compose" template, which allows users to create new blog posts.

When a POST request is made to the "/compose" route, a new Post instance is created with the title and content from the request body. The new post is then saved to the database.

The application defines a route for individual blog post pages ("/posts/:postId") that fetches a specific post from the database based on the requested post ID and renders the "post" template, passing the post data.

The application defines routes for the about ("/about") and contact ("/contact") pages, which render the respective templates and pass the corresponding content.

The application starts listening on port 3000 and logs a message to the console when the server is started.

This code sets up a basic blogging platform where users can view existing blog posts, create new posts, and view individual post pages. The posts are stored in a MongoDB database using Mongoose.
