# News API Documentation

This document provides comprehensive information about various news API responses and their data structures.

---

## 1. News.org API

**API Key:** `8c5fe3e56cd047e3a4e29f2665729b13`

### Response Structure

The API returns an array of news articles with the following structure:

```json
[
  {
    "source": {
      "id": "techcrunch",
      "name": "TechCrunch"
    },
    "author": "Lauren Forristal",
    "title": "Bye-bye bots: Altera's game-playing AI agents get backing from Eric Schmidt | TechCrunch",
    "description": "Autonomous, AI-based players are coming to a gaming experience near you...",
    "url": "https://techcrunch.com/2024/05/08/bye-bye-bots-alteras-game-playing-ai-agents-get-backing-from-eric-schmidt/",
    "urlToImage": "https://techcrunch.com/wp-content/uploads/2024/05/Minecraft-keyart.jpg?resize=1200,720",
    "publishedAt": "2024-05-08T15:14:57Z",
    "content": "Autonomous, AI-based players are coming to a gaming experience near you... [+6416 chars]"
  }
]
```

### Key Fields

- **source**: Contains source ID and name
- **author**: Article author name
- **title**: Article headline
- **description**: Brief description of the article
- **url**: Full article URL
- **urlToImage**: Featured image URL
- **publishedAt**: Publication timestamp (ISO 8601 format)
- **content**: Article content preview with character count

---

## 2. Real-Time News Data API

### Response Structure

```json
{
  "status": "OK",
  "request_id": "4d00ec74-841f-47ce-bebc-515dfd0b6797",
  "data": [
    {
      "article_id": "CBMixAFBVV95cUxPbHVQakhxMUFxbjhFUkVYVWthQ0V0LXRFWUc4YUVVaDg0V0I0RGNGMHFSakJZM1h5aUZCMDhKSjRYUlZxV1BBOFRsT3BxbXh4T09HUkJ0TGRiZFpYdzJhS0pJX2pjOXRqNWdkTHhDRWtGSEpJYm9fZjhiU1pJbC11aUF2dk11QjJTMzhiTDZ0UUVPLWQzSWVLa1pjejY5WFNQeHZXblZiSjhNMWdLWEF4ekNvcFdXaUpWNmZUTFBXdzlibFF2",
      "title": "Inside Oregon's rise as a college football blue blood",
      "link": "https://www.espn.com/college-football/story/_/id/47516141/...",
      "snippet": "In a sport that often tethers itself to history and tradition...",
      "photo_url": "https://a.espncdn.com/photo/2026/0108/r1598085_1296x729_16-9.jpg",
      "thumbnail_url": "https://news.google.com/api/attachments/...",
      "published_datetime_utc": "2026-01-09T12:15:00.000Z",
      "authors": ["Paolo Uggetti"],
      "source_url": "https://www.espn.com",
      "source_name": "ESPN",
      "source_logo_url": "https://encrypted-tbn2.gstatic.com/faviconV2?...",
      "source_favicon_url": "https://encrypted-tbn2.gstatic.com/faviconV2?...",
      "source_publication_id": "CAAqIQgKIhtDQklTRGdnTWFnb0tDR1Z6Y0c0dVkyOXRLQUFQAQ",
      "related_topics": [
        {
          "topic_id": "CAAqKAgKIiJDQkFTRXdvTkwyY3ZNVEZzWjNKb2NUUm9aeElDWlc0b0FBUAE",
          "topic_name": "Paolo Uggetti"
        }
      ]
    }
  ]
}
```

### Key Features

- **Status**: Request status indicator
- **Request ID**: Unique identifier for the request
- **Article ID**: Unique article identifier
- **Media**: Multiple image formats (photo, thumbnail)
- **Source Details**: Comprehensive source information including logos and favicons
- **Related Topics**: Associated topics with IDs and names
- **Authors Array**: Multiple authors supported

---

## 3. Google News API

### Response Structure with Subnews

```json
{
  "timestamp": "1767965460000",
  "title": "U.S. payrolls rose 50,000 in December, less than expected...",
  "snippet": "Nonfarm payrolls rose a seasonally adjusted 50,000 in December...",
  "images": {
    "thumbnail": "https://news.google.com/api/attachments/...",
    "thumbnailProxied": "https://img.devisty.store/newsimage/..."
  },
  "subnews": [
    {
      "timestamp": "1767981660000",
      "title": "The US economy added just 50,000 jobs last month...",
      "snippet": "Economists were expecting 55000 jobs to have been added...",
      "images": {
        "thumbnail": "https://news.google.com/api/attachments/...",
        "thumbnailProxied": "https://img.devisty.store/newsimage/..."
      },
      "newsUrl": "https://www.cnn.com/business/live-news/...",
      "publisher": "CNN"
    }
  ],
  "hasSubnews": true,
  "newsUrl": "https://www.cnbc.com/2026/01/09/jobs-report-december-2025.html",
  "publisher": "CNBC"
}
```

### Key Features

- **Timestamp**: Unix timestamp in milliseconds
- **Images**: Both original and proxied thumbnail URLs
- **Subnews**: Related articles from different sources
- **hasSubnews**: Boolean flag indicating related articles
- **Multiple Publishers**: Coverage from various news outlets (CNN, NYT, NPR, NBC, Bloomberg, Reuters)

