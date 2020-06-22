# Frontend code challenge

## Cryptocurrency Single Page App

For the Bondify code challenge we want you to create a crypto overview and search application. If you’re not familiar with crypto currencies have a look at https://coinmarketcap.com/.
You are going to build the following pages:

- Overview page with the 25 highest market cap coins
- A page showing the coins pairs per exhange
- Lastly a detail page of the coin pair showing its details
- Search box in the overview page that resets the list with the search results
  You will be using React, Typescript and Apollo Client.
  As a convenience we have setup a repository and configured the Apollo Client for you, so that you can get right to the code. The API that you will be using is from bloktap.io. The GraphiQl explorer can be accessed via this link https://api.blocktap.io/graphiql.
  This example query will shows you all the data that you will be needing:

````query PageAssets {
assets(sort: [
{ marketCapRank: ASC } ], page: {limit: 25}) {
id
assetName
assetSymbol
marketCap
markets {
marketSymbol
baseSymbol
exchangeSymbol
ticker {
lastPrice
highPrice
lowPrice
percentChange
}
}
}
}```

What we expect to see are the following:

- Knowledge of routing and navigation
- ES6 and React Hooks
- Typescript typing
- Mobile first responsive implementation of the pages
- Search
  You may use any library that makes your life easier, but we expect you to create the UI-components by yourself. The use of Material-UI or any other component library is not allowed. So the use of StyledComponents is allowed. We will not judge you on pixel perfectness, but on how you approach the responsive and mobile first design.
  Bonus
- Theme toggle for dark mode
  We expect you to spend 6-8 hours to complete this challenge, it is a representation of the daily work load at Bondify. Your countdown starts when you fork the code from our repository and stops when you commit and send us an email when you’re finished. We will then evaluate your work and get back to you.
````
