---
layout: post
title: Google analytics 
date: 2019-09-15 13:00:00 -0000
category: google-anakytics
---
# Setting up Google analytics tracking

## Adding filters

### Ghost spam

Ghost spam: Fake google analytics data sent by spammers without visiting your site.

Solution: Apply a valid hostname filter to only view traffic that actually hit your website. 

1. Create a "Filtered" view.

Get a list of website's valid hostnames.

2. In Analytics, onavigate to the Audience > Technology > Network, in the left side.
3. Change the table's primary dimension to [Hostname](https://analytics.google.com/analytics/web/#/report/visitors-network/a145383681w235426496p222538579/explorer-segmentExplorer.segmentId=analytics.hostname&explorer-table.plotKeys=%5B%5D).
4. In the Admin tab, return to the "Filtered" view
5. Click "Filters" in the View column.
6. Click on "Add Filter"
7. Filter Name: "Include Valid Hostnames"
8. Filter Type: "Custom"
7. Include > Filter Field: "Hostname"
8. In Filter Patterns, add regular expression, eg websitedomain.com|validhostname2|validhostname3
9. Click "Verify this filter"
7. Save

Visit https://carloseo.com/removing-google-analytics-spam/ for links to more robust checkers and examples.

Valid hostnames:
- websitedomain.com, blog.websitedomain.com
- Tools, eg YouTube, MailChimp
- Payment gateways - Shopify, booking systems
- Translation services - Google translate
- Mobile speed-up services - Google weblight

Hostnames to filter out
- Spam
- (Not set) hostname - usually spam
- Scraping sites - URL of the scraper
- Staging/dev environments, eg dev.websitedomain.com
- Internet archives - archive.org

## Other spam

Crawler spam uses a valid hostname and has to be filtered out using an expression that blocks all currently known crawler spam sources.

Some crawlers and bots get into GA by using fake languages which need to be filtered out by allowing in only language information that's structured properly.

The steps for filtering out these two types of filters are very similar to the hostname steps we jsut walked through.

Bots (scrapers, unwanted spiders)

1. In filtered views, click on View Settings 
2. Scroll down to Bot filtering.
3. Click box that says "Exclude all hits from known bots and spiders."
4. Save for all views except Unfiltered one.

Filter out unwanted ISP organizations and domains or networks.

Internal traffic

Add IP filters that block traffic from certain physical locations.
It isn't perfect but will help.
Filter out:
- Staff & offices
- Home offices of remote employees
- People who work on the website

Gather IP addresses

1. Google search for "my ip" from the physical locations you want to filter out.
2. List all IPs in a regex, eg: IP1|IP2|IP3
3. Filters > Add Filter
4. Filter name: Exclude Internal traffic (IP)
5. Filter Type: Custom
6. Exclude: Filter Field > IP Address

Caveats
- IP anonymization (last parts get changed to zeroes), eg 1.23.45.678 -> 1.23.45.0 (new GDPR reg requires)
- Dynamic IPs (some ISP use)
- Team works from multiple locations or frequently travel

Possible to more accurately filter internal traffic using a tag in Google Tag Manager + custom dimension in Google Analytics
Visit https://carloseo.com/removing-google-analytics-spam/ for steps 

For the Google analytics website, follow these instructions.<br />
<a href="https://support.google.com/analytics/answer/1151300?hl=en">https://support.google.com/analytics/answer/1151300?hl=en</a><br />
