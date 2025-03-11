START
PRINT "Enter the total bill amount: "
READ bill_amount
IF bill_amount <= 0 THEN
    PRINT "Error: Bill amount must be a positive number."
    STOP
END IF
PRINT "Enter service quality (poor, fair, good, excellent): "
READ service_quality
IF service_quality = "poor" THEN
    SET tip_percentage = 10
ELSE IF service_quality = "fair" THEN
    SET tip_percentage = 15
ELSE IF service_quality = "good" THEN
    SET tip_percentage = 18
ELSE IF service_quality = "excellent" THEN
    SET tip_percentage = 20
ELSE
    PRINT "Error: Invalid service quality rating."
    STOP
END IF
PRINT "Enter the number of people splitting the bill: "
READ num_people
IF num_people <= 0 THEN
    PRINT "Error: Number of people must be a positive integer."
    STOP
END IF
SET tip_amount = (bill_amount * tip_percentage) / 100
SET total_amount = bill_amount + tip_amount
SET amount_per_person = total_amount / num_people
PRINT "Original Bill Amount: " + bill_amount
PRINT "Service Quality: " + service_quality + " (" + tip_percentage + "% tip)"
PRINT "Tip Amount: " + tip_amount
PRINT "Total Amount (including tip): " + total_amount
PRINT "Number of People: " + num_people
PRINT "Amount per Person: " + amount_per_person
END
