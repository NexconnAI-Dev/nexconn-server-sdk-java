

# CommunityChannelMessageSendRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**fromUserId** | **String** | Sender user ID. Non-members can send through the server API, but push display works best when the sender has an access token. |  |
|**toChannelIds** | **List&lt;String&gt;** | Target community channel IDs. Up to 3 community channels are supported per request. |  |
|**toUserIds** | **List&lt;String&gt;** | Recipient member user IDs for a targeted community message. Only effective when sending to a single community channel. |  [optional] |
|**messageType** | **String** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. |  |
|**content** | **String** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. |  |
|**pushContent** | **String** | Push notification text for offline recipients. Optional for built-in user content messages and required for push-enabled custom or notification messages. |  [optional] |
|**pushData** | **String** | Custom push payload data. Exposed as &#x60;appData&#x60; on mobile push payloads. |  [optional] |
|**shouldPersist** | **Integer** | Whether to store the message in community message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. |  [optional] |
|**isCounted** | **Integer** | Whether to count this message as unread for offline users. &#x60;1&#x60; counts as unread and &#x60;0&#x60; does not. |  [optional] |
|**hasMention** | **Integer** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. |  [optional] |
|**contentAvailable** | **Integer** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. |  [optional] |
|**pushExt** | **String** | Extended push configuration (JSON string as accepted by the server &#x60;CommunityChannelMsgSendInput&#x60;). |  [optional] |
|**subchannelId** | **String** | Target subchannel ID. If omitted, delivery follows the app&#39;s default community-channel behavior. |  [optional] |
|**hasMetadata** | **Boolean** | Whether to enable message metadata for this message. |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** | Custom message metadata entries. Only effective when &#x60;hasMetadata&#x60; is &#x60;true&#x60;. |  [optional] |



