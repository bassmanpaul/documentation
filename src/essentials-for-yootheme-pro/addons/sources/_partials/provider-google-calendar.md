## Google Calendar Source {#google-calendar}

<div class="tm-resource-icon">
    <!--@include: @essentials-for-yootheme-pro/assets/brands/google-calendar.svg-->
</div>

The **Google Calendar Source** feeds data from [Google Calendar](https://calendar.google.com/) supporting [Calendar](#google-calendar-query), [Event](#google-calendar-event-query) and [Events](#google-calendar-events-query) queries.

<!--@include: ./common-provider-settings.md-->

![Google Calendar Configuration](./assets/providers/google-calendar-config.webp)

| Setting | Description | Required |
| --- | --- | :---: |
| *Account* | The Google account which to authenticate with. | &#x2713; |
| *Calendar* | The Google calendar which data to create the source with. | &#x2713; |

### Google Calendar Query

Fetches the Calendar data resolving to a [Google Calendar Type](#google-calendar-type).

| Setting | Default | Description |
| --- | --- | --- |
| *Cache* | `3600` | The duration in seconds before the cache is invalidated and the query re-executed. |

### Google Calendar Event Query

Fetches a single event from the calendar and resolves to a [Google Calendar Event Type](#google-calendar-event-type).

| Setting | Default | Description | Required |
| --- | --- | --- | :---: |
| *Event ID* | | The ID of the event to query. | &#x2713; |
| *Cache* | `3600` | The duration in seconds before the cache is invalidated and the query re-executed. |

### Google Calendar Events Query

Fetches events from the calendar and resolves to a list of [Google Calendar Event Type](#google-calendar-event-type).

| Setting | Default | Description |
| --- | --- | --- |
| *Query* | | Optionaly filter matching terms in the summary, description, location, attendee\'s displayName and attendee\'s email fields. |
| *Single Events Only* | | Whether to expand recurring events into instances and only return single one-off events and instances of recurring events, but not the underlying recurring events themselves. |
| *Order By* | | The order by which to query the events, _Start Time (asc)_ or _Updated (asc)_. |
| *Quantity* | `250` | The maximum amount of events to query. |
| *Time Min / Max* | | Lower and Upper bounds (exclusive) for an event\'s start or end time to filter by. |
| *Cache* | `3600` | The duration in seconds before the cache is invalidated and the query re-executed. |

### Google Calendar Type

Defines the mapping options of a Google Calendar object.

| Option | Description | Type | Filters |
| --- | --- | --- | --- |
| *ID* | Unique identifier of the calendar. | *String* |
| *Summary* | Title of the calendar. | *String* | *Limit* |
| *Description* | Description of the calendar. | *String* | *Limit* |
| *Location* | Geographic location of the event as free-form text. | *String* | *Limit* |
| *Time Zone* | The calendars default time zone. | *String* |

### Google Calendar Event Type

Defines the mapping options of a Google Calendar Event object.

| Option | Description | Type | Filters |
| --- | --- | --- | --- |
| *ID* | Opaque identifier of the event. | *String* |
| *URL* | An absolute link to the event in the Google Calendar Web UI. | *String* |
| *Type* | Specific type of the event, `default`, `outOfOffice`, `focusTime` or `workingLocation`. | *String* |
| *Status* | Status of the event, `confirmed`, `tentative` or `cancelled`. - | *String* |
| *Visibility* | Visibility of the event, `default`, `public`, `private`, or `confidential* | *String* |
| *Summary* | Title of the event. | *String* | *Limit* |
| *Description* | Description of the calendar. | *String* | *Limit* |
| *Location* | Geographic location of the event as free-form text. | *String* | *Limit* |
| *Start* | The (inclusive) start time of the event. For a recurring event, this is the start time of the first instance. | *String* | *Date* |
| *End* | The (exclusive) end time of the event. For a recurring event, this is the end time of the first instance. | *String* | *Date* |
| *Created* | Creation time of the event. | *String* | *Date* |
| *Updated* | Last modification time of the event. | *String* | *Date* |
| *Creator* | The creator of the event. | [Google Calendar Profile Type](#google-calendar-profile-type) |
| *Organizer* | The organizer of the event. | [Google Calendar Profile Type](#google-calendar-profile-type) |
| *Attendees* | The attendees of the event. | [Google Calendar Attendee Type](#google-calendar-attendee-type) |
| *Attachments* | File attachments of the event. | [Google Calendar Attachment Type](#google-calendar-attachment-type) |

### Google Calendar Profile Type

Defines the mapping options of a Google Calendar Profile object.

| Option | Description | Type | Filters |
| --- | --- | --- | --- |
| *ID* | Identifier of the profile. | *String* |
| *Email* | The profile's email. | *String* |
| *Name* | The profile's name. | *String* | *Limit* |

### Google Calendar Attendee Type

Defines the mapping options of a Google Calendar Attendee object.

| Option | Description | Type | Filters |
| --- | --- | --- | --- |
| *ID* | Identifier of the attendee. | *String* |
| *Email* | The attendee's email. | *String* |
| *Name* | The attendee's name. | *String* | *Limit* |
| *Comment* | The attendee's name. | *String* | *Limit* |
| *Response Status* | The attendee's response status, `needsAction`, `declined`, `tentative` or `accepted`. | *String* |
| *Is Organizer* | Whether the attendee is the organizer of the event. | *Boolean* |
| *Is Resource* | Whether the attendee is a resource. | *Boolean* |
| *Is Optional* | Whether this is an optional attendee. | *Boolean* |
| *Additional Guests Count* | Number of additional guests. | *Int* |

### Google Calendar Attachment Type

Defines the mapping options of a Google Calendar Attachment object.

| Option | Description | Type | Filters |
| --- | --- | --- | --- |
| *ID* | Identifier of the attached file. | *String* |
| *Title* | Title of the attachment. | *String* | *Limit* |
| *Mime Type* | Internet media type (MIME type) of the attachment. | *String* |
| *File URL* | URL link to the attachment. | *String* |
| *Icon URL* | URL link to the attachment's icon. | *String* |
