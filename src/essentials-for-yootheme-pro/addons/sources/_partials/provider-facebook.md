## Facebook Source {#facebook}

<div class="tm-resource-icon">
    <!--@include: @essentials-for-yootheme-pro/assets/brands/facebook.svg-->
</div>

The **Facebook Source** feeds data from [Facebook](https://www.facebook.com/) supporting [Page](#facebook-page-query) and [Page Posts](#facebook-page-posts-query) queries.

<!--@include: ./common-provider-settings.md-->

![Facebook Source Configuration](./assets/providers/fb-config.webp)

| Setting | Description | Required |
| --- | --- | :---: |
| *Account* | The Facebook Account which to authenticate with. | &#x2713; |
| *Page* | The Facebook page from which to create the source content. | &#x2713; |

### Facebook Page Query

Fetches the content from the page resolving to a list of [Facebook Page Type](#facebook-page-type).

![Facebook Page Query](./assets/providers/fb-query-page.webp)

| Setting | Default | Description |
| --- | --- | --- |
| *Cache* | `3600` | The duration in seconds before the cache is invalidated and the query re-executed. |

### Facebook Page Posts Query

Fetches the posts from the page resolving to a list of [Facebook Page Post Type](#facebook-page-post-type).

![Facebook Page Posts Query](./assets/providers/fb-query-page-posts.webp)

| Setting | Default | Description |
| --- | --- | --- |
| *Limit* | `20` | The maximum amount of posts to fetch. |
| *Cache* | `3600` | The duration in seconds before the cache is invalidated and the query re-executed. |

### Facebook Page Type

Defines the mapping options of a Facebook Page object.

![Facebook Page Mapping](./assets/providers/fb-type-page.webp)

| Option | Description | Type | Filters |
| --- | --- | --- | --- |
| *ID* | Unique identifier of this Page. | *String* |
| *Name* | The name of this Page. | *String* |
| *Username* | The alias of this Page, e.g for `www.facebook.com/platform` the username is `platform`. | *String* |
| *Link* | The Page's Facebook URL. | *String* |
| *Category* | The Page's category, e.g. _Product/Service_, _Computers/Technology_. | *String* |
| *Description* | The description of this Page. | *String* | *Limit* |
| *Description HTML* | The description of this Page in raw HTML. | *String* |
| *About* | Information about this Page. | *String* | *Limit* |
| *General Info* | General information provided by this Page. | *String* | *Limit* |
| *Website* | The URL of this Page's website. | *String* |
| *WhatsApp Number* | The WhatsApp number of this Page. | *String* |
| *Total Ratings* | Number of public ratings for this Page. | *Int* |
| *Total Followers* | Number of page followers. | *Int* |
| *Total Mentions* | Number of people talking about this Page. | *Int* |

| Page Person Options | Description | Type | Filters |
| --- | --- | --- | --- |
| *Birthday* | The birthday of this Person Page. | *String* | *Date* |
| *Personal Info* | The personal info of this Person Page. | *String* | *Limit* |
| *Personal Interests* | The personal interests of this Person Page. | *String* | *Limit* |
| *Affiliation* | The affiliation of this Person Page. | *String* | *Limit* |

### Facebook Page Post Type

Defines the mapping options of a Facebook Page Post object.

![Facebook Page Post Mapping](./assets/providers/fb-type-post.webp)

| Option | Description | Type | Filters |
| --- | --- | --- | --- |
| *ID* | Unique identifier of this post. | *String* |
| *Permalink* | The permanent static URL of this post, e.g `www.facebook.com/.../posts/10153449196`. | *String* |
| *Picture URL* | The full size picture attached to this post. | *String* |
| *Message* | The message written in this post. | *String* | *Limit* |
| *From* | The name of the user, page, group, or event that published this post. | *String* |
| *Tags* | The profiles tagged in post message as a custom formated string with _Separator_, _Show Link_ and _Link Style_ arguments. | *String* |
| *Created At* | The time this post was published. | *String* | *Date* |
| *Updated At* | The time this post was last updated, which occurs when a user comments on this post. | *String* | *Date* |
| *Is Published* | Whether this post was published. | *Boolean* |
| *Is Expired* | Whether this post has expiration time that has passed. | *Boolean* |
| *Is Hidden* | Whether this post has been set to hidden. | *Boolean* |
| *Is Popular* | Whether this post is currently popular based on whether the total actions as a percentage of reach exceeds a certain threshold. | *Boolean* |
| *Total Shares* | Number of times this post has been shared. | *Int* |
| *Total Likes* | Number of times this post has been liked. | *Int* |
| *Total Comments* | Number of comments made on this post. | *Int* |
| *Total Reactions* | Number of times people reacted to this post. | *Int* |
| *Parent ID* | Unique identifier of a parent post for this post, if it exists. | *String* |
