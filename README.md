API documentation - Create short links with shorten.ly our free API
========================================================

Developer friends, you can create your own short links for free and without registration with our API.

To use our **API**, just send a **GET** request to:

https://api.shorten.ly/?url=\[URL\]

Attaching your original link to be shortened as a parameter.

List of available parameters
----------------------------

| Name                  | Type                                          | Mandatory |
|-----------------------|-----------------------------------------------|-----------|
| url                   | Any URL (Encoded) / max 2000 chars            | yes       |
| alias                 | Type text 2-30 chars                          |           |
| password              | Type text 6-30 chars                          |           |
| expiration_date       | Date format e.g: 2024-12-02 15:00             |           |
| expiration_hits       | Max number of hits before link expires        |           |
| cloak                 | bolean ( yes or no ) / Enable cloaking        |           |
| facebook_pixel        | Facebook pixel ID                             |           |
| x_pixel               | X (Twitter) pixel ID                          |           |
| adword_pixel          | Adword pixel ID                               |           |
| pinterest_pixel       | Pinterest pixel ID                            |           |
| linkedin_pixel        | Linkedin pixel ID                             |           |
| googleanalytics_pixel | Google Analytics pixel ID                     |           |
| googletag_pixel       | Google Tag manager pixel ID                   |           |
| bing_pixel            | Bing pixel ID                                 |           |
| quora_pixel           | Quora  pixel ID                               |           |
| android               | URL (Encoded) destination for android devices |           |
| windows               | URL (Encoded) destination for Widows devices  |           |
| mac                   | URL (Encoded) destination for Mac devices     |           |
| iphone                | URL (Encoded) destination for (iOS) devices   |           |
| linux                 | URL (Encoded) destination for linux devices   |           |


Example of a full request
-------------------------

https://api.shorten.ly/**?url=**https%3A%2F%2Fwww.mylogdomain.com%2Farticle%2Flong-title.html**&alias=**shorty**&expiration\_date=**2024-12-12 12:00**&android=**https%3A%2F%2Fplay.google.com%2Fstore%2Fapps%2Fdetails%3Fid%3Dcom.instagram.barcelona

Example of a JSON response
--------------------------

{
    "success":200,
    "response\_message":"success",
    "short\_url":"https://tin.al/shorty",
    "secret\_password":"AhE5zjHYE",
    "creation\_date":"2024-12-24 12:00"
}   

Rate Limit.
-----------

To ensure the stability of our API and manage unexpected spikes in requests, we have introduced a daily rate limit of 50 short link for unique IP address
