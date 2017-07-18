# Controller Testing Gifs

A React on Rails project, created as part of a code-along lesson for the Launch Academy Rails curriculum. Students are encouraged to start thinking about how to thoroughly test applications that use a Rails back end and a React front end. Using Rspec to tests to test API endpoints, and then using Enzyme tests to test the React front end functionality, is the way we achieve this.

The app has a simple index page that displays all of the gifs in the database, and a React form where a user can submit a new gif with a name and a url. 

Students should test that the `GET#index` method:
* Returns the status 200
* Returns the type `application/json`
* Returns the number of items we expect
* Returns the expected JSON output

Students should test that the `POST#create` method:
* Creates a new instance of the `Gif` class.
* Returns the status 200
* Returns the content type `application/json`
* Returns a Hash of one object, not an array of many objects
* Returns the json we expect for the gif we posted.

## Setup
To get set up, run the following:

```no-highlight
  bundle
  rake db:create
  rake db:migrate
  rake db:seed
```

In a separate terminal tab, run:

```
  yarn
  yarn start
```

Then navigate to `localhost:3000`.

## Testing
You can run the controller tests by running `rspec`. Feel free to add model tests in `spec/models` to test the `Gif` class!

React/Jasmine/Enzyme testing is all set up! Run `yarn test` to run the example tests, or add tests to the `react/test` directory.
