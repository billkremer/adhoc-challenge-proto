# Ad Hoc Code Challenge:
## Proto: a MPS7 Decoder

This is a response to a code challenge.

Created on or around June 2 - 4, 2019


# Ad Hoc Code Challenge:
## Proto: a MPS7 Decoder

This code challenge was completed using JavaScript.  
While this was achieved on the front-end / client-side, the javascript could easily be put into back-end / server-side to obfuscate the logic. 

# Warning:
There is a major concern that the data in the provided txnlog.dat file does not provide accurate data.
The number of records is shown as 71, however there are 72 records present in the file.

After a discussion with the AdHoc Homework team (see screenshots), the 71 is correct and the 72nd record is possibly corrupted data, even though it appears to conform to the proper format.  
It appears to be a Credit that mirrors the debit from record 61.
If this were an actual client, I would want secondary confirmation that the 72nd transaction record did not actually occur, or that it was possibly present in another transaction log.

This can be made apparent by changing line 100 from:
        for (let i = 0; i < numRecords; i++) { 
to
        for (let i = 0; i < numRecords+1; i++) { 

using numRecords+2 goes above the offset.

To operate the code:
First open the MPS7.html file in an internet browser.
Click on 'Choose File'
Select MPS7 data file.
Click on 'Decode'

The selected questions and answers will appear above the log.

What is the total amount in dollars of debits?  $18,203.70
What is the total amount in dollars of credits?  $10,073.36
How many autopays were started?  10
How many autopays were ended?  8
What is balance of user ID 2456938384156277127?  $0.00


