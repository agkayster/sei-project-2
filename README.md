## Project 2: NEWSAPI (A React application that consumes public API and aggregates news headlines)

A react project

## Overview

NEWS API is a news aggregator collating online news from different online papers across various countries. It was a pair coding project built in 2 days, and was both the first aggregating site we built, and our first real-world type practice with REACT. Launch on Check out the GitHub Repo.

## Brief

1. The second project is to **build a React application** that consumes a **public API**.

2. Your app must:
​
* **Consume a public API** – this could be anything but it must make sense for your project.
* **Have several components** - At least one classical and one functional.
* **The app should include a router** - with several "pages".
* **Include wireframes** - that you designed before building the app.
* Have **semantically clean HTML** - you make sure you write HTML that makes structural sense rather than thinking about how it might look, which is the job of CSS.

3. **Be deployed online** and accessible to the public.

## Technologies Used

1. HTML5 with HTML5 audio
2. CSS3 with animation (Style.scss)
3. JavaScript (ES6)
4. React
5. Git 5 GitHub
6. Google Fonts
7. bulma
8. webpack

## Approach Taken

* Started by setting up the HTML file with the id of root.
* The next step was to set up the app.js file which would bring together the codes on the rest of the files.
* We then created the index page which we used to fetch data from a news aggregating API and then filter for various news headlines across the world by inputing their country codes. Once the news headlines came in, we then displayed them on Card structure by setting up our Card.js.
* On the Index.js, we proceeded to add our filter, search and sort functions which would allow users on the app search news companies name, filter for different countries news and sort by latest news. In our index.js, we also created a timer that would refresh the news on the app via an axios get request anytime there was fresh news around the world on any of the news headlines we were aggregating and this would upload it directly to our app.
* We then designed our show page, here you could read more about any particular news you might be interested in by clicking on the particular card which has the news you want to know more about.
* If you wanted to go to the original website where the news we aggregated generated from, we designed a link that would take you directly to the site but on a different web page so you do not have to leave our web app site.
* Once we were done with the show.js page, we then proceeded to build our Home.js page, in doing this we designed a landing page using Bulma. We also designed our Hero container on the landing page with our custom made news aggregator logo and brand name. Our home page also contains a section where the latest news on any headline appears there. This way our users get to read the latest news across the world immediately they get to our home page.
* Our next step after the home page was to develop our Footer, which we did with some ease even though it wasn't as elaborate as we should have made it but it was our first try and I think it came off well and in our footer we proceeded to recognise the site where we received the API key for our project from.
* Our last step was to develop our Navbar where you have the button links for all the pages on the app and we designed a 📡 satellite icon as a clickable lick to our home page.
* Once we got all our pages, Footer and Navbar set up, we then went to the app.js page to add all the routes to as to ensure a smooth flow across the functions in the app, we also imported all the components to the app.js component.

### CSS :

We also had to research for proper professional CSS styling for the type of app we were building.


### Functionality

### Search, Sort and Filtering
* How would users be able to search for a particular headline, or filter for the latest news or sort headlines by Alphabetical order? We had to write a search, sort and filter code in our Index.js component which would allow users to carry out the above.

* We were also able to write a code that would send in the different country codes to the componentDidMount function, which would be triggered by a handleCountry event listener, which would get the latest news across various news headlines per country.

### Search, Sort and Filter code:

The code below was one of my contributions to the project.

```JavaScript
{
  (
<div className="field">
  <input placeholder="search" className="input" onChange={this.handleSearch}/>
</div>
</div>
<div className="column">
<div className="field">
  <div className="select is-fullwidth">
    <select onChange={this.handleSort}>
      <option value="source.name|asc">Name A-Z</option>
      <option value="source.name|desc">Name Z-A</option>
      <option value="publishedAt|asc">News Latest</option>
      <option value="publishedAt|desc">News Oldest</option>
    </select>
  </div>
</div>
</div>
<div className="column">
<div className="field">
  <div className="select is-fullwidth">
    <select onChange={this.handleCountry}>
      <option value="gb">United Kingdom</option>
      <option value="us">United States of America</option>
      <option value="ng">Nigeria</option>
      <option value="it">Italy</option>
      <option value="ru">Russia</option>
      <option value="pl">Poland</option>
      <option value="co">Columbia</option>
      <option value="fr">France</option>
    </select>
  </div>
)
}
```

### Linking our latest news to Home page code:

The code below was one of my contributions to the project.

```JavaScript
<Link to={{
  pathname: '/article',//A link to the pathname article, which carries the news from state
  state: news
}}>
  <Card
    name={news.source.name}
    title={news.title}
    description={news.description}
    image={news.urlToImage}

  />
</Link>
```


### Screen Shots
![image](https://user-images.githubusercontent.com/41432574/65363798-b4eeb200-dc05-11e9-8ef8-70a3db649c4d.png)

![image](https://user-images.githubusercontent.com/41432574/65363884-1f075700-dc06-11e9-9b31-1d384075d198.png)

### Final Products

https://agkayster.github.io/sei-project-2/#/

https://www.linkedin.com/in/ejike-chiboka-pmp

## Bugs
Below is a list of some of the known bugs within the game:

* Fresh News update for other countries apart from GB - We noticed that the news update for other countries does not update as fast as that for the Great Britain and this cause the app to break from time to time.

## Winners and Blockers:

* One of the challenges we faced was trying to link the latest news across the various headlines to our home/landing page section designed for latest news.

* My biggest win so far was the amount of confidence I gained from working with React and building this App.I got the opportunity to apply my new learnings in a real-world project and achieved more than I thought I could on my own, while helping me to understand fully everything we have been taught so far.

## Future Content
We would like to add fresh news update from other countries to the landing page of our web application.


## What we learned
Major learning points:
* Creation of code branches using Git and GitHub
* Pair coding using only one laptop
* Good communication essential for handling the above
* CSS Styling with Bulma as a first time
* Learning when and how to use lodash
* Implementing handleSort, handleSearch, handleCountry, componentDidMount, componentWillUnmount and componentDidUpdate functions in JavaScript.
* Using the bind method in state.
