# Bug reports

Found while testing saucedemo.com with the different test users. All three were reproduced on 26 Nov 2026 in Chrome.

## BUG-001: problem_user sees the same image for every product

- **Severity:** Medium
- **Environment:** Chrome, saucedemo.com, user `problem_user` / `secret_sauce`
- **Steps:**
  1. Login as `problem_user`
  2. Look at the products list
- **Actual result:** all 6 products show the same image (only one unique image source on the page).
- **Expected result:** every product shows its own image, like with `standard_user`.
- **Evidence:** [screenshots/bug-001-same-images.png](screenshots/bug-001-same-images.png)

## BUG-002

- **Severity:** High (blocks checkout)
- **Environment:** Chrome, saucedemo.com, user `problem_user` / `secret_sauce`
- **Steps:**
  1. Login as `problem_user`
  2. Add Sauce Labs Backpack, open the cart, click Checkout
  3. Type first name, last name and postal code
  4. Click Continue
- **Actual result:** the text typed in Last Name replaces the First Name value (the first name field shows "Magdy"), the Last Name field stays empty and the page shows "Error: Last Name is required".
- **Expected result:** each field keeps its own value and the user moves to the overview page.
- **Evidence:** [screenshots/bug-002-last-name-empty.png](screenshots/bug-002-last-name-empty.png)

## BUG-003: login takes about 5 seconds for performance_glitch_user

- **Severity:** Low
- **Environment:** Chrome, saucedemo.com, user `performance_glitch_user` / `secret_sauce`
- **Steps:**
  1. Open the login page
  2. Login as `performance_glitch_user` and time how long until the products page opens
- **Actual result:** about 5 seconds (measured 5.1 s). Other users log in in under 0.1 s.
- **Expected result:** login time similar to the other users.
