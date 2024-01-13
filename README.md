[https://apify.com/epctex/similarweb-scraper?fpr=yhdrb](https://apify.com/epctex/similarweb-scraper?fpr=yhdrb)

# Actor - Similarweb Scraper

## Similarweb scraper

The most comprehensive Similarweb Scraper you will ever find. Obtain data on website popularity and receive it in formats such as JSON, XML, CSV, Excel, or an HTML table. Each scrape allows you to gather the subsequent details:

-   Information on the company
-   Metrics including total visits, average pages viewed, average time spent, and rate of visitors leaving quickly
-   Rankings based on popularity (worldwide/by nation/by category)
-   Origins of web traffic (like advertisements, direct links, search engines, social media, and more)
-   Spread across social media platforms
-   Rival websites
-   Technologies implemented
-   Demographic breakdown by age and gender
-   Trending subjects and websites for users
-   Leading visitor countries

## Bugs, fixes, updates, and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/similarweb-scraper/issues).


## Input Parameters

The input of this scraper should be JSON containing the list of pages on Similarweb that should be visited. Required fields are:

- `websites`: (Required) (Array) Domains or Similarweb full URLs that you want to retrieve the results from right away!

- `proxy`: (Required) (Proxy Object) Proxy configuration.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Compute Unit Consumption

The actor is optimized to run blazing fast and scrape as many items as possible. Therefore, it forefronts all the detailed requests. If the actor doesn't block very often it'll scrape 100 websites in 2 minutes with ~0.02-0.05 compute units. (depending on proxy and number of retries).

### Similarweb Scraper Input example

```json
{
  "websites": [
    "apify.com",
    "https://www.similarweb.com/website/example.com"
  ],
  "disableAnalytics": true,
  "proxy": {
    "useApifyProxy": true
  }
}

```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with a failure state and output an explanation of what is wrong.

## Similarweb Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any language (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Similarweb actor.

## Scraped Similarweb Properties

The structure of each item in Similarweb looks like this:

### Item Detail

```json
{
	"url": "https://www.similarweb.com/website/example.com",
	"name": "example.com",
	"description": "",
	"icon": "https://site-images.similarcdn.com/image?url=example.com&t=2&s=1&h=b63fbdb6c1a27c3f1467398b04fb81fcac694d85223c8a8eb2ca7c3e276b4af8",
	"previewDesktop": "https://site-images.similarcdn.com/image?url=example.com&t=1&s=1&h=b63fbdb6c1a27c3f1467398b04fb81fcac694d85223c8a8eb2ca7c3e276b4af8",
	"previewMobile": "https://site-images.similarcdn.com/image?url=example.com&t=4&s=1&h=b63fbdb6c1a27c3f1467398b04fb81fcac694d85223c8a8eb2ca7c3e276b4af8",
	"totalVisits": 2731009,
	"bounceRate": 0.6584328504024405,
	"pagesPerVisit": 2.1271126903721043,
	"avgVisitDuration": "00:01:10",
	"companyName": "example.com",
	"companyYearFounded": 2020,
	"companyEmployeesMin": 11,
	"companyEmployeesMax": 50,
	"companyAnnualRevenueMin": 5000000,
	"companyAnnualRevenueMax": 10000000,
	"companyHeadquarterCountryCode": "US",
	"companyHeadquarterCity": "Poway",
	"categoryId": "computers_electronics_and_technology/programming_and_developer_software",
	"globalRank": 27325,
	"countryRank": 24029,
	"categoryRank": 494,
	"organicTraffic": 0.02037535305716658,
	"paidTraffic": 0.00013297517471535874,
	"socialNetworkDistribution": [
		{
			"name": "Facebook",
			"visitsShare": 0.3255293008801001,
			"icon": "https://site-images.similarcdn.com/image?url=facebook.com&t=2&s=1&h=be773d6b77aa3d59b6a671c5c27ad729b1ae77400e89776e2f749cce6b926c4b"
		},
		{
			"name": "Reddit",
			"visitsShare": 0.20677069669874004,
			"icon": "https://site-images.similarcdn.com/image?url=reddit.com&t=2&s=1&h=66f2412047e0362ec60d5583d4b186511a8e859446bb112c60d22968facae906"
		}
	],
	"topReferrals": [
		{
			"domain": "sainstore.com.cn",
			"icon": "https://site-images.similarcdn.com/image?url=sainstore.com.cn&t=2&s=1&h=6599e599a77a07a671b445f6dbcc0dcb642ed742b73da654a8f249cd14cd34e2",
			"visitsShare": 0.039163300136706325,
			"isLocked": false
		},
	],
	"topIncomingCategories": [
		{
			"category": "Computers_Electronics_and_Technology/Programming_and_Developer_Software",
			"visitsShare": 0.20976287943264638
		}
	],
	"topOutgoingSites": [
		{
			"domain": "bing.com",
			"icon": "https://site-images.similarcdn.com/image?url=bing.com&t=2&s=1&h=a37ae326ae78ba2da30e9c8da030e84e07d4c76c5452c239f85c9050781ffde8",
			"visitsShare": 0.15244198374460416,
			"isLocked": false
		}
	],
	"trafficSources": {
		"directVisitsShare": 0.7987929429397509,
		"referralVisitsShare": 0.14399020951353203,
		"organicSearchVisitsShare": 0.02037535305716658,
		"paidSearchVisitsShare": 0.00013297517471535874,
		"socialNetworksVisitsShare": 0.012302031511970067,
		"mailVisitsShare": 0.00922292962838403,
		"adsVisitsShare": 0.015183558174481039
	},
	"adsSource": [
		{
			"domain": "spy.house",
			"icon": "https://site-images.similarcdn.com/image?url=spy.house&t=2&s=1&h=726c13ae2747aa7e6eaa3b875da2e2f1fa14bfd4c535bd7a649c7cc417785d7b",
			"visitsShare": 0.024292125814544006,
			"isLocked": false
		}
	],
	"topKeywords": [
		{
			"name": "example.com",
			"estimatedValue": 2310.074622306198,
			"volume": 8810
		},
	],
	"topSimilarityCompetitors": [
		{
			"domain": "imagemagick.org",
			"icon": "https://site-images.similarcdn.com/image?url=imagemagick.org&t=2&s=1&h=4acde3cf8fb1d14a87ca92846d2233fb2ff498afed6faa2520f19e65309e4fd3",
			"visitsTotalCount": 313828,
			"categoryId": "computers_electronics_and_technology/programming_and_developer_software",
			"categoryRank": 4116,
			"affinity": 1,
			"isDataFromGa": false
		}
	],
	"technologies": [
		{
			"categoryId": "payment_and_currencies",
			"topTechName": "PayPal",
			"topTechIconUrl": "https://s3.amazonaws.com/s3-static-us-east-1.similarweb.com/technographics/id=1146",
			"technologiesTotalCount": 21
		}
	],
	"globalRankHistory": [
		{
			"date": "2023-07-01T00:00:00+00:00",
			"rank": 27111
		},
		{
			"date": "2023-08-01T00:00:00+00:00",
			"rank": 23239
		}
	],
	"countryRankCompetitors": [
		{
			"rank": 24027,
			"domain": "beautyrest.com",
			"icon": "https://site-images.similarcdn.com/image?url=beautyrest.com&t=2&s=1&h=8b7053f2087658d99913b631de5c97b9083682ee9fc4b4bfe4a20e40ef093cbd"
		}
	],
	"countryRankHistory": [
		{
			"date": "2023-07-01T00:00:00+00:00",
			"rank": 19812
		}
	],
	"categoryRankCompetitors": [
		{
			"rank": 492,
			"domain": "getintopc.com",
			"icon": "https://site-images.similarcdn.com/image?url=getintopc.com&t=2&s=1&h=27eff1e0f77ac735d5db39957bb5b137f482a949bea4dcf5b83ff0ca2a8087a6"
		}
	],
	"categoryRankHistory": [
		{
			"date": "2023-07-01T00:00:00+00:00",
			"rank": 407
		},
		{
			"date": "2023-08-01T00:00:00+00:00",
			"rank": 402
		},
		{
			"date": "2023-09-01T00:00:00+00:00",
			"rank": 494
		}
	],
	"globalRankCompetitors": [
		{
			"rank": 27323,
			"domain": "soccerbet.rs",
			"icon": "https://site-images.similarcdn.com/image?url=soccerbet.rs&t=2&s=1&h=6b63bac9019d26763bf796676857925f149df5806baaaf5ff4c92e2860fb3676"
		}
	],
	"ageDistribution": [
		{
			"minAge": 25,
			"maxAge": 34,
			"value": 0.34934147381902564
		}
	],
	"topInterestedWebsites": [
		{
			"domain": "iana.org",
			"icon": "https://site-images.similarcdn.com/image?url=iana.org&t=2&s=1&h=8dc33e2b49124d93e7fdb59eb700c2f1535c5e1a10905e508efc65ca6880c622"
		}
	],
	"topInterestedTopics": [
		"google",
		"search",
		"news",
		"internet",
		"community"
	],
	"topInterestedCategories": [
		"computers_electronics_and_technology/computers_electronics_and_technology",
		"computers_electronics_and_technology/programming_and_developer_software",
		"adult",
		"computers_electronics_and_technology/file_sharing_and_hosting",
		"computers_electronics_and_technology/social_networks_and_online_communities"
	],
	"topCountries": [
		{
			"countryAlpha2Code": "US",
			"countryUrlCode": "united-states",
			"visitsShare": 0.17667851173150384,
			"visitsShareChange": -0.02132305166773374
		}
	],
	"globalRankPrev": 23239,
	"globalRankChange": -4086,
	"categoryRankPrev": 402,
	"categoryRankChange": -92,
	"countryRankPrev": 19798,
	"countryRankChange": -4231
}
```

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that are available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
