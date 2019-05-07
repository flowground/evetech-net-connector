# ![LOGO](logo.png) EVE Swagger Interface **flow**ground Connector

## Description

A generated **flow**ground connector for the EVE Swagger Interface API (version 0.8.6).

Generated from: https://api.apis.guru/v2/specs/evetech.net/0.8.6/swagger.json<br/>
Generated at: 2019-05-07T17:40:28+03:00

## API Description

An OpenAPI for EVE Online

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### List all alliances

> List all active player alliances<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/alliances/`<br/>
> <br/>
> Alternate route: `/legacy/alliances/`<br/>
> <br/>
> Alternate route: `/v1/alliances/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Alliance`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get alliance information

> Public information about an alliance<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/alliances/{alliance_id}/`<br/>
> <br/>
> Alternate route: `/v3/alliances/{alliance_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Alliance`

#### Input Parameters
* `alliance_id` - _required_ - An EVE alliance ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get alliance contacts

> Return contacts of an alliance<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/alliances/{alliance_id}/contacts/`<br/>
> <br/>
> Alternate route: `/v2/alliances/{alliance_id}/contacts/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contacts`

#### Input Parameters
* `alliance_id` - _required_ - An EVE alliance ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get alliance contact labels

> Return custom labels for an alliance's contacts<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/alliances/{alliance_id}/contacts/labels/`<br/>
> <br/>
> Alternate route: `/legacy/alliances/{alliance_id}/contacts/labels/`<br/>
> <br/>
> Alternate route: `/v1/alliances/{alliance_id}/contacts/labels/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contacts`

#### Input Parameters
* `alliance_id` - _required_ - An EVE alliance ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### List alliance's corporations

> List all current member corporations of an alliance<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/alliances/{alliance_id}/corporations/`<br/>
> <br/>
> Alternate route: `/legacy/alliances/{alliance_id}/corporations/`<br/>
> <br/>
> Alternate route: `/v1/alliances/{alliance_id}/corporations/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Alliance`

#### Input Parameters
* `alliance_id` - _required_ - An EVE alliance ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get alliance icon

> Get the icon urls for a alliance<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/alliances/{alliance_id}/icons/`<br/>
> <br/>
> Alternate route: `/legacy/alliances/{alliance_id}/icons/`<br/>
> <br/>
> Alternate route: `/v1/alliances/{alliance_id}/icons/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Alliance`

#### Input Parameters
* `alliance_id` - _required_ - An EVE alliance ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Character affiliation

> Bulk lookup of character IDs to corporation, alliance and faction<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/affiliation/`<br/>
> <br/>
> Alternate route: `/legacy/characters/affiliation/`<br/>
> <br/>
> Alternate route: `/v1/characters/affiliation/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.

### Get character's public information

