# Campaign Architecture Frameworks

## Funnel-Based Architecture

### Top of Funnel (Awareness)
```
Campaign Name: [Brand] - TOF - [Month]
Objective: Reach / Brand Awareness
Ad Sets:
- Broad audience (interest-based)
- Lookalike audience (from customers)
- Location/Demographic targeting

Creatives:
- Video ads (15-30 seconds)
- Brand storytelling
- Problem introduction
```

### Middle of Funnel (Consideration)
```
Campaign Name: [Brand] - MOF - [Month]
Objective: Traffic / Engagement
Ad Sets:
- Page engagers
- Video viewers (25%+)
- Website visitors (last 30 days)

Creatives:
- Carousel ads (feature showcase)
- Longer video (60 seconds)
- Educational content
- Social proof elements
```

### Bottom of Funnel (Conversion)
```
Campaign Name: [Brand] - BOF - [Month]
Objective: Conversions / Sales
Ad Sets:
- Add to cart (last 7 days)
- Website visitors (last 7 days)
- Retargeting video viewers (50%+)
- Customer list (exclude purchasers)

Creatives:
- Offer-focused
- Urgency/scarcity
- Strong CTAs
- Social proof (reviews, testimonials)
```

## Audience-Based Architecture

### Cold Audience (Never interacted)
```
Campaign: [Brand] - Cold Traffic
Objective: Awareness → Consideration

Ad Sets by interest cluster:
- Interest Cluster 1: [Related interests]
- Interest Cluster 2: [Competitor interests]
- Interest Cluster 3: [Problem-aware interests]
- Lookalike 1%: From customer list

Budget Allocation: 60% of total
```

### Warm Audience (Interacted but not converted)
```
Campaign: [Brand] - Warm Traffic
Objective: Consideration → Conversion

Ad Sets by engagement type:
- Page engagers (last 30 days)
- Video viewers (50%+, last 30 days)
- Website visitors (last 30 days)
- Instagram engagers

Budget Allocation: 30% of total
```

### Hot Audience (Ready to convert)
```
Campaign: [Brand] - Hot Traffic
Objective: Conversion

Ad Sets by action:
- Add to cart (last 7 days)
- Initiated checkout (last 7 days)
- Viewed content (last 14 days)
- Customer list (exclude recent purchasers)

Budget Allocation: 10% of total
```

## Platform-Specific Architecture

### Meta Ads (Facebook + Instagram)
```
Account Structure Level:
Account
├── Campaign (by objective)
│   ├── Ad Set (by audience)
│   │   ├── Ad (by creative)
│   │   ├── Ad (by creative)
│   │   └── Ad (by creative)
│   ├── Ad Set (by audience)
│   └── Ad Set (by audience)
```

### Campaign Naming Convention
```
Format: [Brand] - [Funnel] - [Audience] - [Month]

Examples:
- BrandX - TOF - Cold_LAL1 - Feb24
- BrandX - MOF - Engagers - Feb24
- BrandX - BOF - ATC_Retargeting - Feb24
```

## Budget Allocation Framework

### By Funnel Stage
| Stage | % of Budget | Rationale |
|-------|-------------|-----------|
| TOF | 50-60% | Feed the funnel |
| MOF | 25-30% | Nurture interest |
| BOF | 15-20% | Close sales |

### By Platform
| Platform | % of Budget | Best For |
|----------|-------------|----------|
| Meta Ads | 40-60% | Broad reach, visual |
| Google Ads | 20-30% | Intent-based |
| TikTok Ads | 10-20% | Gen Z, viral |
| LinkedIn Ads | 5-10% | B2B, professional |

### By Campaign Phase
| Phase | Days | % of Budget | Focus |
|-------|------|-------------|-------|
| Learning | 1-7 | 20% | Test and learn |
| Scaling | 8-21 | 60% | Scale winners |
| Optimization | 22-30 | 20% | Maximize efficiency |

## Campaign Calendar Template

### Week 1: Launch & Learning
```
Day 1-2: Campaign launch, initial ads go live
Day 3-4: Monitor performance, gather initial data
Day 5-7: First optimizations, pause underperformers

Deliverables:
- 3-5 ad sets per campaign
- 3-5 creatives per ad set
- Initial learning data
```

### Week 2-3: Scale & Optimize
```
Day 8-14: Scale winning ad sets/creatives
Day 15-21: Introduce new creative variations
Week 2: Budget +50% on winners
Week 3: Budget +100% on top performers

Deliverables:
- Kill bottom 50% of ads
- Double budget on top 20%
- Test 3-5 new creative angles
```

### Week 4: Maximize & Document
```
Day 22-28: Final optimization push
Day 29-30: Document learnings, prepare next campaign
Day 30+: Decide on continuation/changes

Deliverables:
- Final performance report
- Winning creatives archive
- Learnings document
- Recommendations for next campaign
```

## Retargeting Architecture

### Standard Retargeting Funnel
```
1. Website Visitors (All)
   ↓ Exclude: Purchasers (last 30 days)
2. Content Viewers (Product page)
   ↓ Exclude: Add to cart (last 7 days)
3. Add to Cart
   ↓ Exclude: Purchasers (last 7 days)
4. Initiated Checkout
   ↓ Exclude: Purchasers (last 3 days)
5. Purchasers (Upsell/Cross-sell)
   ↓ Exclude: Recent purchasers
```

### Time-Based Exclusion Windows
| Action | Exclude Window | Rationale |
|--------|---------------|-----------|
| Purchase | 30-90 days | Don't retarget recent buyers |
| Add to Cart | 7 days | Gave them time to convert |
| Video View | 14 days | Prevent fatigue |
| Website Visit | 30 days | Fresh audience needed |

## Campaign Scaling Framework

### Horizontal Scaling (More audiences)
```
✅ When to use:
- Winning creative has found product-market fit
- CAC is acceptable
- Platform has more inventory

✅ How to scale:
- Duplicate winning ad set to new audiences
- Expand location targeting
- Add similar interest clusters
- Increase lookalike percentage (1% → 2%)
```

### Vertical Scaling (More budget)
```
✅ When to use:
- Winning ad set is spend-capped
- CPA stable as budget increases
- Platform delivering more impressions

✅ How to scale:
- Increase budget by 20-50% increments
- Don't change targeting
- Keep creatives consistent
- Monitor closely for diminishing returns
```

---

## Architecture Checklist

Before launching, verify:

Campaign Structure
- [ ] Campaigns aligned with objectives
- [ ] Ad sets aligned with audiences
- [ ] Clear naming convention used
- [ ] Budget allocated by funnel stage

Audience Setup
- [ ] Cold, warm, hot audiences defined
- [ ] Exclusion sets configured
- [ ] Lookalike audiences created
- [ ] Retargeting windows set

Creative Readiness
- [ ] 3-5 angles per audience
- [ ] Multiple formats per angle
- [ ] Platform specs followed
- [ ] Tracking parameters added

Measurement Setup
- [ ] Pixel installed and tested
- [ ] Conversion events defined
- [ ] UTM parameters configured
- [ ] Analytics integration active
