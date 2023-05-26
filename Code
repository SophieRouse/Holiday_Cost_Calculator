# This code calculates how much a holiday will cost depending on location and number of days.
# The user can select from a list of holiday locations, which have prices linked to them in dictionaries.

# This dictionary is used to assign prices of flights to certain cities.
flight_price = {
    "Paris": 40.99,
    "Marrakesh": 70.99,
    "Brussels": 29.99,
    "Barbados": 680.99,
    "Florida": 700.99,
    "Las Vegas": 980.99,
    "Hong Kong": 590.99
}

#This dictionary is used to assign hotel prices to each city.
hotel_price = {
    "Paris": 120.50,
    "Marrakesh": 110.00,
    "Brussels": 50.30,
    "Barbados": 200.40,
    "Florida": 250.00,
    "Las Vegas": 90.99,
    "Hong Kong": 130.99
}

# Users input which city they want to fly to.
# If they input something other than a city name in the list they will recieve an error message.
while True:
    try:
        city_flight = input("Please enter the city you will be flying to. Choose from: Paris, Marrakesh, Brussels, Barbados, Florida, Las Vegas or Hong Kong. ")
        if not city_flight in flight_price.keys():
            print("ERROR: Invalid City Name")
            raise ValueError 

# The user is also asked to input the number of nights they will stay at a hotel and number of days they require a car rental for.
# The user has to input an integer, or an error message is returned.
        num_nights = int(input("Please enter the number of nights you will be staying at the hotel: "))
        rental_days = int(input("Please enter the number of days you will be hiring a car for: "))
        break
    except ValueError as error:
        print("ERROR: Invalid input")
        print(error)

# Functions are defined to allow easier calculations.
def hotel_cost(num_nights):
    return float(num_nights) * hotel_price[city_flight]

def plane_cost(city_flight):
    return flight_price[city_flight]

def car_rental(rental_days):
    return float(rental_days) * 60.0

def holiday_cost(hotel_cost, plane_cost, car_rental):
    return hotel_cost + plane_cost + car_rental

# The user's inputs are used to calculate costs which are then printed back to them.
print("\nThe hotel will cost: £", hotel_cost(num_nights))
print("The flights will cost: £", plane_cost(city_flight))
print("The car rental will cost: £", car_rental(rental_days))
print("The total cost of your holiday will be: £", holiday_cost(hotel_cost(num_nights), plane_cost(city_flight), car_rental(rental_days)))
