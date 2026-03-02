# ShopConnect Grocery AI: Business & Engineering Context

This document outlines the core business constraints and algorithmic modeling requirements for the ShopConnect Grocery AI domain pack.

## 1. Grocery Pre-Order System Constraints

- **Inventory Allocation**: Pre-orders must place soft-holds on future projected inventory. The system must probabilistically forecast available SKU counts for the delivery delivery date (T+x).
- **Cold-Chain Logistics**: Certain items (frozen, refrigerated) have strict capacity limits in delivery fulfillment windows. Pre-order permutations must validate against available cold-storage transport slots in real-time.
- **Substitution Fallbacks**: Every pre-order item must have an associated algorithmic substitution SLA (e.g., "exact brand match required" vs "any 2% milk").

## 2. Pantry Depletion Modeling

- **Consumption Rate Profiling**: The system must track user-specific consumption rates for staple goods (e.g., milk, bread, eggs) using a time-series decay model.
- **Depletion Triggers**: When a user's probability of depletion for a staple exceeds a tunable confidence threshold (default `p > 0.85`), the system must enqueue the item to the user's active recommendation pipeline.
- **Seasonal Adjustments**: The model must apply seasonal modifiers to consumption rates (e.g., ice cream depletion increases in summer).

## 3. Repeat Purchase Inference

- **Frequency Vectors**: Build an embedding vector for each user based on purchase frequency, grouping items into temporal cohorts (weekly regimens, monthly bulk purchases).
- **Abandonment Detection**: The system must differentiate between temporary anomalous gaps in purchasing versus a permanent shift in user preference, decaying the recommendation score for repeatedly ignored staples.

## 4. Nutrition Scoring Logic

- **Composite Index Scoring**: Each product must calculate a composite health score normalized between 0 and 100, weighting macronutrients, sodium, added sugars, and specific user dietary profiles (e.g., Keto, Diabetic).
- **Basket-Level Evaluation**: The AI must be capable of computing an aggregated nutritional score for the entire shopping cart to provide immediate feedback against the user's weekly health goals.

## 5. Meal Planning Constraints

- **Ingredient Intersection**: Meal plans must optimize for ingredient overlap to minimize user cost and food waste. The planner is constrained to generate non-overlapping secondary ingredients.
- **Yield Mapping**: The engine must convert abstract recipe requirements (e.g., "1 cup of flour") into exact purchasable SKUs (e.g., "1x 5lb Bag Gold Medal Flour").
- **Substitution in Planning**: If a central ingredient for a planned meal is out-of-stock, the algorithm must dynamically recalculate the rest of the meal plan's ingredient dependencies.

## 6. Healthbot Evolution Plan

- **Phase 1: Reactive Parsing**: The Healthbot must parse simple natural language queries against the user's current basket (e.g., "Is my cart healthy?").
- **Phase 2: Proactive Optimization**: Implement multi-armed bandit strategies where the bot suggests direct 1:1 swaps (e.g., swapping white rice for quinoa) at checkout.
- **Phase 3: Autonomous Cohort Analysis**: The Healthbot will compare user buying patterns against anonymized, demographically similar cohorts with high nutritional scores to auto-generate weekly adaptive cart templates.
