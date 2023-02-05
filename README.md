# Project Proposal: Kareem DaCosta

## Project Purpose

My project will be for a startup called Sustainable Sister. I will be building a website that aims to be the all-in-one online fashion shopping hub. Our primary feature will be a search engine that allows users to easily search across multiple brands while personalizing results. We are slated to release an early version of the website and app this Spring. We will then expand to additional features beyond searching to transform the search engine into a fashion hub. I can’t say more due to an NDA, but this is an overview of what we hope to accomplish.

## Goals and Objectives

**Base Goal:** A populated database for the website. A fully designed home page and product-list page (but not necessarily linking to the database, instead using sample data).
**Stretch Goal 1:** Backend endpoints that link the website to the database and enable searching using various filters.
**Stretch Goal 2:** User authentication to allow for more personalization. Greater customization to transition the website from merely searching into more of a “hub.”

Since I will be developing the website this semester, it will be too early to measure success by any quantifiable user-based metric, such as user retention, user count, etc. I will instead measure success based on how much progress was made towards the website’s completion, how many features were added, and the scope of the website (how many stores it is able to search across). I will also measure success based on how efficient the server is, especially when populating the database.

## Method

The website will be created using a React.js frontend with (most likely) a Node.js/Express.js backend. The database management system I will use is still under consideration. Version control will be done through git/Github. The database will be populated with a python script.
Note: I may collaborate with other software engineers if Sustainable Sister recruits more web developers; however, as of now, I will be working on this website by myself.

An **ideal timeline** that will enable completion of both stretch goals is as follows:
End of February: Finish home page, populate database, finish preliminary search page
End of March: Finalize search page, finish Stretch Goal #1
End of April: Finish Stretch Goal #2
_Note:_ Stretch Goal #2 is very ambitious and encompasses a lot of smaller pieces, so while it is unlikely that I will be able to complete it, I hope to make some progress towards it.

The estimated cost of this project is $0 while in development. I intend to spend approximately 8-10 hours a week developing this website. Resources include:
Markup : - **Nabihah Ahmad**, the CEO of Sustainable Sister - **Jake Torres**, another software engineer at Sustainable Sister who is currently working on the mobile app but could provide some aid if needed - **Stack Overflow** - **Youtube/Blog** tutorials such as [this one](https://towardsdatascience.com/web-scraping-of-10-online-shops-in-30-minutes-with-python-and-scrapy-a7f66e42446d?gi=835eca195ca1)
My Own Experience interning as a web developer at Meta last summer where I learned React.js and Node.js/Express.js

## Examples

I have worked on a few projects in React.js and Node.js/Express.js, including my personal portfolio and Dungeon Delver, a website I made last summer.

The website I will be coding will be similar to [lyst.com](https://www.lyst.com/), which raised at a valuation of $700 million in 2021, but my website aims to have more features than lyst.

## Background/Research

I decided to use React.js for the frontend and Node.js/Express.js for the backend for a few reasons:
Markup : - I already had prior experience using these frameworks - React.js is extremely flexible and I find it easy to use once the initial learning curve is overcome. Node.js/Express.js is also similarly very easy to set up. - Since both frameworks use JavaScript, teaching other people how to contribute would be easier since they would only have to learn one language, not multiple. Despite React.js and Node.js/Express.js having very different syntaxes, the underlying language is the same, which makes them easier to pick up with one another.

### Why React over Angular?

https://kinsta.com/blog/angular-vs-react/
Markup : - Angular’s strengths include its detailed documentation and ongoing support by Google. It also is built on TypeScript, which makes it easier to identify errors. - React.js’s strengths are that it is extremely lightweight and has many third-party libraries. Additionally, it focuses on render speed, which will make the website load faster.
https://www.freecodecamp.org/news/angular-vs-react-what-to-choose-for-your-app-2/
Markup : - Angular doesn’t require additional libraries, but it is difficult to learn. When it comes to expansion, since Sustainable Sister is made of college students, any incoming developers would most likely not have much exposure to either React.js or Angular. Since React.js is easier to learn, it would make more sense from a growth standpoint. - React’s one-way data binding (data flows from parents in the DOM to children, but not the other way around) makes it fast, and the inflexibility this structure provides can be offset through state management systems like Redux or Recoil. - CreateReactApp makes it very easy to set up and start working in a React.js app.

### Why Node.js/Express.js over Django?

https://www.monocubed.com/blog/django-vs-express/
Markup : - Express is much faster than Django. Since we are building a webstore, speed on the backend is important since it will be having to query and process through a large database of fashion items. Leaving users waiting a long time for requests to be processed will probably result in many users leaving the website before they view the items. - Express.js is less complex than Django, which as stated above, will make it easy for newer college developers to pick up. Since it is written in JavaScript, Express.js will be easier for students with web development experience to learn. Express.js is also very scalable, which will make it easy to add new features over time. - Django is used for full-stack development, but since I am using React.js for the frontend, I don’t need Django’s frontend capabilities. Thus, Express.js makes more sense for my project. - React.js with Express.js is a very common, fast, and powerful combination to create a full stack application. For the reasons listed above, this is what we will be using.

#### But Django is Still Necessary; When?

In the future, we will most likely have a machine learning algorithm, which would be easier to do in Python (Django). Down the line, I will look into using pickle in Express and then unpacking with tensorflow.js as seen here, but for now my plan is to use a Django backend (Using Django REST Framework) for anything that requires machine learning and an express.js backend for other features. Like I said, I will try to use pickle with Express.js so that I only have one backend to work with, but I may end up having to use django (or flask!)

### Why Azure?

Markup : - The three main options I was looking at were Amazon Web Services, Google’s Firebase, and Microsoft’s Azure. - Azure provides integration with Neo4J as seen here. This will make it much easier to create machine learning models in the future. This, combined with Microsoft’s new investments in AI (OpenAI investment, etc.) make it the best choice for a web app that relies heavily on machine learning. While I won’t need it as much now, future features will most likely include machine learning (recommendation systems, etc) which will be easiest to implement on Azure.
References (for future ML functionality)
[Machine Learning with Django](https://www.deploymachinelearning.com/)
[Recommendation System in Python: LightFM](https://towardsdatascience.com/recommendation-system-in-python-lightfm-61c85010ce17)
[https://github.com/lyst/lightfm/issues/207](https://github.com/lyst/lightfm/issues/207)
[An Introduction to Recommender Systems Using LightFM in Azure ML](https://python.plainenglish.io/introduction-to-recommender-systems-using-lightfm-in-azure-ml-e86feaff6ac4)
[Recommendation System in Python: LightFM](https://towardsdatascience.com/recommendation-system-in-python-lightfm-61c85010ce17)
[Real-time Machine Learning For Recommendations](https://eugeneyan.com/writing/real-time-recommendations/)
[https://github.com/lyst/lightfm/issues/425](https://github.com/lyst/lightfm/issues/425)
[https://github.com/lyst/lightfm/issues/210](https://github.com/lyst/lightfm/issues/210)
[How I would explain building "LightFM Hybrid Recommenders" to a 5-year old!](https://towardsdatascience.com/how-i-would-explain-building-lightfm-hybrid-recommenders-to-a-5-year-old-b6ee18571309)
