{
  "info": {
    "name": "SendGrid Get Teammates",
    "_postman_id": "581b059c-1c21-419d-b068-b6a688f8fa1e",
    "description": "This endpoint allows you to retrieve a list of all current teammates.\n\n**Note:** The Response Header will include pagination info. For example:\n\nlink: ```<https://api.sendgrid.com/v3/teammates?limit=10&offset=0>; rel=\"first\"; title=\"1\", <https://api.sendgrid.com/v3/teammates?limit=10&offset=10>; rel=\"last\"; title=\"2\", <https://api.sendgrid.com/v3/teammates?limit=10&offset=0>; rel=\"prev\"; title=\"1\"```",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Email",
      "item": [
        {
          "id": "bbb8d58b-c238-485b-8090-564fd9bc0c40",
          "name": "teammates.get",
          "request": {
            "url": "http://api.sendgrid.com/v3/teammates?limit=%7B%7D&offset=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint allows you to retrieve a list of all current teammates.\n\n**Note:** The Response Header will include pagination info. For example:\n\nlink: ```<https://api.sendgrid.com/v3/teammates?limit=10&offset=0>; rel=\"first\"; title=\"1\", <https://api.sendgrid.com/v3/teammates?limit=10&offset=10>; rel=\"last\"; title=\"2\", <https://api.sendgrid.com/v3/teammates?limit=10&offset=0>; rel=\"prev\"; title=\"1\"```"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c7f61c7e-4cfa-4ae0-abc7-7c04f6cbd3e3"
            }
          ]
        }
      ]
    }
  ]
}