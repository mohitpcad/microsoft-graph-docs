---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const event = {
  subject: "Let's go for lunch",
  body: {
    contentType: "HTML",
    content: "Does noon work for you?"
  },
  start: {
      dateTime: "2020-02-21T12:00:00",
      timeZone: "Pacific Standard Time"
  },
  end: {
      dateTime: "2020-02-21T14:00:00",
      timeZone: "Pacific Standard Time"
  },
  location:{
      displayName:"Harry's Bar"
  },
  attendees: [
    {
      emailAddress: {
        address:"AlexW@contoso.OnMicrosoft.com",
        name: "Alex Wilbur"
      },
      type: "required"
    }
  ],
  recurrence: {
    pattern: {
      type: "daily",
      interval: 1
    },
    range: {
      type: "numbered",
      startDate: "2020-02-21",
      numberOfOccurrences: 2
    }
  }
};

let res = await client.api('/me/events')
	.post(event);

```