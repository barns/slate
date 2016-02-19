# Errors

JsonGeocode may occasionally respond with an error code when something goes wrong:


Error Code | Meaning
---------- | -------
400 | Bad Request -- You've forgotten or misspelled a required parameter
401 | Unauthorized -- You didn't provide an API key, or the one you provided isn't valid
406 | Not Acceptable -- Make sure you're requesting json - we only provide data in this format!
429 | Too Many Requests -- You've hit your request limit for this month. You can wait for your renewal date, or upgrade your subscription. Up to you.
500 | Internal Server Error -- There seems to be an issue on our end. We'll take a look into it right away.
503 | Service Unavailable -- We're working on improving the api, so we're offline for a bit. Please try again later.
