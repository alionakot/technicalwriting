#### Task
Write 5 requirements for a taxi ordering application with cryptocurrency payment in the format of a technical specification.   
Expand 2 of these requirements into the format of a technical project.

## Technical Specification (Fragment)

**Requirement 1: User Interface**  
The user must be able to see the following elements upon launching the application:

1. A map displaying their current location.
2. A search bar where they can enter their destination address.
3. A list of their recent destination points.
The user must confirm the accuracy of the taxi's arrival point if it's determined correctly via geolocation.

If geolocation is inaccurate or imprecise, the user should have the option to move the marker to a more accurate point on the map.

**Requirement 2: Tariff and Payment Selection**  
The user must have the ability to select a tariff (economy, comfort, pet-friendly) and a payment method (credit card or cryptocurrency).

**Requirement 3: Driver Location Tracking and Notifications**  
The user should be able to track the driver's location on the map, with dynamic updates reflecting the vehicle's movement. The following notifications should be sent to the user after order confirmation:

* Driver found with vehicle details.
* Driver will arrive in 2 minutes.
* Driver has arrived.
* The trip has begun.
* The trip has ended.

Alternatively:
* Vehicle not found.
* Driver declined the order.

## Technical Project (Fragment)
**Feature: Address Selection (Requirement 2-3)**  
Upon app launch, the user will see:

* A map displaying their current location.  
* Their location displayed as a red balloon at the center of the map (automatically determined).  
* A dropdown search bar for entering the destination address.  
* Screen Layout (Refer to Figure 1):  

The map occupies the top 2/3 of the screen.  
The address selection panel occupies the bottom 1/3 and includes:
* A search bar labeled "Where to?"
* The three most recent destination points (if the user has chosen less than 3 unique addresses, only the existing number of unique addresses will be displayed, as shown in Figure 2).
* A "Select on Map" button.

**Functionality of Address Fields A and B:**

* Users can click on any of their recent addresses or input a new one.
* To enter a new address, the user clicks the search bar, which opens a window with two address fields, A and B.
* Next to Address A, there is an icon resembling a green circle, connected by a line pointing down to a blue geolocation icon next to Address B. Address A is pre-filled based on the user's geolocation. Address B is initially blank, with the cursor automatically placed in the Address B field.
* Beneath the Address B field is the list of the user's recent destination points. If the user doesn't have any previous addresses, this field will remain empty.

Next to the Address B field is a plus icon (+). Clicking it adds another address field below Address B, converting Address B into an intermediate point (marked by a smaller blue circle than the green circle at Address A).

Below the list of recent addresses, there's a "Select on Map" button. Clicking this button opens the map at the user's current geolocation, with a red balloon in the center. As the user moves the map, the address displayed at the bottom updates accordingly. The user selects their destination on the map and clicks the "Confirm" button (examples are shown in Figure 3).

**Feature: Payment and Tariff Selection (Requirement 4-5)**  
Tariff and Payment

After choosing the destination, the user will see:

The selected address at the top of the screen.
* A map displaying the route from Address A to Address B.
* Tariff selection (automatically set to "economy" by default).
* Estimated trip cost according to the selected tariff.
* Payment method selection and a "Confirm Taxi Order" button (as shown in Figure 4).

Options for Tariff Selection:

* Economy
* Comfort
* Pet-Friendly

Options for Payment Method Selection (Figure 5):

* Online Credit Card Payment
* Cryptocurrency Payment
After selecting the payment method, the user clicks the "Confirm Taxi Order" button, initiating the driver search process.

Payment Note: In initial releases, payment will be processed after the trip. Order confirmation functionality will be implemented in later versions of the app.
