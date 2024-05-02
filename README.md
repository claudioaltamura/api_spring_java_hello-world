# Spring/Java: API Basic Role-Based Access Control (RBAC) Code Sample

This Java code sample demonstrates **how to implement Role-Based Access Control (RBAC)** in Spring API servers using Auth0.

This code sample is part of the ["Auth0 Developer Resources"](https://developer.auth0.com/resources), a place where you can explore the authentication and authorization features of the Auth0 Identity Platform.

Visit the ["Spring/Java Code Sample: Role-Based Access Control For Basic APIs"](https://developer.auth0.com/resources/code-samples/api/spring/basic-role-based-access-control) page for instructions on how to configure and run this code sample and how to integrate it with a Single-Page Application (SPA) of your choice.

## Why Use Auth0?

Auth0 is a flexible drop-in solution to add authentication and authorization services to your applications. Your team and organization can avoid the cost, time, and risk that come with building your own solution to authenticate and authorize users. We offer tons of guidance and SDKs for you to get started and [integrate Auth0 into your stack easily](https://developer.auth0.com/resources/code-samples/full-stack).

## Examples


export access_token=$(\
curl --request POST \
--url https://dev-tpypdjz8s3hafrlp.us.auth0.com/oauth/token \
--header 'content-type: application/json' \
--data '{"client_id":"9YWxN37dU5WsO9QdNnAXmj1NrbyT6VFZ","client_secret":"WMkRx6OKFKsEjb_IAKgSXcmtN0aKQoGTKgeFHcNYt0W6PDZdxhM2TBIFcX-eB7nD","audience":"http://localhost:8080/api/v1/superheroes","grant_type":"client_credentials"}' | jq --raw-output '.access_token'
)

export access_token="eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6Ik1FSXNFZUhMUUhtYlFYTFZ0bXRUbiJ9.eyJpc3MiOiJodHRwczovL2Rldi10cHlwZGp6OHMzaGFmcmxwLnVzLmF1dGgwLmNvbS8iLCJzdWIiOiI5WVd4TjM3ZFU1V3NPOVFkTm5BWG1qMU5yYnlUNlZGWkBjbGllbnRzIiwiYXVkIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL2FwaS92MS9zdXBlcmhlcm9lcyIsImlhdCI6MTcwOTgxMzM3OSwiZXhwIjoxNzA5ODk5Nzc5LCJhenAiOiI5WVd4TjM3ZFU1V3NPOVFkTm5BWG1qMU5yYnlUNlZGWiIsImd0eSI6ImNsaWVudC1jcmVkZW50aWFscyIsInBlcm1pc3Npb25zIjpbXX0.nPpMZun0fWaxoDbaENAIKl3V-SWr961OSo1cByyoESCYL2xfT6vbScc9PrWkqYhokOPcaAzSKFBpDZZUjxREOmOIhSiC09cIjY7SZNB-RdpwNdIwGtjSjpqDav7D6g1YIYzESK0Fxm4ihtcTTWbeVfEz_IfSjQH0DaMElbjmHYVwx-LyXvf5enlA6krr1i132RgbsEY1F-zrTVZKeGfIgUu4XlnhAYn7OxcjXMvo6b6SkPhDoYasV7ycUZON3dkLMwaOlUTvgeTM7ozaNX2WuF4n-vAB3cnAbTpRCFXjzNbTrMkHa4E8mhsYzGhTFblF9Cp3k246I33Gwznt_iYT_w"

curl --request GET \
--url http://localhost:8081/api/messages/admin \
--header "Authorization: Bearer $access_token" \
--header "content-type: application/json"


curl --request POST \
--url https://dev-tpypdjz8s3hafrlp.us.auth0.com/oauth/token \
--header 'content-type: application/json' \
--data '{"client_id":"BcYubxu9jXhqRRVUZsJaYQHdf0d3lI85","client_secret":"L1VDw7Dpi6n7250oL6VGPBjcJctZKanSDsIJvoDynQoMUIFt2YPhdO2NQ6zy-7SC","audience":"http://localhost:8080/api/v1/superheroes","grant_type":"client_credentials"}'
)



