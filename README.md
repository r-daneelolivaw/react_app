# React App for Drupal 8

React app boilerplate for progressive decoupling.
The demo loads articles from a JSON API endpoint.

## Getting started

This boilerplate is based on the method adopted by the
[React Comments](https://www.drupal.org/project/react_comments) module.

### React

1. cd in _/path/to/module/react_app/js/src_.
2. Install dependencies with `yarn install`.
3. Copy the _constants/.env.example.js_ file to _constants/.env.local.js_ 
and set there your Drupal 8 site url.
It will be used while debugging React as a standalone app for JSON API requests.
4. Edit _App.js_ and your components.
5. Run `yarn start` to start the React development server 
and test your app outside of Drupal.
6. Run `php build.php` to bundle the dist js and css. 
that are referenced by _react_app.libraries.yml_.

### Drupal

Generate some articles. Install devel_generate then:

`drush genc 20 --types=article`

Install JSON API 

```
composer require drupal/jsonapi
drush en jsonapi
```

Head to _http://drupal8site/react-app/app_ to access the embedded React app.
