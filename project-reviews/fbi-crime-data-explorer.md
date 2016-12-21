# FBI Crime Data Explorer
[Project repository](//github.com/18f/crime-data-explorer)

## General project

*What are you planning on building?*
A client based application that consumes the [Crime Data API](https://github.com/18f/crime-data-api) to visualize crime data from the FBI's UCR program.

*How will it work with other clients?*
It will consume the Crime Data API, but through a passthrough endpoint (`/api/*`) on the express server that powers the front end project. We want to use a passthrough endpoint so that we can secure our API key.

*Is there anything unique about the design of the product?*
Nothing too technically unique, though it is has no write functionality.

*How will the project be passed off after 18F has finished it?*
That is still being determined.

*Who are the users?*
We think of our users as the general public, as this is an open data project built on Federal data from the FBI.

*Are there analytics for the current users?*
The product most similar to the Crime Data Explorer is the [Crime in the US reports]() that have been published for quite a few years. There is basic web analytics for the reports and the [UCR program homepage](https://ucr.fbi.gov/) but we are hoping the Crime Data Explorer attracts a whole new cohort of users to the site.

## CSS

*Will a CSS methodology/framework be employed. example: BassCSS, Atomic CSS?*
We will mostly be using BassCSS and Atomic CSS, though we

What will the CSS class naming convention be. example BEM?

*Will the project use the US WD standards?*
As inspiration, but not as a direct dependency.

*Will there be a design system or pattern library?*
Yes, the style guide will live in [the 18f/crime-data-style repo](https://github.com/18f/crime-data-style).

*How will visual UI or style be tested?*
Unsure, what is the recommended method for 18F currently?

*Will there be a coding style guide? If so, will an existing style guide be used?*
Yes, using the 18F linting style guide based on AirBnb.

*How will a CSS linter be set up? When will it run? What happens when it fails?*
Our linter is set up to run with an `npm` command. We have CodeClimate set up for every pull request to lint the entire project and prevent a merge if it fails.

*Will you use a CSS processor such as Sass or PostCSS?*
Yes, both. We will mostly use Sass but we are also using `autoprefixer`.

*How will icons be done?*
We will determine this after we decide [which browsers we have to support](https://github.com/18F/crime-data-api/issues/207). Hopefully, we can use SVGs for any icons.

*How will images be done?*
Gzipped, but not sure what else beyond that.

## Javascript

*What will the backend be?*
This application will be served by an `express` server. The API that it consumes is a Python Flask app.

*Is there an API built for this?*
Yes, [18f/crime-data-api](https://github.com/18f/crime-data-api).

*Does the site need to work without Javascript?*
No, though we do want to have isomorophic rendering so that the initial loads work without JavaScript.

*Will a JavaScript framework be used?*
Yes, we are using `react` along with `redux` as the primary frameworks in the application.

*Can web components be leveraged?*
Theoretically, sure. We are using `react` so we'll be building our UI in components, though not standards compliant custom elements.

*What JS style guide will be used? Will there be modifications made to the base 18F styleguide setup?*
The 18F style guide will be used.

*How will a JS linter be set up? When will it run? What happens when it fails?*
Similarly to our CSS set up, our JS linter will be run with every pull request on CodeClimate.

*What tool will be used for dependency management?*
`npm`

*When and how will dependencies be upgraded?*
No formal or determined process for this exists right now.

## Build

*What is the build process?*
We use `webpack` to bundle/build our client side application. It is invoked with `npm run build`.

*How will JS files be sent to browser? Just one file? Multiple files?*
Just one file.

*Will you ever want to split up the JS files into multiple bundles?*
Perhaps, though for now we're sticking with a single bundle as it is easier to work with. We are watching the size of the resulting bundle to make sure it isn't too large.

*Will this be continuously deployed?*
Yes, it is deployed on every commit to `master` by [CircleCI](https://circleci.com/gh/18F/crime-data-explorer)

*What language dependencies? Ruby, Node, Python? Can we keep it to just 1?*
We split out the front end consumer and the API for this exact reason. The 18f/crime-data-explorer project will just require node.

*In what cases should the build fail?*

## Testing

Structure: integration / unit / functional, the mix between them, methodology

Decide when tests should be written, or coverage amount?

*How will it fit into code review process?*
Tests should accompany most features, and all that aren't strictly based in React components.

*How will JS unit tests be run?*
By CircleCI and with an `npm test` command.

*Will they require DOM? Will they test the DOM?*
Since we are using `react` and `redux` we should be able to minimize the amount of DOM testing we do need to do. However, since we do want to be able to test some of our components, we include `jsdom` in the testing environment.

## Devices

What browsers will be supported? This should likely be based on user analytics if any are available.

What is the usage percentage cut-off? For example, if (using analytics) there are 2% of users with IE6 will you support that browser?

What device sizes will the site support? What device sizes will be focused on?

Will it be mobile first? If not, why not?

How will accessibility be ensured? How will accessibility testing be done, if it is?

What accessibility standard does the site have to conform to?

## Performance

What metrics should be tracked? ie: page load, speed index, custom events, number of requests, total request size, etc.

When should performance be measured? ie: on live staging site, locally during test runs.

How should performance be measured? ie: with what tools

What should performance budgets for decided metrics be? ie: faster then 1000 for speed index, faster than 1s for certain custom event, total request size below 2mb.

How should performance metrics and budgets be incorporated into workflow? Going over a budget requires re-implementation, or issue.
