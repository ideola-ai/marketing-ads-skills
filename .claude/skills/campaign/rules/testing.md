# A/B Testing Framework

## Testing Philosophy

### Core Principles
1. **Test one variable at a time** - Isolate what's working
2. **Statistical significance matters** - 95%+ confidence
3. **Sample size matters** - Minimum 1000 impressions
4. **Test quickly, fail fast** - Weekly testing cycles
5. **Document everything** - Learnings compound over time

### What to Test (Priority Order)

| Priority | Variable | Difficulty | Impact |
|----------|----------|------------|--------|
| 1 | Hook/Creative | Low | High |
| 2 | Audience | Medium | High |
| 3 | Offer | Medium | High |
| 4 | Format | Low | Medium |
| 5 | CTA | Low | Medium |
| 6 | Landing Page | High | Medium |
| 7 | Bid Strategy | Low | Low |

## Test Types

### Creative Tests
```
Test: Hook Variations
Variable: First 1-3 seconds of creative
Control: Everything else stays same
Variations: 3-5 different hooks
Duration: 3-5 days or 1000 impressions each
Winner: Highest CTR, lowest CPC
```

```
Test: Format Comparison
Variable: Ad format (video vs image vs carousel)
Control: Same message, audience, offer
Variations: 2-3 formats
Duration: 7 days
Winner: Highest conversion rate, lowest CPA
```

```
Test: Creative Style
Variable: UGC vs Professional vs Mixed
Control: Same message and offer
Variations: 2-3 styles
Duration: 7 days
Winner: Best engagement + conversion balance
```

### Audience Tests
```
Test: Lookalike Percentage
Variable: LAL 1% vs LAL 2% vs LAL 5%
Control: Same creative, same budget
Variations: 3 audience sizes
Duration: 7-14 days
Winner: Best CPA with scale potential
```

```
Test: Interest Clusters
Variable: Different interest-based audiences
Control: Same creative, same budget
Variations: 3-5 interest groups
Duration: 7 days
Winner: Lowest CPA, best ROAS
```

### Offer Tests
```
Test: Discount Percentage
Variable: 10% vs 20% vs 30% off
Control: Same creative, same audience
Variations: 3 offer levels
Duration: 7-14 days
Winner: Best ROAS (not just conversion rate)
```

```
Test: Bonus vs Discount
Variable: Free shipping vs % off vs free gift
Control: Same creative, same audience
Variations: 3 offer types
Duration: 7 days
Winner: Best ROAS and profit margin
```

## Test Structure

### Proper A/B Test Setup
```
Ad Set A (Control):
- Creative: Original
- Audience: Same
- Budget: Equal split
- Duration: Same time period

Ad Set B (Variant):
- Creative: Changed variable
- Audience: Same
- Budget: Equal split
- Duration: Same time period

Compare: Performance metrics
Winner: Statistically significant winner
Scale: Winner, kill loser
```

### Multivariate Testing (Advanced)
```
Only use after single-variable testing complete:
- Test 2-3 variables simultaneously
- Requires more budget and traffic
- Use for optimization phase
- Example: Hook x Format x CTA = 8 variations

Not recommended for:
- New campaigns
- Limited budgets
- Small audiences
```

## Statistical Significance

### When Do You Have a Winner?

#### Minimum Requirements
- [ ] At least 1000 impressions per variation
- [ ] At least 50 conversions per variation (for conversion tests)
- [ ] Test ran for minimum 3-5 days
- [ ] Consistent performance (not just one day spike)

#### Quick Confidence Check
```
If Variant A beats Variant B:
- 20%+ difference = Likely winner (80% confidence)
- 30%+ difference = Strong winner (90% confidence)
- 50%+ difference = Definite winner (95%+ confidence)

For high-stakes decisions, use proper statistical calculator
```