---

## 4. NewsNow API

### Response Structure

```json
{
  "title": "Iran's Supreme Leader Vows to 'Not Back Down' as Protests Swell",
  "top_image": "https://static01.nyt.com/images/2026/01/09/multimedia/...",
  "images": [
    "https://static01.nyt.com/images/2026/01/09/multimedia/..."
  ],
  "videos": [],
  "url": "https://www.nytimes.com/2026/01/09/world/middleeast/...",
  "date": "Fri, 09 Jan 2026 10:27:59 GMT",
  "short_description": "Iran's Supreme Leader Vows to 'Not Back Down'...",
  "text": "Iran's supreme leader vowed on Friday that the government...",
  "publisher": {
    "href": "https://www.nytimes.com",
    "title": "The New York Times"
  }
}
```

### Key Features

- **Top Image**: Featured article image
- **Images Array**: All images from the article
- **Videos Array**: Video content (if available)
- **Date**: Human-readable date format
- **Full Text**: Complete article text content
- **Publisher Object**: Structured publisher information with URL and name

---

## 5. NewsData.io API

**API Key:** `pub_cbb1452397a14d6da2430bb3c64feeaa`

### Response Structure

```json
{
  "article_id": "fa6e5c4597f51b927b8e169c658fbbed",
  "link": "https://en.prnasia.com/story/518232-0.shtml",
  "title": "InfiMotion Technology Showcases Leading E-Drive Solutions at CES 2026",
  "description": "LAS VEGAS, Jan. 9, 2026 /PRNewswire/ -- As the premier global tech event...",
  "content": "ONLY AVAILABLE IN PAID PLANS",
  "keywords": ["tds", "pdt", "cpr", "aut", "trn", "ecp", "cse"],
  "creator": null,
  "language": "english",
  "country": [
    "yemen", "afghanistan", "india", "singapore", "saudi arabia",
    "united arab emirates", "china", "taiwan", "pakistan", "brunei",
    "syria", "bhutan", "turkey", "armenia", "qatar", "philippines",
    "hong kong", "romania", "laos", "timor-leste", "bangladesh",
    "vietnam", "azerbaijan", "uzbekistan", "turkmenistan", "macau",
    "bahrain", "tajikistan"
  ],
  "category": ["technology", "top"],
  "datatype": "news",
  "pubDate": "2026-01-09 06:34:00",
  "pubDateTZ": "UTC",
  "fetched_at": "2026-01-09 07:00:38",
  "image_url": "https://mma.prnasia.com/media2/2858068/2.jpg?p=medium600",
  "video_url": null,
  "source_id": "en_prnasisa",
  "source_name": "Pr Newswire Apac",
  "source_priority": 4111305,
  "source_url": "https://en.prnasia.com",
  "source_icon": "https://n.bytvi.com/en_prnasisa.png",
  "sentiment": "ONLY AVAILABLE IN PROFESSIONAL AND CORPORATE PLANS",
  "sentiment_stats": "ONLY AVAILABLE IN PROFESSIONAL AND CORPORATE PLANS",
  "ai_tag": "ONLY AVAILABLE IN PROFESSIONAL AND CORPORATE PLANS",
  "ai_region": "ONLY AVAILABLE IN CORPORATE PLANS",
  "ai_org": "ONLY AVAILABLE IN CORPORATE PLANS",
  "ai_summary": "ONLY AVAILABLE IN PAID PLANS",
  "duplicate": true
}
```

### Key Features

- **Keywords Array**: Article categorization tags
- **Multi-Country Support**: Articles tagged with multiple countries
- **Categories**: Multiple category classification
- **Timezone Information**: Publication timezone specified
- **Fetched Timestamp**: When the article was retrieved
- **Source Priority**: Numerical priority value
- **Source Icon**: Publisher favicon/icon URL
- **Advanced Features**: Sentiment analysis, AI tagging, and summaries (paid plans)
- **Duplicate Flag**: Indicates if content is duplicated

### Premium Features (Paid Plans Only)

- Full article content
- Sentiment analysis
- Sentiment statistics
- AI-generated tags
- AI region detection
- AI organization extraction
- AI-generated summaries

---

## API Comparison

| Feature | News.org | Real-Time News | Google News | NewsNow | NewsData.io |
|---------|----------|----------------|-------------|---------|-------------|
| Images | ✅ | ✅ | ✅ | ✅ | ✅ |
| Videos | ❌ | ❌ | ❌ | ✅ | ✅ |
| Full Text | Partial | ❌ | ❌ | ✅ | Paid |
| Related Articles | ❌ | ✅ | ✅ | ❌ | ❌ |
| Source Logos | ❌ | ✅ | ❌ | ❌ | ✅ |
| Keywords | ❌ | ❌ | ❌ | ❌ | ✅ |
| Multi-Country | ❌ | ❌ | ❌ | ❌ | ✅ |
| AI Features | ❌ | ❌ | ❌ | ❌ | Paid |
| Sentiment | ❌ | ❌ | ❌ | ❌ | Paid |

---

## Notes

- All timestamps are provided in different formats across APIs (ISO 8601, Unix milliseconds, GMT string)
- Image URLs vary in format and may include proxied versions
- Some features are restricted to paid tiers in certain APIs
- API keys should be kept secure and not exposed in client-side code