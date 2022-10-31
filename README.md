# Hi! Montero here.
I'm a full stack engineer, marketer and former startup founder. I enjoy working with startups, helping them build products and internal tools. I am a self-taught developer and everything I know I have learned by building interesting B2B products. I am always open to work opportunities, so feel free to drop me an email in case you want to connect.

## Tech Stack
![tech-skills](https://user-images.githubusercontent.com/13739454/124678033-5a305400-de87-11eb-9276-c52253de7202.png)

- Javascript
- Python
- React & React Native
- Redux
- Node
- Postgres
- Django

## Featured Projects

## [NubeBar](https://github.com/donmonty/api-nubebar-django)
NubeBar is a mobile app that helps bars and restaurants manage their alcohol inventory in order to avoid theft and boost revenue. For most bars and restaurants alcohol sales represent 40% or more of total sales. Alcohol also has the highest margins and is the most valuable inventory. Despite this, most businesses manage their alcohol inventory using manual, time-consuming methods that make inventory control a big challenge. NubeBar solves this problem.

Thanks to NubeBar's bar code and QR scanner, bar managers can do full inventory counts in a matter of minutes, not hours. And with the help of NubeBar's analytics module, bar managers have a detailed view of their inventory over time. NubeBar highlights any differences between reported sales and actual alcohol consumption, allowing bar managers to uncover theft or malpractice at the bottle level with milliliter precision.

I built the app using React Native, Django and Postgres. I like to think that I worked as a full stack entrepreneur because I did everything: customer research and development, sales, UI design, frontend engineering, backend engineering and customer support.

- [Check out the backend repo (Django).](https://github.com/donmonty/api-nubebar-django)
- [Check out the mobile app repo (React Native).](https://github.com/donmonty/frontend-nubebar)
- [Watch a quick video of the app here](https://www.notion.so/NubeBar-e54b9344880e4a34a0aa655b94def266#a8fd30fa783f478cb3316b7f2561f001)


![nubebar-banner](https://user-images.githubusercontent.com/13739454/198862782-abba9349-52ab-48ab-afc9-701d11a7f9ce.png)

## [Analytics Dashboard](https://www.loom.com/share/35250740c3a54e36a0080be862ea0ebb)
Dots is a YC-backed company that helps manage Discord and Slack communities at scale, providing custom onboarding flows and analytics. I helped them build an analytics dashboard where community managers could check out critical data such as active users, popular threads, user retention and community growth over time.

The frontend is built with React, Ant Design and Recharts. The dashboard fetches data direclty from the Postgres database thanks to Supabase and its RPC functionality which executes complex queries in the form of stored procedures.

[Watch a quick video of the dashboard here](https://www.loom.com/share/35250740c3a54e36a0080be862ea0ebb)

<img width="1417" alt="Screen Shot 2022-04-10 at 19 26 00" src="https://user-images.githubusercontent.com/13739454/198871787-12aaa2b9-e381-4320-bd77-a7576e8649c4.png">
<img width="1429" alt="Screen Shot 2022-04-10 at 19 19 17" src="https://user-images.githubusercontent.com/13739454/198871793-859beba0-02b0-49c2-9113-30f8c8187eb8.png">

## [Multi Step Form](https://github.com/donmonty/multistep-form)
Culina Health is a NY startup that connects people who want to eat healthier with registered dietitians around the US. They needed to build a complex multi step form that could be reused later to build other complex forms inside the company.  

Building convoluted forms is not a trivial thing so I used Formik, a battle-tested library that simplifies the process and provides great flexibility thanks to its React Context-based approach and its integration with Yup to handle complex validations.

Features:
- Accomodates any number of steps/screens
- Follows different routes depending on user input
- Built with React Router v6, Formik and Typescript
- Form validation handled with Yup
- Styling done with Tailwind CSS
- Handles image uploads with React Dropzone
- Stripe integration

[Check out the repository here](https://github.com/donmonty/multistep-form)

![steps-1](https://user-images.githubusercontent.com/13739454/198870740-a4fec6b4-95f9-4055-a6f4-4ae6063d16df.png)
![steps-2](https://user-images.githubusercontent.com/13739454/198870755-f7cb3d99-b358-4310-81e6-712f31a85b55.png)


## [Parking Lot Search App](https://airgarage-client.herokuapp.com/)
An app that connects to the Yelp API and searches for the worst rated parking spaces in America. Built for [Air Garage](https://www.airgarage.com/), a YC startup that automates the operation of parking lots and enables churches and businesses to rent out parking to drivers on demand. 
Although the app looks quite simple, it deals with a couple of technical challenges under the hood. First, it's not possible to make requests to the Yelp API using a regular frontend client. Second, the Yelp API does not provide any functionality to search and sort businesses by reverse ratings. To solve these challenges the app includes a backend that handles requests to the Yelp API and performs a series of tricks to sort parking lots from worst rated to best, maintaining a nice set of paginated results. 

Built with:
- React
- Styled components
- Node / Express

- [Check out the deployed app](https://airgarage-client.herokuapp.com/)

![parking-lot-search-app](https://user-images.githubusercontent.com/13739454/130372381-6ec733a0-2235-4824-9b78-ed817b6740e7.png)