### Sample Size Calculator (Rule of Thumb)
```
For CTR Testing (CTR ~1-2%):
- Need: 10,000 impressions per variation
- Time: 3-7 days depending on budget

For Conversion Testing (CVR ~1-2%):
- Need: 100+ conversions per variation
- Time: 7-14 days depending on budget

For CPA Testing:
- Need: 50+ conversions per variation
- Time: 7-14 days depending on budget
```

## Testing Calendar

### Week 1: Launch Tests
```
Day 1-2: Campaign launch, baseline established
Day 3-4: Monitor performance, gather data
Day 5-7: Initial cut decisions (clear losers only)

Actions:
- Pause ads with <50% of benchmark CTR
- Keep top 70% of creatives running
- Document early observations
```

### Week 2: Decision Point
```
Day 8-10: Significant data accumulated
Day 11-12: Statistical analysis
Day 13-14: Make decisions, scale winners

Actions:
- Kill bottom 50% of ads
- Double budget on top 20%
- Prepare new variations of winners
```

### Week 3: Iteration Tests
```
Day 15-17: Launch new variations
Day 18-21: Monitor and compare

Actions:
- Test iterations of winning angles
- Small budget on new concepts (20%)
- Maintain winners (80%)
```

### Week 4: Final Optimization
```
Day 22-28: Final selections and documentation

Actions:
- Finalize winning creatives
- Document all test results
- Prepare recommendations for next campaign
```

## Test Documentation Template

```markdown
## Test Report: [Test Name]

### Test Overview
- **Date Range:** [Start] - [End]
- **Objective:** [What we wanted to learn]
- **Hypothesis:** [What we thought would happen]

### Test Setup
- **Variable Tested:** [What changed]
- **Control:** [Description]
- **Variations:** [List variations]
- **Budget:** [Total spend]

### Results
| Variation | Impressions | CTR | CPC | Conversions | CPA | ROAS |
|-----------|-------------|-----|-----|-------------|-----|------|
| Control   |             |     |     |             |     |      |
| Variant A |             |     |     |             |     |      |
| Variant B |             |     |     |             |     |      |

### Winner
- **Winning Variation:** [Name]
- **Margin of Victory:** [X% better]
- **Confidence Level:** [%]

### Key Learnings
- [What surprised you]
- [What confirmed assumptions]
- [What to test next]

### Next Actions
- [ ] [Action 1]
- [ ] [Action 2]
- [ ] [Action 3]
```

## Common Testing Mistakes

### Don't Do This
```
❌ Testing too many variables at once
❌ Calling winners too early (<1000 impressions)
❌ Testing without enough budget
❌ Changing multiple things mid-test
❌ Not documenting results
❌ Testing seasonal concepts in wrong season
❌ Ignoring statistical significance
❌ Scaling losers because of "gut feeling"
```

### Do This Instead
```
✅ Test one variable at a time
✅ Wait for statistical significance
✅ Budget properly for testing
✅ Let tests run their course
✅ Document everything
✅ Time tests with seasonality
✅ Scale only proven winners
```

## Testing ROI Calculation

### Is Testing Worth It?
```
Calculate: Potential lift vs Testing cost

Example:
- Current spend: $10,000/month
- Current CPA: $50
- Current conversions: 200/month

If test improves CPA by 10%:
- New CPA: $45
- Same budget = 222 conversions
- Value of improvement: 22 extra conversions = $1,100/month

Testing cost: $500 (creative + time)
ROI: 120% first month, compounding thereafter

✅ Worth testing if:
- Expected lift > testing cost
- Learnings apply to future campaigns
- Budget supports testing phase
```

---

## Testing Checklist

Pre-Test
- [ ] Hypothesis clearly stated
- [ ] One variable isolated
- [ ] Control group defined
- [ ] Success criteria set
- [ ] Budget allocated
- [ ] Timeline set

During Test
- [ ] No mid-test changes
- [ ] Daily monitoring (no intervention)
- [ ] Data collecting accurately
- [ ] Notes taken on anomalies

Post-Test
- [ ] Statistical significance confirmed
- [ ] Results documented
- [ ] Learnings extracted
- [ ] Decisions made
- [ ] Next test planned
