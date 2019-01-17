# Intro

The purpose of this document is to provide documentation on the integration process for XSocialCampaigns.
We want to be able to handle all the incoming integrations properly while still being able to develop the
other projects we have in our pipeline. While Jose and I both know what our plan is we feel like having everyone
aware of this information will help us help you.

# The Integration Process at a glance

> All the information in one organized place is the goal.

This implies that a parser is already in place for the current method the client wants.
For new clients or clients that are adding parsers to their campaigns please see the parser section.

For the purpose of integration we do not care about the in coming order process or the lander creation (see exceptions).
We pick up right as the lander is made and ready to go.

## Steps For Integration

- Lander is done and handed over to development.
- Development will seek the proper integration information to generate tasks (see note)
- Development will add integration tasks to the integration queue.
- Development will clear out integration queue once a day.
- Development will send emails to client to confirm that the integration was successful.

Our currently daily schedule will consist of us seeking information for integration starting at 3pm each day to generate
a to-do list.
We will be completing that list between 8am and 9am each morning. Our hope is that by standardizing this process we can later fully automate the integration process.

**The note:** Intake desk sends posting docs for each campaign they need integrated. It would be nicer if everyone did this.

# Creating Parsers

Our system uses different types of parsers for integration. This is most time intensive part of this system.
Thankfully we normally only create one parser for client and most use an intake system such as captorra, ice or IntakeDesk

## Steps For Parsers

- Development team gets informed a new client is being onboarded or an existing client is now requesting integration.
  > Odds are we can use an existing parser most of the time. We really only need to create new ones for custom systems.
- Development team gets in contact with client to get requirements for paser. Such as which endpoint, data format, custom fields ect.
- Development team creates parser.
- Normal integration process takes over at this point.

# Creating SpreadSheets

While parsers are the most popular types of integration we can also generate spreadsheet reports of all leads for a certian lander.

All spreadsheets activate at 5am UTC time.

We do have a generic version of a spread sheet that we can generate as well as create custom templates based on
a client request.

# Exceptions

The production pipeline does not matter to the development team until it hits integration ready unless:

- Custom scripts are needed on the lander.
  > Such as the rightsignature, rerouting landers based on questions, DQ that production can't do)
- **It is a new client. Please do tell us!**
