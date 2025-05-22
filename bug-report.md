# Bug Report: Safeguru Website Testing

## Overview
During automated testing of Safeguru.com using Playwright and TypeScript, the following issues were identified.

---

## Bug #1: Search Functionality – Incorrect Results for Certain Keywords

### **Steps to Reproduce**
1. Navigate to `https://safeguru.com`.
2. Locate the **search bar**.
3. Enter the keyword `"guantes"` and press **Enter**.
4. Observe the results displayed.

### **Expected Result**
- The search results should display products related to `"guantes"`.
- Pagination should be available for large results.
- Search suggestions should appear while typing.

### **Actual Result**
- Results returned included unrelated items (e.g., **cascos** instead of guantes).
- No pagination was shown for a large number of results.
- Search suggestions were missing.

### **Severity Level**
🔴 **High** – Incorrect product search results impact user experience.

---

## Bug #2: Product Page – "Add to Cart" Button Not Working

### **Steps to Reproduce**
1. Perform a search for `"guantes"`.
2. Click on a **product from search results**.
3. Locate and click the `"Add to Cart"` button.
4. Open the cart to verify if the item was added.

### **Expected Result**
- The selected product should be added to the cart.
- The cart should update to reflect the item’s name and price.

### **Actual Result**
- Clicking `"Add to Cart"` had **no effect**.
- The cart remained **empty** even after multiple attempts.
- No error messages appeared in the UI.

### **Severity Level**
🟠 **Medium** – Major issue affecting purchasing functionality.

---
## Bug #3: Performance – Slow Page Load Times

### **Steps to Reproduce**
1. Navigate to `https://safeguru.com`.
2. Measure page load time using **Playwright performance checks**.
3. Compare results against an acceptable threshold (**<3 seconds**).

### **Expected Result**
- Page should load within **3 seconds**.

### **Actual Result**
- Homepage took **6+ seconds** to fully load.
- High console errors detected during load.

### **Severity Level**
🟡 **Low** – Performance issues affect responsiveness.

Bug #4: Cart Functionality – Incorrect Price Updates
Steps to Reproduce:

Add multiple items to the cart.

Update the quantity of an item.

Observe the total price calculation.

Expected Result:
The total price should update correctly based on quantity.

Actual Result:
Price remained unchanged after modifying item quantity.
Inconsistent calculation observed.
Severity Level: 🟠 Medium – Impacts transaction accuracy.

Bug #5: Broken Links on Footer

Steps to Reproduce:
Scroll to the bottom of the homepage.
Click on links within the footer section.

Expected Result:
Links should correctly navigate to expected pages.

Actual Result:
Some links led to 404 error pages.
Certain links were non-clickable.

Severity Level: 🟡 Low – Impacts usability but does not break core functionality.
