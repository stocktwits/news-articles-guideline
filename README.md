# news-articles-guideline

## RSS Feed Structure

The RSS feed follows the standard RSS 2.0 format with additional custom elements. Here's an overview of the XML structure:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0" 
     xmlns:atom="http://www.w3.org/2005/Atom"
     xmlns:content="http://purl.org/rss/1.0/modules/content/"
     xmlns:media="http://search.yahoo.com/mrss/"
     xmlns:snf="http://www.stocktwits.com/snf">
  <channel>
    <title>Stocktwits News Feed</title>
    <link>https://stocktwits.com/news-articles</link>
    <description>Latest news from Stocktwits</description>
    <language>en-us</language>
    <pubDate>Mon, 01 Jan 2023 12:00:00 -0500</pubDate>
    <copyright>Copyright 2023 Stocktwits</copyright>
    <snf:logo>
      <url>https://example.com/stocktwits-logo.png</url>
    </snf:logo>
    <snf:darkModeLogo>
      <url>https://example.com/stocktwits-logo-dark.png</url>
    </snf:darkModeLogo>
    <item>
      <title>Example Stocktwits Article</title>
      <link>https://stocktwits.com/news/category/subcategory/article-slug/12345</link>
      <guid>https://stocktwits.com/news/category/subcategory/article-slug/12345</guid>
      <description><![CDATA[Article summary...]]></description>
      <content:encoded><![CDATA[Full article content...]]></content:encoded>
      <pubDate>Mon, 01 Jan 2023 12:00:00 -0500</pubDate>
      <lastUpdate>Mon, 01 Jan 2023 14:30:00 -0500</lastUpdate>
      <isUpdated>true</isUpdated>
      <author>John Doe</author>
      <publisher>Stocktwits</publisher>
      <image>
        <url>https://example.com/article-image.jpg</url>
        <source>Stocktwits</source>
        <caption>Image caption</caption>
      </image>
      <media:thumbnail>https://example.com/article-image.jpg</media:thumbnail>
      <language>en</language>
      <symbol>AAPL</symbol>
      <symbol>GOOGL</symbol>
      <category>Technology</category>
      <subcategory>Software</subcategory>
      <tag>Earnings</tag>
      <tag>Market Analysis</tag>
    </item>
  </channel>
</rss>
```

### Channel Elements

- `<title>`: The title of the news feed
- `<link>`: URL to the Stocktwits news page
- `<description>`: A brief description of the feed
- `<language>`: The language of the feed (always "en-us")
- `<pubDate>`: The publication date of the feed
- `<copyright>`: Copyright information
- `<snf:logo>`: Stocktwits logo URL (custom element)
- `<snf:darkModeLogo>`: Stocktwits dark mode logo URL (custom element)

### Item Elements

Each `<item>` represents a news article with the following elements:

- `<title>`: The headline of the article
- `<link>`: The unique URL of the article
- `<guid>`: A unique identifier for the article (same as the link)
- `<description>`: A summary of the article (CDATA-encoded)
- `<content:encoded>`: The full content of the article (CDATA-encoded)
- `<pubDate>`: The publication date of the article
- `<lastUpdate>`: The last modification date of the article
- `<isUpdated>`: Boolean indicating if the article has been updated
- `<author>`: The name of the article's author
- `<publisher>`: Always set to "Stocktwits"
- `<image>`: Information about the article's featured image
  - `<url>`: URL of the image
  - `<source>`: Source of the image (always "Stocktwits")
  - `<caption>`: Caption for the image
- `<media:thumbnail>`: URL of the article's thumbnail image
- `<language>`: The language of the article (always "en")
- `<symbol>`: Stock symbols associated with the article (can appear multiple times)
- `<category>`: The main category of the article
- `<subcategory>`: The subcategory of the article
- `<tag>`: Tags associated with the article (can appear multiple times)

This structure provides a comprehensive representation of Stocktwits news articles in RSS format, including custom elements for Stocktwits-specific information.
