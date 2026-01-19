# 🗺️ Experiment 01: Spatial Autocorrelation Analysis

## Business Objective
**Identify luxury housing price clusters** (hotspots) to create high-signal spatial features for price prediction.

## Reseach Question
**Does housing price exhibit spatial autocorrelation in NYC, and can we detect statistically significant clusters?**

## 📊 Key Results

| Feature | Method | Parameters | Performance | Status |
|---------|--------|------------|-------------|--------|
| `is_hotspot_price` | Adaptive KNN | k=5, Z>1.96 (95%) | **125 hotspots**<br>Mean: **$18.35M**<br>Excellent separation | ✅ **Production** |
| `is_coldspot_price` | All methods | All tested | **No signal**<br>Co-op bias only | ❌ **Excluded** |

## Methodology Summary

1.Spatial Weighting: Fixed Distance vs Adaptive KNN (k=5,10,15)
2. Normalization: Raw price → PPS → Type → Type+Borough
3. Significance: Z > 1.96 (95% confidence) / Z < -1.282 (80%)
4. Validation: Boxplots, mean price, visual inspection

**Tested 18 parameter combinations** → **k=5 Adaptive KNN optimal.**

## 🚫 Why Coldspots Failed
- 89% Co-ops (regulated pricing)
- No signal at Z < -1.282 (80% confidence)
- Z < -0.4 required (statistically weak)
- Normalization doesn't remove structural bias

# Feature stats
is_hotspot_price: 125 hotspots (2.5% of listings)
Mean price premium: +$12.8M vs non-hotspots

