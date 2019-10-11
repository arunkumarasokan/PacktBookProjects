About Helpdesk Agent Assisted Bot:

Agent Assistant Robot will trigger the bot with Hotkey keyboard trigger(Shfit+p) by the Agent.
The bot will then read all unread emails in inbox, checks one email at a time for a subject which contacts 'Ticket' in its text and if a email subject matches this condition it then downloads the excel Attachment.
The excel attachment has the content of the helpdesk ticket.
New workflow called"ReadExcelContent.XAML" is invoked to read the content of the Excel ticket request file and store those in seperate variables.
The output arguments from this workflow are inputed as the input arguments to the next invoked workflow called "ZohoAutomation.XAML". This workflow will create ahelpdesk ticket in Zoho desk application.
Then the next email is processed and so on.
Use Shift+ o to stop the bot

Pre Requiste:

1. Microsoft Outlook with a account already configured
2. Zoho Desk already logged in a Chrome Browser in "Ticket" home page
3. Update the Variable called 'strBrowserTitle' in ZohoAutomation.XAML with the Zoho portal name i.e update the name of your desk inplace of '*HCLTestportal*' (make sure you have the * prefix and suffix)
4. Send  a Mail with Subject "Ticket" and it should have an attachment called 'Request.xlsx' file ( you can find a sample input file in the Attachments folder)
5. Open the Main.xaml in Studio and Run the automation.
6. Use SHIFT + p to Trigger the automation and when prompted SHIFT +o to stop the bot