> Public information about a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/`<br/>
> <br/>
> Alternate route: `/v4/characters/{character_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get agents research

> Return a list of agents research information for a character. The formula for finding the current research points with an agent is: currentPoints = remainderPoints + pointsPerDay * days(currentTime - researchStartDate)<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/agents_research/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/agents_research/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/agents_research/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get character assets

> Return a list of the characters assets<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/assets/`<br/>
> <br/>
> Alternate route: `/v3/characters/{character_id}/assets/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Assets`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get character asset locations

> Return locations for a set of item ids, which you can get from character assets endpoint. Coordinates for items in hangars or stations are set to (0,0,0)<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/assets/locations/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/assets/locations/`

*Tags:* `Assets`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get character asset names

> Return names for a set of item ids, which you can get from character assets endpoint. Typically used for items that can customize names, like containers or ships.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/assets/names/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/assets/names/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/assets/names/`

*Tags:* `Assets`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get character attributes

> Return attributes of a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/attributes/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/attributes/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/attributes/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Skills`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get blueprints

> Return a list of blueprints the character owns<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/blueprints/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/blueprints/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### List bookmarks

> A list of your character's personal bookmarks<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/bookmarks/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/bookmarks/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Bookmarks`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### List bookmark folders

> A list of your character's personal bookmark folders<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/bookmarks/folders/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/bookmarks/folders/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Bookmarks`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### List calendar event summaries

> Get 50 event summaries from the calendar. If no from_event ID is given, the resource will return the next 50 chronological event summaries from now. If a from_event ID is specified, it will return the next 50 chronological event summaries from after that event<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/calendar/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/calendar/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/calendar/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Calendar`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `from_event` - _optional_ - The event ID to retrieve events from
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get an event

> Get all the information for a specific event<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/calendar/{event_id}/`<br/>
> <br/>
> Alternate route: `/v3/characters/{character_id}/calendar/{event_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Calendar`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `event_id` - _required_ - The id of the event requested
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Respond to an event

> Set your response status to an event<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/calendar/{event_id}/`<br/>
> <br/>
> Alternate route: `/v3/characters/{character_id}/calendar/{event_id}/`

*Tags:* `Calendar`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `event_id` - _required_ - The ID of the event requested
* `token` - _optional_ - Access token to use if unable to set a header

### Get attendees

> Get all invited attendees for a given event<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/calendar/{event_id}/attendees/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/calendar/{event_id}/attendees/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/calendar/{event_id}/attendees/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds

*Tags:* `Calendar`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `event_id` - _required_ - The id of the event requested
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get clones

> A list of the character's clones<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/clones/`<br/>
> <br/>
> Alternate route: `/v3/characters/{character_id}/clones/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 120 seconds

*Tags:* `Clones`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Delete contacts

> Bulk delete contacts<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contacts/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/contacts/`

*Tags:* `Contacts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `contact_ids` - _required_ - A list of contacts to delete
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get contacts

> Return contacts of a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contacts/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/contacts/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contacts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Add contacts

> Bulk add contacts with same settings<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contacts/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/contacts/`

*Tags:* `Contacts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `label_ids` - _optional_ - Add custom labels to the new contact
* `standing` - _required_ - Standing for the contact
* `token` - _optional_ - Access token to use if unable to set a header
* `watched` - _optional_ - Whether the contact should be watched, note this is only effective on characters

### Edit contacts

> Bulk edit contacts with same settings<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contacts/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/contacts/`

*Tags:* `Contacts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `label_ids` - _optional_ - Add custom labels to the contact
* `standing` - _required_ - Standing for the contact
* `token` - _optional_ - Access token to use if unable to set a header
* `watched` - _optional_ - Whether the contact should be watched, note this is only effective on characters

### Get contact labels

> Return custom labels for a character's contacts<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contacts/labels/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/contacts/labels/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/contacts/labels/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contacts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get contracts

> Returns contracts available to a character, only if the character is issuer, acceptor or assignee. Only returns contracts no older than 30 days, or if the status is "in_progress".<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contracts/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/contracts/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/contracts/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contracts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get contract bids

> Lists bids on a particular auction contract<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contracts/{contract_id}/bids/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/contracts/{contract_id}/bids/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/contracts/{contract_id}/bids/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contracts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `contract_id` - _required_ - ID of a contract
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get contract items

> Lists items of a particular contract<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/contracts/{contract_id}/items/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/contracts/{contract_id}/items/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/contracts/{contract_id}/items/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Contracts`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `contract_id` - _required_ - ID of a contract
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation history

> Get a list of all the corporations a character has been a member of<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/corporationhistory/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/corporationhistory/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/corporationhistory/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Calculate a CSPA charge cost

> Takes a source character ID in the url and a set of target character ID's in the body, returns a CSPA charge cost<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/cspa/`<br/>
> <br/>
> Alternate route: `/v4/characters/{character_id}/cspa/`

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get jump fatigue

> Return a character's jump activation and fatigue information<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/fatigue/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/fatigue/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/fatigue/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get fittings

> Return fittings of a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/fittings/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/fittings/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/fittings/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Fittings`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Create fitting

> Save a new fitting for a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/fittings/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/fittings/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/fittings/`

*Tags:* `Fittings`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Delete fitting

> Delete a fitting from a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/fittings/{fitting_id}/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/fittings/{fitting_id}/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/fittings/{fitting_id}/`

*Tags:* `Fittings`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fitting_id` - _required_ - ID for a fitting of this character
* `token` - _optional_ - Access token to use if unable to set a header

### Get character fleet info

> Return the fleet ID the character is in, if any.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/fleet/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/fleet/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/fleet/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 60 seconds

*Tags:* `Fleets`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Overview of a character involved in faction warfare

> Statistical overview of a character involved in faction warfare<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/fw/stats/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/fw/stats/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/fw/stats/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Faction Warfare`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get active implants

> Return implants on the active clone of a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/implants/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/implants/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/implants/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Clones`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### List character industry jobs

> List industry jobs placed by a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/industry/jobs/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/industry/jobs/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/industry/jobs/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Industry`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `include_completed` - _optional_ - Whether to retrieve completed character industry jobs. Only includes jobs from the past 90 days
* `token` - _optional_ - Access token to use if unable to set a header

### Get a character's recent kills and losses

> Return a list of a character's kills and losses going back 90 days<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/killmails/recent/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/killmails/recent/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/killmails/recent/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Killmails`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get character location

> Information about the characters current location. Returns the current solar system id, and also the current station or structure ID if applicable<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/location/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/location/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/location/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Location`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get loyalty points

> Return a list of loyalty points for all corporations the character has worked for<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/loyalty/points/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/loyalty/points/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/loyalty/points/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Loyalty`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Return mail headers

> Return the 50 most recent mail headers belonging to the character that match the query criteria. Queries can be filtered by label, and last_mail_id can be used to paginate backwards<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mail/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 30 seconds

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `labels` - _optional_ - Fetch only mails that match one or more of the given labels
* `last_mail_id` - _optional_ - List only mail with an ID lower than the given ID, if present
* `token` - _optional_ - Access token to use if unable to set a header

### Send a new mail

> Create and send a new mail<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mail/`

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get mail labels and unread counts

> Return a list of the users mail labels, unread counts for each label and a total unread count.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/labels/`<br/>
> <br/>
> Alternate route: `/v3/characters/{character_id}/mail/labels/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 30 seconds

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Create a mail label

> Create a mail label<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/labels/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/labels/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/mail/labels/`

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Delete a mail label

> Delete a mail label<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/labels/{label_id}/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/labels/{label_id}/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mail/labels/{label_id}/`

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `label_id` - _required_ - An EVE label id
* `token` - _optional_ - Access token to use if unable to set a header

### Return mailing list subscriptions

> Return all mailing lists that the character is subscribed to<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/lists/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/lists/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mail/lists/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 120 seconds

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Delete a mail

> Delete a mail<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/{mail_id}/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/{mail_id}/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mail/{mail_id}/`

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `mail_id` - _required_ - An EVE mail ID
* `token` - _optional_ - Access token to use if unable to set a header

### Return a mail

> Return the contents of an EVE mail<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/{mail_id}/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/{mail_id}/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mail/{mail_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 30 seconds

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `mail_id` - _required_ - An EVE mail ID
* `token` - _optional_ - Access token to use if unable to set a header

### Update metadata about a mail

> Update metadata about a mail<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mail/{mail_id}/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mail/{mail_id}/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mail/{mail_id}/`

*Tags:* `Mail`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `mail_id` - _required_ - An EVE mail ID
* `token` - _optional_ - Access token to use if unable to set a header

### Get medals

> Return a list of medals the character has<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/medals/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/medals/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/medals/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Character mining ledger

> Paginated record of all mining done by a character for the past 30 days<br/>
> <br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/mining/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/mining/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/mining/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds

*Tags:* `Industry`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get character notifications

> Return character notifications<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/notifications/`<br/>
> <br/>
> Alternate route: `/v4/characters/{character_id}/notifications/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get new contact notifications

> Return notifications about having been added to someone's contact list<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/notifications/contacts/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/notifications/contacts/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/notifications/contacts/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get character online

> Checks if the character is currently online<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/online/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/online/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 60 seconds

*Tags:* `Location`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get a character's completed tasks

> Return a list of tasks finished by a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/opportunities/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/opportunities/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/opportunities/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Opportunities`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### List open orders from a character

> List open market orders placed by a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/orders/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/orders/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 1200 seconds

*Tags:* `Market`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### List historical orders by a character

> List cancelled and expired market orders placed by a character up to 90 days in the past.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/orders/history/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/orders/history/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/orders/history/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Market`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get colonies

> Returns a list of all planetary colonies owned by a character.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/planets/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/planets/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/planets/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds

*Tags:* `Planetary Interaction`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get colony layout

> Returns full details on the layout of a single planetary colony, including links, pins and routes. Note: Planetary information is only recalculated when the colony is viewed through the client. Information will not update until this criteria is met.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/planets/{planet_id}/`<br/>
> <br/>
> Alternate route: `/v3/characters/{character_id}/planets/{planet_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds

*Tags:* `Planetary Interaction`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `planet_id` - _required_ - Planet id of the target planet
* `token` - _optional_ - Access token to use if unable to set a header

### Get character portraits

> Get portrait urls for a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/portrait/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/portrait/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get character corporation roles

> Returns a character's corporation roles<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/roles/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/roles/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Search on a string

> Search for entities that match a given sub-string.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/search/`<br/>
> <br/>
> Alternate route: `/v3/characters/{character_id}/search/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Search`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `categories` - _required_ - Type of entities to search for
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `search` - _required_ - The string to search on
* `strict` - _optional_ - Whether the search should be a strict match
* `token` - _optional_ - Access token to use if unable to set a header

### Get current ship

> Get the current ship type, name and id<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/ship/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/ship/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/ship/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Location`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get character's skill queue

> List the configured skill queue for the given character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/skillqueue/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/skillqueue/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/skillqueue/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 120 seconds

*Tags:* `Skills`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get character skills

> List all trained skills for the given character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/skills/`<br/>
> <br/>
> Alternate route: `/v4/characters/{character_id}/skills/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 120 seconds

*Tags:* `Skills`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get standings

> Return character standings from agents, NPC corporations, and factions<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/standings/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/standings/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/standings/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Yearly aggregate stats

> Returns aggregate yearly stats for a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/stats/`<br/>
> <br/>
> Alternate route: `/v2/characters/{character_id}/stats/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 86400 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get character corporation titles

> Returns a character's titles<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/titles/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/titles/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/titles/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Character`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get a character's wallet balance

> Returns a character's wallet balance<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/wallet/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/wallet/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/wallet/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 120 seconds

*Tags:* `Wallet`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get character wallet journal

> Retrieve the given character's wallet journal going 30 days back<br/>
> <br/>
> ---<br/>
> Alternate route: `/legacy/characters/{character_id}/wallet/journal/`<br/>
> <br/>
> Alternate route: `/v4/characters/{character_id}/wallet/journal/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Warning: This route has an upgrade available<br/>
> <br/>
> ---<br/>
> [Diff of the upcoming changes](https://esi.evetech.net/diff/latest/dev/#GET-/characters/{character_id}/wallet/journal/)

*Tags:* `Wallet`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get wallet transactions

> Get wallet transactions of a character<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/characters/{character_id}/wallet/transactions/`<br/>
> <br/>
> Alternate route: `/legacy/characters/{character_id}/wallet/transactions/`<br/>
> <br/>
> Alternate route: `/v1/characters/{character_id}/wallet/transactions/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Wallet`

#### Input Parameters
* `character_id` - _required_ - An EVE character ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `from_id` - _optional_ - Only show transactions happened before the one referenced by this id
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get public contract bids

> Lists bids on a public auction contract<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/contracts/public/bids/{contract_id}/`<br/>
> <br/>
> Alternate route: `/legacy/contracts/public/bids/{contract_id}/`<br/>
> <br/>
> Alternate route: `/v1/contracts/public/bids/{contract_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contracts`

#### Input Parameters
* `contract_id` - _required_ - ID of a contract
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return

### Get public contract items

> Lists items of a public contract<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/contracts/public/items/{contract_id}/`<br/>
> <br/>
> Alternate route: `/legacy/contracts/public/items/{contract_id}/`<br/>
> <br/>
> Alternate route: `/v1/contracts/public/items/{contract_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Contracts`

#### Input Parameters
* `contract_id` - _required_ - ID of a contract
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return

### Get public contracts

> Returns a paginated list of all public contracts in the given region<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/contracts/public/{region_id}/`<br/>
> <br/>
> Alternate route: `/legacy/contracts/public/{region_id}/`<br/>
> <br/>
> Alternate route: `/v1/contracts/public/{region_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 1800 seconds

*Tags:* `Contracts`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `region_id` - _required_ - An EVE region id

### Moon extraction timers

> Extraction timers for all moon chunks being extracted by refineries belonging to a corporation.<br/>
> <br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporation/{corporation_id}/mining/extractions/`<br/>
> <br/>
> Alternate route: `/legacy/corporation/{corporation_id}/mining/extractions/`<br/>
> <br/>
> Alternate route: `/v1/corporation/{corporation_id}/mining/extractions/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 1800 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Station_Manager

*Tags:* `Industry`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Corporation mining observers

> Paginated list of all entities capable of observing and recording mining for a corporation<br/>
> <br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporation/{corporation_id}/mining/observers/`<br/>
> <br/>
> Alternate route: `/legacy/corporation/{corporation_id}/mining/observers/`<br/>
> <br/>
> Alternate route: `/v1/corporation/{corporation_id}/mining/observers/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Accountant

*Tags:* `Industry`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Observed corporation mining

> Paginated record of all mining seen by an observer<br/>
> <br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporation/{corporation_id}/mining/observers/{observer_id}/`<br/>
> <br/>
> Alternate route: `/legacy/corporation/{corporation_id}/mining/observers/{observer_id}/`<br/>
> <br/>
> Alternate route: `/v1/corporation/{corporation_id}/mining/observers/{observer_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Accountant

*Tags:* `Industry`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `observer_id` - _required_ - A mining observer id
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get npc corporations

> Get a list of npc corporations<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/npccorps/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/npccorps/`<br/>
> <br/>
> Alternate route: `/v1/corporations/npccorps/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Corporation`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get corporation information

> Public information about a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/`<br/>
> <br/>
> Alternate route: `/v4/corporations/{corporation_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get alliance history

> Get a list of all the alliances a corporation has been a member of<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/alliancehistory/`<br/>
> <br/>
> Alternate route: `/v2/corporations/{corporation_id}/alliancehistory/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get corporation assets

> Return a list of the corporation assets<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/assets/`<br/>
> <br/>
> Alternate route: `/v3/corporations/{corporation_id}/assets/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Assets`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation asset locations

> Return locations for a set of item ids, which you can get from corporation assets endpoint. Coordinates for items in hangars or stations are set to (0,0,0)<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/assets/locations/`<br/>
> <br/>
> Alternate route: `/v2/corporations/{corporation_id}/assets/locations/`<br/>
> <br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Assets`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation asset names

> Return names for a set of item ids, which you can get from corporation assets endpoint. Only valid for items that can customize names, like containers or ships<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/assets/names/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/assets/names/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/assets/names/`<br/>
> <br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Assets`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation blueprints

> Returns a list of blueprints the corporation owns<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/blueprints/`<br/>
> <br/>
> Alternate route: `/v2/corporations/{corporation_id}/blueprints/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### List corporation bookmarks

> A list of your corporation's bookmarks<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/bookmarks/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/bookmarks/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/bookmarks/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Bookmarks`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### List corporation bookmark folders

> A list of your corporation's bookmark folders<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/bookmarks/folders/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/bookmarks/folders/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/bookmarks/folders/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Bookmarks`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation contacts

> Return contacts of a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/contacts/`<br/>
> <br/>
> Alternate route: `/v2/corporations/{corporation_id}/contacts/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contacts`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation contact labels

> Return custom labels for a corporation's contacts<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/contacts/labels/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/contacts/labels/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/contacts/labels/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contacts`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get all corporation ALSC logs

> Returns logs recorded in the past seven days from all audit log secure containers (ALSC) owned by a given corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/containers/logs/`<br/>
> <br/>
> Alternate route: `/v2/corporations/{corporation_id}/containers/logs/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation contracts

> Returns contracts available to a corporation, only if the corporation is issuer, acceptor or assignee. Only returns contracts no older than 30 days, or if the status is "in_progress".<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/contracts/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/contracts/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/contracts/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Contracts`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation contract bids

> Lists bids on a particular auction contract<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/contracts/{contract_id}/bids/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/contracts/{contract_id}/bids/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/contracts/{contract_id}/bids/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Contracts`

#### Input Parameters
* `contract_id` - _required_ - ID of a contract
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation contract items

> Lists items of a particular contract<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/contracts/{contract_id}/items/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/contracts/{contract_id}/items/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/contracts/{contract_id}/items/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Contracts`

#### Input Parameters
* `contract_id` - _required_ - ID of a contract
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### List corporation customs offices

> List customs offices owned by a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/customs_offices/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/customs_offices/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/customs_offices/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Planetary Interaction`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation divisions

> Return corporation hangar and wallet division names, only show if a division is not using the default name<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/divisions/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/divisions/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/divisions/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation facilities

> Return a corporation's facilities<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/facilities/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/facilities/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/facilities/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Factory_Manager

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Overview of a corporation involved in faction warfare

> Statistics about a corporation involved in faction warfare<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/fw/stats/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/fw/stats/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/fw/stats/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Faction Warfare`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation icon

> Get the icon urls for a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/icons/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/icons/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/icons/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List corporation industry jobs

> List industry jobs run by a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/industry/jobs/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/industry/jobs/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/industry/jobs/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Factory_Manager

*Tags:* `Industry`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `include_completed` - _optional_ - Whether to retrieve completed corporation industry jobs. Only includes jobs from the past 90 days
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get a corporation's recent kills and losses

> Get a list of a corporation's kills and losses going back 90 days<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/killmails/recent/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/killmails/recent/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/killmails/recent/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Killmails`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation medals

> Returns a corporation's medals<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/medals/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/medals/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/medals/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation issued medals

> Returns medals issued by a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/medals/issued/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/medals/issued/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/medals/issued/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation members

> Return the current member list of a corporation, the token's character need to be a member of the corporation.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/members/`<br/>
> <br/>
> Alternate route: `/v3/corporations/{corporation_id}/members/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation member limit

> Return a corporation's member limit, not including CEO himself<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/members/limit/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/members/limit/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/members/limit/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation's members' titles

> Returns a corporation's members' titles<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/members/titles/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/members/titles/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/members/titles/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Track corporation members

> Returns additional information about a corporation's members which helps tracking their activities<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/membertracking/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/membertracking/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/membertracking/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### List open orders from a corporation

> List open market orders placed on behalf of a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/orders/`<br/>
> <br/>
> Alternate route: `/v3/corporations/{corporation_id}/orders/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 1200 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Accountant, Trader

*Tags:* `Market`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### List historical orders from a corporation

> List cancelled and expired market orders placed on behalf of a corporation up to 90 days in the past.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/orders/history/`<br/>
> <br/>
> Alternate route: `/v2/corporations/{corporation_id}/orders/history/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Accountant, Trader

*Tags:* `Market`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation member roles

> Return the roles of all members if the character has the personnel manager role or any grantable role.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/roles/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/roles/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/roles/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation member roles history

> Return how roles have changed for a coporation's members, up to a month<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/roles/history/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/roles/history/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/roles/history/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation shareholders

> Return the current shareholders of a corporation.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/shareholders/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/shareholders/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/shareholders/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation standings

> Return corporation standings from agents, NPC corporations, and factions<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/standings/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/standings/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/standings/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation starbases (POSes)

> Returns list of corporation starbases (POSes)<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/starbases/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/starbases/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/starbases/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get starbase (POS) detail

> Returns various settings and fuels of a starbase (POS)<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/starbases/{starbase_id}/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/starbases/{starbase_id}/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/starbases/{starbase_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `starbase_id` - _required_ - An EVE starbase (POS) ID
* `system_id` - _required_ - The solar system this starbase (POS) is located in,
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation structures

> Get a list of corporation structures. This route's version includes the changes to structures detailed in this blog: https://www.eveonline.com/article/upwell-2.0-structures-changes-coming-on-february-13th Note: this route will not return any flex structures owned by a corporation, use the v3 route to have those included in the response. A list of FLEX structures can be found here: https://support.eveonline.com/hc/en-us/articles/213021829-Upwell-Structures<br/>
> <br/>
> ---<br/>
> Alternate route: `/v2/corporations/{corporation_id}/structures/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Station_Manager<br/>
> <br/>
> <br/>
> ---<br/>
> Warning: This route has an upgrade available<br/>
> <br/>
> ---<br/>
> [Diff of the upcoming changes](https://esi.evetech.net/diff/latest/dev/#GET-/corporations/{corporation_id}/structures/)

*Tags:* `Corporation`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation titles

> Returns a corporation's titles<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/titles/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/titles/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/titles/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Director

*Tags:* `Corporation`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Returns a corporation's wallet balance

> Get a corporation's wallets<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/wallets/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/wallets/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/wallets/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Accountant, Junior_Accountant

*Tags:* `Wallet`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation wallet journal

> Retrieve the given corporation's wallet journal for the given division going 30 days back. Note: any journal records having to do with the new navigation structures from the release of Onslaught will not show up in this version. To see those, use the v4 version of this route.<br/>
> <br/>
> ---<br/>
> Alternate route: `/legacy/corporations/{corporation_id}/wallets/{division}/journal/`<br/>
> <br/>
> Alternate route: `/v3/corporations/{corporation_id}/wallets/{division}/journal/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Accountant, Junior_Accountant<br/>
> <br/>
> <br/>
> ---<br/>
> Warning: This route has an upgrade available<br/>
> <br/>
> ---<br/>
> [Diff of the upcoming changes](https://esi.evetech.net/diff/latest/dev/#GET-/corporations/{corporation_id}/wallets/{division}/journal/)

*Tags:* `Wallet`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `division` - _required_ - Wallet key of the division to fetch journals from
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `token` - _optional_ - Access token to use if unable to set a header

### Get corporation wallet transactions

> Get wallet transactions of a corporation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/corporations/{corporation_id}/wallets/{division}/transactions/`<br/>
> <br/>
> Alternate route: `/legacy/corporations/{corporation_id}/wallets/{division}/transactions/`<br/>
> <br/>
> Alternate route: `/v1/corporations/{corporation_id}/wallets/{division}/transactions/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds<br/>
> <br/>
> ---<br/>
> Requires one of the following EVE corporation role(s): Accountant, Junior_Accountant

*Tags:* `Wallet`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `division` - _required_ - Wallet key of the division to fetch journals from
* `from_id` - _optional_ - Only show journal entries happened before the transaction referenced by this id
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Get attributes

> Get a list of dogma attribute ids<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/dogma/attributes/`<br/>
> <br/>
> Alternate route: `/legacy/dogma/attributes/`<br/>
> <br/>
> Alternate route: `/v1/dogma/attributes/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Dogma`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get attribute information

> Get information on a dogma attribute<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/dogma/attributes/{attribute_id}/`<br/>
> <br/>
> Alternate route: `/legacy/dogma/attributes/{attribute_id}/`<br/>
> <br/>
> Alternate route: `/v1/dogma/attributes/{attribute_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Dogma`

#### Input Parameters
* `attribute_id` - _required_ - A dogma attribute ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get dynamic item information

> Returns info about a dynamic item resulting from mutation with a mutaplasmid.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/dogma/dynamic/items/{type_id}/{item_id}/`<br/>
> <br/>
> Alternate route: `/legacy/dogma/dynamic/items/{type_id}/{item_id}/`<br/>
> <br/>
> Alternate route: `/v1/dogma/dynamic/items/{type_id}/{item_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Dogma`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `item_id` - _required_ - item_id integer
* `type_id` - _required_ - type_id integer

### Get effects

> Get a list of dogma effect ids<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/dogma/effects/`<br/>
> <br/>
> Alternate route: `/legacy/dogma/effects/`<br/>
> <br/>
> Alternate route: `/v1/dogma/effects/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Dogma`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get effect information

> Get information on a dogma effect<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/dogma/effects/{effect_id}/`<br/>
> <br/>
> Alternate route: `/v2/dogma/effects/{effect_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Dogma`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `effect_id` - _required_ - A dogma effect ID
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get fleet information

> Return details about a fleet<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `token` - _optional_ - Access token to use if unable to set a header

### Update fleet

> Update settings about a fleet<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `token` - _optional_ - Access token to use if unable to set a header

### Get fleet members

> Return information about fleet members<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/members/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/members/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/members/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Fleets`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `token` - _optional_ - Access token to use if unable to set a header

### Create fleet invitation

> Invite a character into the fleet. If a character has a CSPA charge set it is not possible to invite them to the fleet using ESI<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/members/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/members/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/members/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `token` - _optional_ - Access token to use if unable to set a header

### Kick fleet member

> Kick a fleet member<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/members/{member_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/members/{member_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/members/{member_id}/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `member_id` - _required_ - The character ID of a member in this fleet
* `token` - _optional_ - Access token to use if unable to set a header

### Move fleet member

> Move a fleet member around<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/members/{member_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/members/{member_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/members/{member_id}/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `member_id` - _required_ - The character ID of a member in this fleet
* `token` - _optional_ - Access token to use if unable to set a header

### Delete fleet squad

> Delete a fleet squad, only empty squads can be deleted<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/squads/{squad_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/squads/{squad_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/squads/{squad_id}/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `squad_id` - _required_ - The squad to delete
* `token` - _optional_ - Access token to use if unable to set a header

### Rename fleet squad

> Rename a fleet squad<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/squads/{squad_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/squads/{squad_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/squads/{squad_id}/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `squad_id` - _required_ - The squad to rename
* `token` - _optional_ - Access token to use if unable to set a header

### Get fleet wings

> Return information about wings in a fleet<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/wings/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/wings/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/wings/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Fleets`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `token` - _optional_ - Access token to use if unable to set a header

### Create fleet wing

> Create a new wing in a fleet<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/wings/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/wings/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/wings/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `token` - _optional_ - Access token to use if unable to set a header

### Delete fleet wing

> Delete a fleet wing, only empty wings can be deleted. The wing may contain squads, but the squads must be empty<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/wings/{wing_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/wings/{wing_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/wings/{wing_id}/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `token` - _optional_ - Access token to use if unable to set a header
* `wing_id` - _required_ - The wing to delete

### Rename fleet wing

> Rename a fleet wing<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/wings/{wing_id}/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/wings/{wing_id}/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/wings/{wing_id}/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `token` - _optional_ - Access token to use if unable to set a header
* `wing_id` - _required_ - The wing to rename

### Create fleet squad

> Create a new squad in a fleet<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fleets/{fleet_id}/wings/{wing_id}/squads/`<br/>
> <br/>
> Alternate route: `/legacy/fleets/{fleet_id}/wings/{wing_id}/squads/`<br/>
> <br/>
> Alternate route: `/v1/fleets/{fleet_id}/wings/{wing_id}/squads/`

*Tags:* `Fleets`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `fleet_id` - _required_ - ID for a fleet
* `token` - _optional_ - Access token to use if unable to set a header
* `wing_id` - _required_ - The wing_id to create squad in

### List of the top factions in faction warfare

> Top 4 leaderboard of factions for kills and victory points separated by total, last week and yesterday<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fw/leaderboards/`<br/>
> <br/>
> Alternate route: `/legacy/fw/leaderboards/`<br/>
> <br/>
> Alternate route: `/v1/fw/leaderboards/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Faction Warfare`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List of the top pilots in faction warfare

> Top 100 leaderboard of pilots for kills and victory points separated by total, last week and yesterday<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fw/leaderboards/characters/`<br/>
> <br/>
> Alternate route: `/legacy/fw/leaderboards/characters/`<br/>
> <br/>
> Alternate route: `/v1/fw/leaderboards/characters/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Faction Warfare`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List of the top corporations in faction warfare

> Top 10 leaderboard of corporations for kills and victory points separated by total, last week and yesterday<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fw/leaderboards/corporations/`<br/>
> <br/>
> Alternate route: `/legacy/fw/leaderboards/corporations/`<br/>
> <br/>
> Alternate route: `/v1/fw/leaderboards/corporations/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Faction Warfare`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### An overview of statistics about factions involved in faction warfare

> Statistical overviews of factions involved in faction warfare<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fw/stats/`<br/>
> <br/>
> Alternate route: `/legacy/fw/stats/`<br/>
> <br/>
> Alternate route: `/v1/fw/stats/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Faction Warfare`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Ownership of faction warfare systems

> An overview of the current ownership of faction warfare solar systems<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fw/systems/`<br/>
> <br/>
> Alternate route: `/v2/fw/systems/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 1800 seconds

*Tags:* `Faction Warfare`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Data about which NPC factions are at war

> Data about which NPC factions are at war<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/fw/wars/`<br/>
> <br/>
> Alternate route: `/legacy/fw/wars/`<br/>
> <br/>
> Alternate route: `/v1/fw/wars/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Faction Warfare`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List incursions

> Return a list of current incursions<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/incursions/`<br/>
> <br/>
> Alternate route: `/legacy/incursions/`<br/>
> <br/>
> Alternate route: `/v1/incursions/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Incursions`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List industry facilities

> Return a list of industry facilities<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/industry/facilities/`<br/>
> <br/>
> Alternate route: `/legacy/industry/facilities/`<br/>
> <br/>
> Alternate route: `/v1/industry/facilities/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Industry`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List solar system cost indices

> Return cost indices for solar systems<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/industry/systems/`<br/>
> <br/>
> Alternate route: `/legacy/industry/systems/`<br/>
> <br/>
> Alternate route: `/v1/industry/systems/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Industry`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List insurance levels

> Return available insurance levels for all ship types<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/insurance/prices/`<br/>
> <br/>
> Alternate route: `/legacy/insurance/prices/`<br/>
> <br/>
> Alternate route: `/v1/insurance/prices/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Insurance`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get a single killmail

> Return a single killmail from its ID and hash<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/killmails/{killmail_id}/{killmail_hash}/`<br/>
> <br/>
> Alternate route: `/legacy/killmails/{killmail_id}/{killmail_hash}/`<br/>
> <br/>
> Alternate route: `/v1/killmails/{killmail_id}/{killmail_hash}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 1209600 seconds

*Tags:* `Killmails`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `killmail_hash` - _required_ - The killmail hash for verification
* `killmail_id` - _required_ - The killmail ID to be queried

### List loyalty store offers

> Return a list of offers from a specific corporation's loyalty store<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/loyalty/stores/{corporation_id}/offers/`<br/>
> <br/>
> Alternate route: `/legacy/loyalty/stores/{corporation_id}/offers/`<br/>
> <br/>
> Alternate route: `/v1/loyalty/stores/{corporation_id}/offers/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Loyalty`

#### Input Parameters
* `corporation_id` - _required_ - An EVE corporation ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get item groups

> Get a list of item groups<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/markets/groups/`<br/>
> <br/>
> Alternate route: `/legacy/markets/groups/`<br/>
> <br/>
> Alternate route: `/v1/markets/groups/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Market`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get item group information

> Get information on an item group<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/markets/groups/{market_group_id}/`<br/>
> <br/>
> Alternate route: `/legacy/markets/groups/{market_group_id}/`<br/>
> <br/>
> Alternate route: `/v1/markets/groups/{market_group_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Market`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `market_group_id` - _required_ - An Eve item group ID

### List market prices

> Return a list of prices<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/markets/prices/`<br/>
> <br/>
> Alternate route: `/legacy/markets/prices/`<br/>
> <br/>
> Alternate route: `/v1/markets/prices/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Market`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List orders in a structure

> Return all orders in a structure<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/markets/structures/{structure_id}/`<br/>
> <br/>
> Alternate route: `/legacy/markets/structures/{structure_id}/`<br/>
> <br/>
> Alternate route: `/v1/markets/structures/{structure_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Market`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `structure_id` - _required_ - Return orders in this structure
* `token` - _optional_ - Access token to use if unable to set a header

### List historical market statistics in a region

> Return a list of historical market statistics for the specified type in a region<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/markets/{region_id}/history/`<br/>
> <br/>
> Alternate route: `/legacy/markets/{region_id}/history/`<br/>
> <br/>
> Alternate route: `/v1/markets/{region_id}/history/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Market`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `region_id` - _required_ - Return statistics in this region
* `type_id` - _required_ - Return statistics for this type

### List orders in a region

> Return a list of orders in a region<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/markets/{region_id}/orders/`<br/>
> <br/>
> Alternate route: `/legacy/markets/{region_id}/orders/`<br/>
> <br/>
> Alternate route: `/v1/markets/{region_id}/orders/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 300 seconds

*Tags:* `Market`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `order_type` - _required_ - Filter buy/sell orders, return all orders by default. If you query without type_id, we always return both buy and sell orders
    Possible values: buy, sell, all.
* `page` - _optional_ - Which page of results to return
* `region_id` - _required_ - Return orders in this region
* `type_id` - _optional_ - Return orders only for this type

### List type IDs relevant to a market

> Return a list of type IDs that have active orders in the region, for efficient market indexing.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/markets/{region_id}/types/`<br/>
> <br/>
> Alternate route: `/legacy/markets/{region_id}/types/`<br/>
> <br/>
> Alternate route: `/v1/markets/{region_id}/types/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 600 seconds

*Tags:* `Market`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `region_id` - _required_ - Return statistics in this region

### Get opportunities groups

> Return a list of opportunities groups<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/opportunities/groups/`<br/>
> <br/>
> Alternate route: `/legacy/opportunities/groups/`<br/>
> <br/>
> Alternate route: `/v1/opportunities/groups/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Opportunities`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get opportunities group

> Return information of an opportunities group<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/opportunities/groups/{group_id}/`<br/>
> <br/>
> Alternate route: `/legacy/opportunities/groups/{group_id}/`<br/>
> <br/>
> Alternate route: `/v1/opportunities/groups/{group_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Opportunities`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `group_id` - _required_ - ID of an opportunities group
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get opportunities tasks

> Return a list of opportunities tasks<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/opportunities/tasks/`<br/>
> <br/>
> Alternate route: `/legacy/opportunities/tasks/`<br/>
> <br/>
> Alternate route: `/v1/opportunities/tasks/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Opportunities`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get opportunities task

> Return information of an opportunities task<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/opportunities/tasks/{task_id}/`<br/>
> <br/>
> Alternate route: `/legacy/opportunities/tasks/{task_id}/`<br/>
> <br/>
> Alternate route: `/v1/opportunities/tasks/{task_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Opportunities`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `task_id` - _required_ - ID of an opportunities task

### Get route

> Get the systems between origin and destination<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/route/{origin}/{destination}/`<br/>
> <br/>
> Alternate route: `/legacy/route/{origin}/{destination}/`<br/>
> <br/>
> Alternate route: `/v1/route/{origin}/{destination}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 86400 seconds

*Tags:* `Routes`

#### Input Parameters
* `avoid` - _optional_ - avoid solar system ID(s)
* `connections` - _optional_ - connected solar system pairs
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `destination` - _required_ - destination solar system ID
* `flag` - _optional_ - route security preference
    Possible values: shortest, secure, insecure.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `origin` - _required_ - origin solar system ID

### Search on a string

> Search for entities that match a given sub-string.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/search/`<br/>
> <br/>
> Alternate route: `/v2/search/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Search`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `categories` - _required_ - Type of entities to search for
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `search` - _required_ - The string to search on
* `strict` - _optional_ - Whether the search should be a strict match

### List sovereignty campaigns

> Shows sovereignty data for campaigns.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/sovereignty/campaigns/`<br/>
> <br/>
> Alternate route: `/legacy/sovereignty/campaigns/`<br/>
> <br/>
> Alternate route: `/v1/sovereignty/campaigns/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 5 seconds

*Tags:* `Sovereignty`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List sovereignty of systems

> Shows sovereignty information for solar systems<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/sovereignty/map/`<br/>
> <br/>
> Alternate route: `/legacy/sovereignty/map/`<br/>
> <br/>
> Alternate route: `/v1/sovereignty/map/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Sovereignty`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### List sovereignty structures

> Shows sovereignty data for structures.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/sovereignty/structures/`<br/>
> <br/>
> Alternate route: `/legacy/sovereignty/structures/`<br/>
> <br/>
> Alternate route: `/v1/sovereignty/structures/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 120 seconds

*Tags:* `Sovereignty`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Retrieve the uptime and player counts

> EVE Server status<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/status/`<br/>
> <br/>
> Alternate route: `/legacy/status/`<br/>
> <br/>
> Alternate route: `/v1/status/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 30 seconds

*Tags:* `Status`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Set Autopilot Waypoint

> Set a solar system as autopilot waypoint<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/ui/autopilot/waypoint/`<br/>
> <br/>
> Alternate route: `/v2/ui/autopilot/waypoint/`

*Tags:* `User Interface`

#### Input Parameters
* `add_to_beginning` - _required_ - Whether this solar system should be added to the beginning of all waypoints
* `clear_other_waypoints` - _required_ - Whether clean other waypoints beforing adding this one
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `destination_id` - _required_ - The destination to travel to, can be solar system, station or structure's id
* `token` - _optional_ - Access token to use if unable to set a header

### Open Contract Window

> Open the contract window inside the client<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/ui/openwindow/contract/`<br/>
> <br/>
> Alternate route: `/legacy/ui/openwindow/contract/`<br/>
> <br/>
> Alternate route: `/v1/ui/openwindow/contract/`

*Tags:* `User Interface`

#### Input Parameters
* `contract_id` - _required_ - The contract to open
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Open Information Window

> Open the information window for a character, corporation or alliance inside the client<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/ui/openwindow/information/`<br/>
> <br/>
> Alternate route: `/legacy/ui/openwindow/information/`<br/>
> <br/>
> Alternate route: `/v1/ui/openwindow/information/`

*Tags:* `User Interface`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `target_id` - _required_ - The target to open
* `token` - _optional_ - Access token to use if unable to set a header

### Open Market Details

> Open the market details window for a specific typeID inside the client<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/ui/openwindow/marketdetails/`<br/>
> <br/>
> Alternate route: `/legacy/ui/openwindow/marketdetails/`<br/>
> <br/>
> Alternate route: `/v1/ui/openwindow/marketdetails/`

*Tags:* `User Interface`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header
* `type_id` - _required_ - The item type to open in market window

### Open New Mail Window

> Open the New Mail window, according to settings from the request if applicable<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/ui/openwindow/newmail/`<br/>
> <br/>
> Alternate route: `/legacy/ui/openwindow/newmail/`<br/>
> <br/>
> Alternate route: `/v1/ui/openwindow/newmail/`

*Tags:* `User Interface`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `token` - _optional_ - Access token to use if unable to set a header

### Get ancestries

> Get all character ancestries<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/ancestries/`<br/>
> <br/>
> Alternate route: `/legacy/universe/ancestries/`<br/>
> <br/>
> Alternate route: `/v1/universe/ancestries/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get asteroid belt information

> Get information on an asteroid belt<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/asteroid_belts/{asteroid_belt_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/asteroid_belts/{asteroid_belt_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/asteroid_belts/{asteroid_belt_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `asteroid_belt_id` - _required_ - asteroid_belt_id integer
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get bloodlines

> Get a list of bloodlines<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/bloodlines/`<br/>
> <br/>
> Alternate route: `/legacy/universe/bloodlines/`<br/>
> <br/>
> Alternate route: `/v1/universe/bloodlines/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get item categories

> Get a list of item categories<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/categories/`<br/>
> <br/>
> Alternate route: `/legacy/universe/categories/`<br/>
> <br/>
> Alternate route: `/v1/universe/categories/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get item category information

> Get information of an item category<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/categories/{category_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/categories/{category_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/categories/{category_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `category_id` - _required_ - An Eve item category ID
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get constellations

> Get a list of constellations<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/constellations/`<br/>
> <br/>
> Alternate route: `/legacy/universe/constellations/`<br/>
> <br/>
> Alternate route: `/v1/universe/constellations/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get constellation information

> Get information on a constellation<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/constellations/{constellation_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/constellations/{constellation_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/constellations/{constellation_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `constellation_id` - _required_ - constellation_id integer
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get factions

> Get a list of factions<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/factions/`<br/>
> <br/>
> Alternate route: `/v2/universe/factions/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get graphics

> Get a list of graphics<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/graphics/`<br/>
> <br/>
> Alternate route: `/legacy/universe/graphics/`<br/>
> <br/>
> Alternate route: `/v1/universe/graphics/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get graphic information

> Get information on a graphic<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/graphics/{graphic_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/graphics/{graphic_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/graphics/{graphic_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `graphic_id` - _required_ - graphic_id integer
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get item groups

> Get a list of item groups<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/groups/`<br/>
> <br/>
> Alternate route: `/legacy/universe/groups/`<br/>
> <br/>
> Alternate route: `/v1/universe/groups/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return

### Get item group information

> Get information on an item group<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/groups/{group_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/groups/{group_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/groups/{group_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `group_id` - _required_ - An Eve item group ID
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Bulk names to IDs

> Resolve a set of names to IDs in the following categories: agents, alliances, characters, constellations, corporations factions, inventory_types, regions, stations, and systems. Only exact matches will be returned. All names searched for are cached for 12 hours<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/ids/`<br/>
> <br/>
> Alternate route: `/legacy/universe/ids/`<br/>
> <br/>
> Alternate route: `/v1/universe/ids/`

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get moon information

> Get information on a moon<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/moons/{moon_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/moons/{moon_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/moons/{moon_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `moon_id` - _required_ - moon_id integer

### Get names and categories for a set of ID's

> Resolve a set of IDs to names and categories. Supported ID's for resolving are: Characters, Corporations, Alliances, Stations, Solar Systems, Constellations, Regions, Types<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/names/`<br/>
> <br/>
> Alternate route: `/v2/universe/names/`

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.

### Get planet information

> Get information on a planet<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/planets/{planet_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/planets/{planet_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/planets/{planet_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `planet_id` - _required_ - planet_id integer

### Get character races

> Get a list of character races<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/races/`<br/>
> <br/>
> Alternate route: `/legacy/universe/races/`<br/>
> <br/>
> Alternate route: `/v1/universe/races/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.

### Get regions

> Get a list of regions<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/regions/`<br/>
> <br/>
> Alternate route: `/legacy/universe/regions/`<br/>
> <br/>
> Alternate route: `/v1/universe/regions/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get region information

> Get information on a region<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/regions/{region_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/regions/{region_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/regions/{region_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `region_id` - _required_ - region_id integer

### Get schematic information

> Get information on a planetary factory schematic<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/schematics/{schematic_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/schematics/{schematic_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/schematics/{schematic_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Planetary Interaction`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `schematic_id` - _required_ - A PI schematic ID

### Get stargate information

> Get information on a stargate<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/stargates/{stargate_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/stargates/{stargate_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/stargates/{stargate_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `stargate_id` - _required_ - stargate_id integer

### Get star information

> Get information on a star<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/stars/{star_id}/`<br/>
> <br/>
> Alternate route: `/legacy/universe/stars/{star_id}/`<br/>
> <br/>
> Alternate route: `/v1/universe/stars/{star_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `star_id` - _required_ - star_id integer

### Get station information

> Get information on a station<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/stations/{station_id}/`<br/>
> <br/>
> Alternate route: `/v2/universe/stations/{station_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `station_id` - _required_ - station_id integer

### List all public structures

> List all public structures<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/structures/`<br/>
> <br/>
> Alternate route: `/legacy/universe/structures/`<br/>
> <br/>
> Alternate route: `/v1/universe/structures/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `filter` - _optional_ - Only list public structures that have this service online
    Possible values: market, manufacturing_basic.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get structure information

> Returns information on requested structure if you are on the ACL. Otherwise, returns "Forbidden" for all inputs.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/structures/{structure_id}/`<br/>
> <br/>
> Alternate route: `/v2/universe/structures/{structure_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `structure_id` - _required_ - An Eve structure ID
* `token` - _optional_ - Access token to use if unable to set a header

### Get system jumps

> Get the number of jumps in solar systems within the last hour ending at the timestamp of the Last-Modified header, excluding wormhole space. Only systems with jumps will be listed<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/system_jumps/`<br/>
> <br/>
> Alternate route: `/legacy/universe/system_jumps/`<br/>
> <br/>
> Alternate route: `/v1/universe/system_jumps/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get system kills

> Get the number of ship, pod and NPC kills per solar system within the last hour ending at the timestamp of the Last-Modified header, excluding wormhole space. Only systems with kills will be listed<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/system_kills/`<br/>
> <br/>
> Alternate route: `/v2/universe/system_kills/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get solar systems

> Get a list of solar systems<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/systems/`<br/>
> <br/>
> Alternate route: `/legacy/universe/systems/`<br/>
> <br/>
> Alternate route: `/v1/universe/systems/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag

### Get solar system information

> Get information on a solar system.<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/systems/{system_id}/`<br/>
> <br/>
> Alternate route: `/v4/universe/systems/{system_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `system_id` - _required_ - system_id integer

### Get types

> Get a list of type ids<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/types/`<br/>
> <br/>
> Alternate route: `/legacy/universe/types/`<br/>
> <br/>
> Alternate route: `/v1/universe/types/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return

### Get type information

> Get information on a type<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/universe/types/{type_id}/`<br/>
> <br/>
> Alternate route: `/v3/universe/types/{type_id}/`<br/>
> <br/>
> ---<br/>
> This route expires daily at 11:05

*Tags:* `Universe`

#### Input Parameters
* `Accept-Language` - _optional_ - Language to use in the response
    Possible values: de, en-us, fr, ja, ru, zh.
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `language` - _optional_ - Language to use in the response, takes precedence over Accept-Language
    Possible values: de, en-us, fr, ja, ru, zh.
* `type_id` - _required_ - An Eve item type ID

### List wars

> Return a list of wars<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/wars/`<br/>
> <br/>
> Alternate route: `/legacy/wars/`<br/>
> <br/>
> Alternate route: `/v1/wars/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Wars`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `max_war_id` - _optional_ - Only return wars with ID smaller than this

### Get war information

> Return details about a war<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/wars/{war_id}/`<br/>
> <br/>
> Alternate route: `/legacy/wars/{war_id}/`<br/>
> <br/>
> Alternate route: `/v1/wars/{war_id}/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Wars`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `war_id` - _required_ - ID for a war

### List kills for a war

> Return a list of kills related to a war<br/>
> <br/>
> ---<br/>
> Alternate route: `/dev/wars/{war_id}/killmails/`<br/>
> <br/>
> Alternate route: `/legacy/wars/{war_id}/killmails/`<br/>
> <br/>
> Alternate route: `/v1/wars/{war_id}/killmails/`<br/>
> <br/>
> ---<br/>
> This route is cached for up to 3600 seconds

*Tags:* `Wars`

#### Input Parameters
* `datasource` - _optional_ - The server name you would like data from
    Possible values: tranquility, singularity.
* `If-None-Match` - _optional_ - ETag from a previous request. A 304 will be returned if this matches the current ETag
* `page` - _optional_ - Which page of results to return
* `war_id` - _required_ - A valid war ID

## License

**flow**ground :- Telekom iPaaS / evetech-net-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
