# Validating Dog Walker Data

## Practice

1. `Name`, `Address`, `NeighborhoodId` properties on an Owner should be required.
1. `Name` and `OwnerId` on Dog should be required.
1. Walker `Name` and `NeighborhoodId` should be required.
1. `Name` for Owners, Dogs, and Walkers should be a minimum of of 2 characters and and no more than 40.

## Challenge: Regular Expressions

Regular expressions are a useful machanism in all software languages that allow you to do advanced pattern matching. Visit [https://regexr.com/](https://regexr.com/) and [https://www.regular-expressions.info/](https://www.regular-expressions.info/) and find a way to write a regular expression validation rule for the following requirement.

1. Although Owners' phone numbers are stored in a string, validate that the string contains only digits.
1. If the phone number validation fails, the client should get the error message _"Phone number must contain only digits"_
