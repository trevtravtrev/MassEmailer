# MassEmailer  
A simple mass emailing script. Send an email to an unlimited amount of email addresses in separate emails.  
  
Python 3.8  
Dependencies: Standard Library  
  
How To Use:  
1. Download MassEmailer.py to a folder  
2. Create a .txt file for your email body text  
3. Create another .txt file with your newline separated email list  
4. Open MassEmailer.py and change function parameters to your own  
   - Your email address  
   - Your email address password  
   - Your email provider's server  
   - Number of email addresses from your addresses text file you want to send to  
   - Your email address text file name  
   - Your email body text  
   - Your email subject  
   
Example Use:  
- Make a file called addresses.txt containing 5,000 email addresses  
- Make a file called email.txt that contains just the body of your email  
- Input all your personal parameters into MassEmailer.py  
- For gmail, set the "num_of_addresses" parameter to 100 (100 email/day gmail limit)  
- Schedule this script to run every 24 hours  
- When the script runs once there will be 4,900 email addresses left in addresses.txt, after the second run there will be 4,800 email addresses left in addresses.txt, etc 

Example Code:  
'''
    body_text = parse_email_body('email.txt')  
    email_address_list = parse_email_addresses('addresses.txt', 99)  
    
    for email_address in email_address_list:  
        email_message = create_message('your email subject', 'your email address', email_address, body_text)  
        send_email('your email address', 'your email password', email_message)  
        sleep(1)  
 '''
   
Important Notes:  
- This program has you input how many of the email addresses from your email address .txt file you want to send to each run, this is due to email send limits like gmail's limiting to only sending 100 emails per day. Once the program sends to those email addresses, it deletes the used addresses from your .txt file only leaving the un-used addresses. Keep a copy of your original email list safe elsewhere or you will lose ALL of them once the program has sent an email to them.
