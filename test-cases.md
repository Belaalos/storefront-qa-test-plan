# Test cases

| ID | Module | Title | Steps | Expected result | Priority | Status |
|---|---|---|---|---|---|---|
| TC-01 | Login | Login with valid credentials | Open site; enter standard_user / secret_sauce; click Login | Products page opens | High | Pass (automated) |
| TC-02 | Login | Login with wrong password | Enter standard_user and a wrong password; click Login | Error: Username and password do not match | High | Pass (automated) |
| TC-03 | Login | Login with unknown username | Enter a user that does not exist; click Login | Error: Username and password do not match | Medium | Pass (automated) |
| TC-04 | Login | Login with empty username | Leave username empty, enter password; click Login | Error: Username is required | Medium | Pass (automated) |
| TC-05 | Login | Login with empty password | Enter username, leave password empty; click Login | Error: Password is required | Medium | Not run |
| TC-06 | Login | Login with both fields empty | Click Login with empty form | Error: Username is required | Low | Not run |
| TC-07 | Login | Locked out user | Login as locked_out_user | Error: Sorry, this user has been locked out | High | Pass (automated) |
| TC-08 | Login | Logout | Login; open menu; click Logout | Login page is shown | High | Pass (automated) |
| TC-09 | Login | Open inventory without login | Go to /inventory.html directly without logging in | Error says you can only access it when logged in | High | Pass (automated) |
| TC-10 | Login | Error message can be closed | Trigger a login error; click the X on the message | Error message disappears | Low | Not run |
| TC-11 | Login | Password field is masked | Type in the password field | Characters are hidden | Low | Not run |
| TC-12 | Inventory | Six products are listed | Login and look at the products page | 6 products with name, price, image | High | Pass (automated) |
| TC-13 | Inventory | Sort by name A to Z | Choose Name (A to Z) | Products sorted alphabetically | Medium | Pass (automated) |
| TC-14 | Inventory | Sort by name Z to A | Choose Name (Z to A) | Products sorted in reverse alphabetical order | Medium | Pass (automated) |
| TC-15 | Inventory | Sort by price low to high | Choose Price (low to high) | Prices ascending | Medium | Pass (automated) |
| TC-16 | Inventory | Sort by price high to low | Choose Price (high to low) | Prices descending | Medium | Pass (automated) |
| TC-17 | Inventory | Open product details | Click a product name | Details page shows the same name, price and description | High | Not run |
| TC-18 | Inventory | Product images are different | Compare the images on the products page | Each product shows its own image | Medium | Not run |
| TC-19 | Cart | Add one product | Click Add to cart on a product | Button changes to Remove; cart badge shows 1 | High | Pass (automated) |
| TC-20 | Cart | Add several products | Add 2 products | Cart badge shows 2 | High | Pass (automated) |
| TC-21 | Cart | Remove product from the products page | Add a product, then click Remove | Badge decreases; button back to Add to cart | High | Pass (automated) |
| TC-22 | Cart | Cart page lists added products | Add products; open the cart | Names and prices match the products added | High | Pass (automated) |
| TC-23 | Cart | Remove product on the cart page | In the cart, click Remove | Product disappears from the list | Medium | Pass (automated) |
| TC-24 | Cart | Continue shopping from the cart | Click Continue Shopping | Products page is shown | Low | Not run |
| TC-25 | Cart | Cart is kept after refresh | Add a product; refresh the page | Cart badge still shows the product | Medium | Not run |
| TC-26 | Checkout | Complete purchase | Add product; Checkout; fill name and zip; Continue; Finish | Thank you for your order message | High | Pass (automated) |
| TC-27 | Checkout | First name is required | Checkout; leave first name empty; Continue | Error: First Name is required | High | Pass (automated) |
| TC-28 | Checkout | Last name is required | Fill first name only; Continue | Error: Last Name is required | Medium | Not run |
| TC-29 | Checkout | Postal code is required | Fill first and last name only; Continue | Error: Postal Code is required | Medium | Not run |
| TC-30 | Checkout | Overview shows correct total | Go to overview with 2 products | Item total + tax equals total | High | Not run |
| TC-31 | Checkout | Cancel checkout | On the information page click Cancel | Back to the cart with items still in it | Low | Not run |
| TC-32 | Checkout | Cart is empty after finishing | Finish an order; look at the cart badge | Badge is gone, cart empty | Medium | Not run |
| TC-33 | Problem user | Product images with problem_user | Login as problem_user; view products | Each product has its own image (see BUG-001) | Medium | Fail |
| TC-34 | Problem user | Last name field with problem_user | Login as problem_user; add product; checkout; type a last name | Last name stays in its own field and is accepted (see BUG-002) | High | Fail |
| TC-35 | Performance | Login speed with performance_glitch_user | Login as performance_glitch_user and time it | Login finishes in a normal time (see BUG-003) | Low | Fail |
| TC-36 | Menu | Reset App State | Add product; menu > Reset App State | Cart is emptied | Low | Not run |
| TC-37 | Menu | About link | Menu > About | Opens saucelabs.com | Low | Not run |
