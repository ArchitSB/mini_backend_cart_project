FlipDeal is an eCommerce company that has recently started dealing with multiple fitness products. Currently, they are starting small with 3 items in their cart:
 Shoes
 Bag
 Jacket

They have also launched a “Prime Membership” program where if you are the member at their platform, you get good discounts on the products.

Now, they already have built the frontend of the application showing the cart page with product details, images, and other options. But now they want a backend developer who can create the APIs for various cart actions and work with frontend.

Objective:
 FlipDeal has given you the project to create the APIs on the backend for their “Cart Page”.

What are the various actions a user has to take?

1.Add all the 3 Products to the Cart.
2.Once the products are added, check for the membership status.
3.If the membership status is “Standard”: No Discount is Added. If the membership status is “Prime”: 10% discount is added to the total cart amount.
4.Once done, select the location where you want your package to be delivered. We have 4 cities:
 Mumbai
 Delhi
 Chennai
 Kolkata

5.Based on the distance for the selected city, it calculates the “Shipping Cost”.
6.Now, select the type of “Shipping Method”. If the Shipping method is “Standard”, it calculates the time in which the package will be delivered in which is 1 day per 50 kms. If the Shipping method is “Express”, it calculates the time in which the package will be delivered which is 1 day per 100 kms
7.The Estimated Delivery time is visible.
8.Based on all the factors, the total payable amount is calculated.
9.Total Cart Amount
10.Membership Discount (if any)
11.Shipping Cost (Based on the Location)
12.Estimated Delivery Time (in days)
13.Tax Rate
14.Loyalty Points

Note: If you wish to test it with other factors, click “Reset form” button and try again.

API Endpoints:

Calculate Cart Total: When a user adds a new item to the cart, the frontend makes a GET request to /cart-total with the price of the new item and the current cart total to update the total price.

Apply Membership Discount: If the user is a member, the frontend makes a GET request to /membership-discount to apply any applicable discounts to the cart total.

CalculateTax: For the total cart amount, the frontend makes a GET request to /calculate-tax to apply 5% tax rate on the total cart amount.

Estimate Delivery Time: The user can see the estimated delivery time by making a GET request to /estimate-delivery with the chosen shipping method and delivery distance.

Calculate Shipping Cost: The shipping cost based on the weight of the items and the delivery distance is calculated by making a GET request to /shipping-cost.

Calculate Loyalty Points: To calculate the loyalty points, front end is making a GET request to /loyalty-points to add 2 points per $1.


vercel link: https://bd1-1.vercel.app/