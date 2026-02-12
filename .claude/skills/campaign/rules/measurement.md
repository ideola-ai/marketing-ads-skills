# Campaign Measurement & Analytics

## KPI Framework by Funnel Stage

### Top of Funnel (Awareness)
```
Primary KPIs:
- CPM (Cost per 1,000 impressions)
- Reach (Unique people reached)
- Impressions (Total views)
- Frequency (Average times seen)
- Video View Rate (% watched to completion)

Secondary KPIs:
- Brand lift (brand awareness surveys)
- Click-through rate (CTR)
- CPC (Cost per click)

Benchmarks:
- CPM: $5-20 (varies by platform/audience)
- Video View Rate: 20-40% (3-sec views)
- Frequency: 1.5-3 (sweet spot)
```

### Middle of Funnel (Consideration)
```
Primary KPIs:
- CTR (Click-through rate)
- CPC (Cost per click)
- Landing page views
- Time on site
- Pages per session
- Engagement rate

Secondary KPIs:
- Cost per landing page view
- Bounce rate
- Return visitors

Benchmarks:
- CTR: 0.5-1.5% (Meta), 0.3-1% (Display)
- CPC: $0.50-3.00 (varies widely)
- Landing page view rate: 60-80%
```

### Bottom of Funnel (Conversion)
```
Primary KPIs:
- Conversions (lead/sale)
- CPA (Cost per acquisition)
- ROAS (Return on ad spend)
- Conversion rate
- Revenue

Secondary KPIs:
- Cost per lead (CPL)
- Cost per sale
- Customer acquisition cost (CAC)
- Lifetime value (LTV)

Benchmarks:
- CPA: Varies by industry ($10-200+)
- ROAS: 2.0x-4.0x is good, 4.0x+ excellent
- Conversion rate: 1-3% (landing page dependent)
```

## Platform-Specific Metrics

### Meta Ads (Facebook + Instagram)
```
Key Metrics Dashboard:
- Amount Spent
- Impressions
- Reach
- CPM
- CPC
- CTR (all)
- Landing Page Views
- Leads / Purchases
- CPA / ROAS
- Frequency

Quality Metrics:
- Quality Ranking (below/above average)
- Conversion Rate Ranking
- Engagement Rate Ranking

Target Frequency Goals:
- Awareness: 1.5-2.5
- Consideration: 2-4
- Conversion: 3-5 (retargeting)
```

### TikTok Ads
```
Key Metrics Dashboard:
- Amount Spent
- Impressions
- CPM
- CPC (very low usually)
- CTR (2-6 seconds)
- Video plays (2s, 6s, 100%)
- Conversions
- CPA

TikTok-Specific:
- 2-second video view rate
- 6-second video view rate
- Video plays at 25%, 50%, 75%
- Watch time (total)
```

### Google Ads
```
Key Metrics Dashboard:
- Cost
- Impressions
- CTR
- CPC
- Conversion rate
- Cost per conversion
- Conversion value
- ROAS

Quality Score:
- Quality Score (1-10)
- Expected CTR
- Ad relevance
- Landing page experience

Target KPIs:
- CTR: 3-5% (Search), 0.5-1% (Display)
- Quality Score: 7+ is good
```

### LinkedIn Ads
```
Key Metrics Dashboard:
- Amount Spent
- Impressions
- CPM
- CPC (usually higher)
- CTR
- Leads / Conversions
- Open rate (Sponsored Messaging)
- Conversation rate (Conversation Ads)

Target KPIs:
- CPM: $30-100+ (expensive but quality)
- CTR: 0.3-0.8%
- CPC: $3-10+
- Lead open rate: 20-40%
```

## Attribution Models

### First-Click Attribution
```
Definition: Credit goes to first touchpoint

Use When:
- Brand awareness campaigns
- Long consideration cycles
- Understanding initial interest

Pros: Shows top-of-funnel effectiveness
Cons: Ignores nurturing efforts
```

### Last-Click Attribution
```
Definition: Credit goes to final touchpoint before conversion

Use When:
- Direct response campaigns
- Short consideration cycles
- Platform's default reporting

Pros: Easy to measure, platform default
Cons: Misses full customer journey
```

### View-Through Attribution
```
Definition: Credits ads that were viewed but not clicked

Use When:
- Display/video campaigns
- Brand awareness
- Understanding assist impact

Pros: Captures passive influence
Cons: Harder to prove causality
```

