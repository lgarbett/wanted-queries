<img src="https://devmounta.in/img/logowhiteblue.png" width="250" align="right">

# AJ's Enter Wanted Test

This protect is to create a web form that will generate the text to submit to the NCIC to add, edit, or delete a warrant.

It is assumed that if incorrect entry occurs, the proper error message will be displayed to assist the user in correcting their mistakes.

Development on the application has been focused only on completing the form and validations, stylistic concerns are not being addressed at this time.

### The requirements are as follows for each screen, and the results:

<details>

<summary> Enter Wanted Requirements </summary>

<br />

#### This screen exists to generate the text string which will be sent to the state or federal government, who will register a warrant using the supplied information.

alpha: any alphabetical characters, upper or lower case

numeric: numbers only, 0-9

special: these are any characters other than numbers and letters, including blank spaces ' ' - Periods '.' should not be allowed, as it will break message parsing.

* Header: Required, 9-19 characters in length, any allowed
* MKE: Required, 2-4 alpha/special characters in length
* Originating Agency Identifier: Required, 9 alphanumeric characters in length
* Name: Required, 3-30 characters in length, any allowed
* Sex: Required, 1 character in length, alphabet only, F (female) M (male) and U (unknown) are the only accepted entries
* Race: Required, 1 character in length, alphabet only
* Height: Required, 3 characters in length, numeric only in FII format, where F is feet and I is inches
* Weight: Required, 1-3 characters in length, numeric only in lbs, leading zeros to be entered systematically as necessary to change the length to 3 characters in the assembled query.
* Hair: Required, 3-10 characters in length, alpha only
* Offense: Required, 5-15 characters in length, any allowed
* Date of Warrant/Violation: Required, 8 characters in length, numeric in MMDDYYYY format (allows dates from 1900 to today +1 day, to account for time zone differences)
* Drivers License: Optional, 1-20 characters in length, any characters allowed, if included requires DL State & DL Expiration Year
* DL State: Optional, 2 characters in length, State Abbreviations only, if included requires Drivers License & DL Expiration Year
* DL Expiration Year: Optional, 4 characters in length, numeric in YYYY format, if included requires Drivers License & DL State
* License Plate: Optional, 5-8 alphanumeric characters in length, if included requires License State & License Year
* License State: Optional, 2 characters in length, State Abbreviations only, if included requires License Plate and License Year
* License Year: Optional, 4 characters in length, numeric in YYYY format, if included requires License Plate and License Year

Upon successful entry, a text message will be created, which consists of each of the values entered, separated by a '.' - any optional fields left blank will still be denoted in the message by an additional '.'

</details>

<details>

<summary> Modify Wanted Requirements </summary>

<br />

#### This screen exists to generate the text string which will be sent to the state or federal government, who will use the Warrant ID to find an existing warrant which will be modified with any other supplied information.

alpha: any alphabetical characters, upper or lower case

numeric: numbers only, 0-9

special: these are any characters other than numbers and letters, including blank spaces ' ' - Periods '.' should not be allowed, as it will break message parsing.

* Warrant ID: Required, 10 numbers - this ID is returned to the sending organization by the receiving organization when a warrant is entered.
* Header: Optional, 9-19 characters in length, any allowed
* MKE: Optional, 2-4 alpha/special characters in length
* Originating Agency Identifier: Optional, 9 alphanumeric characters in length
* Name: Optional, 3-30 characters in length, any allowed
* Sex: Optional, 1 character in length, alphabet only, F (female) M (male) and U (unknown) are the only accepted entries
* Race: Optional, 1 character in length, alphabet only
* Height: Optional, 3 characters in length, numeric only in FII format, where F is feet and I is inches
* Weight: Optional, 1-3 characters in length, numeric only in lbs, leading zeros to be entered systematically as necessary to change the length to 3 characters in the assembled query.
* Hair: Optional, 3-10 characters in length, alpha only
* Offense: Optional, 5-15 characters in length, any allowed
* Date of Warrant/Violation: Optional, 8 characters in length, numeric in MMDDYYYY format (allows dates from 1900 to today +1 day, to account for time zone differences)
* Drivers License: Optional, 1-20 characters in length, any characters allowed, if included requires DL State & DL Expiration Year
* DL State: Optional, 2 characters in length, State Abbreviations only, if included requires Drivers License & DL Expiration Year
* DL Expiration Year: Optional, 4 characters in length, numeric in YYYY format, if included requires Drivers License & DL State
* License Plate: Optional, 5-8 alphanumeric characters in length, if included requires License State & License Year
* License State: Optional, 2 characters in length, State Abbreviations only, if included requires License Plate and License Year
* License Year: Optional, 4 characters in length, numeric in YYYY format, if included requires License Plate and License Year

Upon successful entry, a text message will be created, which consists of each of the values entered, separated by a '.' - any optional fields left blank will still be denoted in the message by an additional '.'

</details>

<details>

<summary> Cancel Wanted Requirements </summary>

<br />

#### This screen exists to generate the text string which will be sent to the state or federal government, who will use the Warrant ID to find and cancel an existing warrant.

alpha: any alphabetical characters, upper or lower case

numeric: numbers only, 0-9

special: these are any characters other than numbers and letters, including blank spaces ' ' - Periods '.' should not be allowed, as it will break message parsing.

* Warrant ID: Required, 10 numbers - this ID is returned to the sending organization by the receiving organization when a warrant is entered.
* Reason for Cancellation: Required, 10-150 characters in length, any allowed - this is a free text field to explain why a warrant is being cancelled.
* Date of Cancellation: Required, 8 characters long, numerid in MMDDYYYY format - this is the date the cancellation is to take effect.

</details>

## Contributions

If you see a problem or a typo, please fork, make the necessary changes, and create a pull request so we can review your changes and merge them into the master repo and branch.

## Copyright

© DevMountain LLC, 2017. Unauthorized use and/or duplication of this material without express and written permission from DevMountain, LLC is strictly prohibited. Excerpts and links may be used, provided that full and clear credit is given to DevMountain with appropriate and specific direction to the original content.

<p align="center">
<img src="https://devmounta.in/img/logowhiteblue.png" width="250">
</p>