---
swagger: "2.0"
x-collection-name: SendGrid
x-complete: 0
info:
  title: SendGrid Delete Teammates Username
  description: |-
    This endpoint allows you to delete a teammate.

    **Only the parent user or an admin teammate can delete another teammate.**
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /teammates:
    get:
      summary: Get Teammates
      description: |-
        This endpoint allows you to retrieve a list of all current teammates.

        **Note:** The Response Header will include pagination info. For example:

        link: ```<https://api.sendgrid.com/v3/teammates?limit=10&offset=0>; rel="first"; title="1", <https://api.sendgrid.com/v3/teammates?limit=10&offset=10>; rel="last"; title="2", <https://api.sendgrid.com/v3/teammates?limit=10&offset=0>; rel="prev"; title="1"```
      operationId: teammates.get
      x-api-path-slug: teammates-get
      parameters:
      - in: query
        name: limit
        description: Number of items to return
      - in: query
        name: offset
        description: Paging offset
      responses:
        200:
          description: OK
      tags:
      - Email
      - Teammates
    post:
      summary: Add Teammates
      description: |-
        This endpoint allows you to send a teammate invitation via email with a predefined set of scopes, or permissions.

        **Note:** A teammate invite will expire after 7 days, but you may resend the invite at any time to reset the expiration date.

        Essentials, [Legacy Lite](https://sendgrid.com/docs/Classroom/Basics/Billing/legacy_lite_plan.html), and Free Trial users may create up to one teammate per account. There are no limits for how many teammates a Pro or higher account may create.
      operationId: teammates.post
      x-api-path-slug: teammates-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Teammates
  /teammates/pending:
    get:
      summary: Get Teammates Pending
      description: |-
        This endpoint allows you to retrieve a list of all pending teammate invitations.

        **Note:** Each teammate invitation is valid for 7 days. Users may resend the invite to refresh the expiration date.
      operationId: teammates.pending.get
      x-api-path-slug: teammatespending-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Teammates
      - Pending
  /teammates/pending/{token}:
    delete:
      summary: Delete Teammates Pending Token
      description: This endpoint allows you to delete a pending teammate invite.
      operationId: teammates.pending.token.delete
      x-api-path-slug: teammatespendingtoken-delete
      responses:
        200:
          description: OK
      tags:
      - Email
      - Teammates
      - Pending
      - Token
  /teammates/pending/{token}/resend:
    post:
      summary: Add Teammates Pending Token Resend
      description: |-
        This endpoint allows you to resend a teammate invite.

        **Note:** Teammate invitations will expire after 7 days. Resending an invite will reset the expiration date.
      operationId: teammates.pending.token.resend.post
      x-api-path-slug: teammatespendingtokenresend-post
      responses:
        200:
          description: OK
      tags:
      - Email
      - Teammates
      - Pending
      - Token
      - Resend
  /teammates/{username}:
    delete:
      summary: Delete Teammates Username
      description: |-
        This endpoint allows you to delete a teammate.

        **Only the parent user or an admin teammate can delete another teammate.**
      operationId: teammates.username.delete
      x-api-path-slug: teammatesusername-delete
      responses:
        200:
          description: OK
      tags:
      - Email
      - Teammates
      - Username
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---