### Multi-Touch Attribution (Advanced)
```
Definition: Distributes credit across touchpoints

Use When:
- Complex customer journeys
- Multi-platform campaigns
- Data-driven marketing

Pros: Most accurate picture
Cons: Requires advanced analytics setup
```

## Tracking Setup

### Essential Tracking Elements
```
1. Pixel Installation
   [ ] Meta Pixel on all pages
   [ ] Google Tag Manager installed
   [ ] TikTok Pixel (if using)
   [ ] LinkedIn Insight Tag (if using)

2. Conversion Events
   [ ] PageView (base)
   [ ] ViewContent (product views)
   [ ] AddToCart
   [ ] InitiateCheckout
   [ ] Purchase
   [ ] Lead (for lead gen)
   [ ] Custom events as needed

3. UTM Parameters
   [ ] utm_source (platform)
   [ ] utm_medium (ad type)
   [ ] utm_campaign (campaign name)
   [ ] utm_content (creative/audience)
   [ ] utm_term (keywords)

4. Value Tracking
   [ ] Dynamic value for purchases
   [ ] Lead value assigned
   [ ] ROAS calculation enabled
```

### UTM Parameter Structure
```
Format: [URL]?utm_[parameter]=[value]

Example:
https://example.com/product?
utm_source=facebook
&utm_medium=cpc
&utm_campaign=spring_sale
&utm_content=video_ad_variant_a
&utm_term=lookalike_1_percent

Naming Conventions:
- Source: facebook, instagram, tiktok, google, linkedin
- Medium: cpc, display, video, social
- Campaign: descriptive name, date coded
- Content: creative_type, audience, variant
```

## Reporting Templates

### Daily Monitoring (for active campaigns)
```
Campaign Health Check:
- Yesterday's spend
- Yesterday's results (conversions/revenue)
- CPA/ROAS vs target
- Top 3 performing ads
- Bottom 3 performing ads
- Actions needed

Time investment: 5-10 minutes
```

### Weekly Report
```
Executive Summary:
- Week over week performance
- Budget consumed
- Results achieved
- CPA/ROAS summary

By Campaign:
- Performance breakdown
- Winning/losing audiences
- Creative performance
- Recommendations

Time investment: 30-45 minutes
```

### Monthly Report
```
Campaign Performance:
- Total spend vs budget
- Total conversions/revenue
- Overall CPA/ROAS
- Month over month trends

Learnings:
- What worked
- What didn't
- Audience insights
- Creative insights
- Platform insights

Next Steps:
- Recommendations
- Budget adjustments
- Test ideas
- Action items

Time investment: 1-2 hours
```

## Optimization Triggers

### When to Take Action

#### Green Light (Scale)
```
✅ ROAS > 3.0x (or target)
✅ CPA < target
✅ CTR above benchmark
✅ Conversion rate stable
✅ Frequency < 4

Action: Scale budget by 20-50%
```

#### Yellow Light (Monitor)
```
⚠️ ROAS 1.5-3.0x
⚠️ CPA at target
⚠️ CTR at benchmark
⚠️ Frequency 4-6

Action: Monitor closely, optimize creatives
```

#### Red Light (Fix)
```
❌ ROAS < 1.5x
❌ CPA above target
❌ CTR below benchmark
❌ Frequency > 6

Action: Pause or significantly restructure
```

### Optimization Actions

| Situation | Action | Timeline |
|-----------|--------|----------|
| High CPA, low CTR | New creatives, pause losers | Immediately |
| High CPA, high CTR | Check landing page, offer | 24-48 hours |
| High Frequency | New audiences, refresh creative | 48-72 hours |
| Scaling winner | Increase budget 20-50% | Weekly |
| Learning phase | Don't touch for 7 days | Day 1-7 |

---

## Measurement Checklist

Setup Phase
- [ ] All pixels installed and tested
- [ ] Conversion events configured
- [ ] Value tracking enabled
- [ ] UTM parameters documented
- [ ] Analytics integration verified
- [ ] Baseline metrics documented

Monitoring Phase
- [ ] Daily check schedule set
- [ ] Alert thresholds configured
- [ ] Dashboard built
- [ ] Access granted to all stakeholders

Reporting Phase
- [ ] Report templates created
- [ ] Report schedule defined
- [ ] Stakeholder list confirmed
- [ ] Goals and targets documented

Optimization Phase
- [ ] Optimization triggers defined
- [ ] Scaling rules established
- [ ] Pause/kill criteria set
- [ ] Testing framework ready
