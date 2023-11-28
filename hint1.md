# Extracting new posts from a subreddit using the Reddit API

## New post endpoint
- Endpoint: `https://oauth.reddit.com`
- Path: `/r/{subreddit}/new`
- Query parameters: See [here](https://www.reddit.com/dev/api/#GET_new)

## listings query parameters and pagination
Many endpoints on reddit use the same protocol for controlling pagination and filtering. These endpoints are called Listings and share five common parameters: after / before, limit, count, and show.

Listings do not use page numbers because their content changes so frequently. Instead, they allow you to view slices of the underlying data. Listing JSON responses contain after and before fields which are equivalent to the "next" and "prev" buttons on the site and in combination with count can be used to page through the listing.

The common parameters are as follows:

- after / before - only one should be specified. these indicate the fullname of an item in the listing to use as the anchor point of the slice.
- limit - the maximum number of items to return in this slice of the listing.
- count - the number of items already seen in this listing. on the html site, the builder uses this to determine when to give values for before and after in the response.
- show - optional parameter; if all is passed, filters such as "hide links that I have voted on" will be disabled.

To page through a listing, start by fetching the first page without specifying values for after and count. The response will contain an after value which you can pass in the next request. It is a good idea, but not required, to send an updated value for count which should be the number of items already fetched.

## Extracting more than limit
The Reddit API limits the number of posts that can be fetched in a single request. To fetch more posts, you need to use the `limit` and `after` parameter in the API request. The `limit` parameter specifies the number of posts to fetch in a single request, which is set to 25 by default and can go up to 100 at max. The `after` parameter specifies the post ID to start fetching from. 

Using the combination of these two parameters, you can fetch more posts than the limit. For example, if you want to fetch 100 posts, you can set the `limit` parameter to 100. If you want to fetch more than 100 posts, you can set the `limit` parameter to 100 and the `after` parameter to the ID of the 100th post. This will fetch the next 100 posts after the 100th post. You can repeat this process until you have fetched the desired number of posts.

See the [Reddit API documentation](https://www.reddit.com/dev/api/) for more details.