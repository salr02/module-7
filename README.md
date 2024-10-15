# module-7

# Step 1: Create a list for an S3 object
s3_car <- list(make = "Toyota", model = "Camry", year = 2020)

# Step 2: Assign a class to the object
class(s3_car) <- "car"

# Step 3: Create a generic function to print the car details
print.car <- function(obj) {
  cat("Car Make:", obj$make, "\n")
  cat("Car Model:", obj$model, "\n")
  cat("Car Year:", obj$year, "\n")
}

# Step 4: Test the S3 object
print(s3_car)

# Step 1: Define an S4 class for a car
setClass(
  "Car",
  slots = list(
    make = "character",
    model = "character",
    year = "numeric"
  )
)

# Step 2: Create an instance of the S4 class
s4_car <- new("Car", make = "Honda", model = "Civic", year = 2019)

# Step 3: Define a method to show the S4 object
setMethod("show", "Car", function(object) {
  cat("Car Make:", object@make, "\n")
  cat("Car Model:", object@model, "\n")
  cat("Car Year:", object@year, "\n")
})

# Step 4: Test the S4 object
s4_car
