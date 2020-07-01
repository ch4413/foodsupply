# foodsupply

#### 1. Forecast: We start with a forecast
For each store and item:

Calculation:
* Forecast - stockfile  = amount_to_purchase

Problem:
* The stockfile is unreliable. **Note:** Look at where stockfile is recorded.
* Suppliers under and over-deliver

Limitation:
* amount_to_purchase can only be in tray sizes.
* Must order enough to cover delivery period as suppliers can't deliver every day. **Note:** Check the range of delivery periods.

#### 2. Depot: Supplier delivers to the depots

Problem:
* There will be a difference between the shipped amount from a depot and the amount arriving at a store

Limitation:
* The allocation to a shop is limited by the supply to the depot.

#### 3. In Store: Products arrive at the store

Problem:
* Delivered amount can differ from depot shipping amount - incorrectly picked

#### 4. Closing Inventory:

Closing inventory is also taken in store and all its fields are contained in the In Store data.

**Note:** Check if they are the same. If same, discard, closing inventory. If not, give measure of difference and check with company why there are two and which is most reliable.

### Plan

1. Check data quality
2. Join data and remove values
3. Create metrics
4. Create final dataset
5. Lightweight analysis
6. Create plotss