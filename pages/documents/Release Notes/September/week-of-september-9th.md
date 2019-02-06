---
pagename: Week of September 9th
categoryName: Release notes
subCategoryName: 2018
indicator: both
subtitle: ''
level3: September
permalink: release-notes-2018-september-week-of-september-9th.html
isTutorial: false
isNew: false
date: 2019-02-06 17:29:42 +0200
published: false

---
These release notes include new features arriving to LiveEngage during September 2018. Exact delivery dates may vary, and brands may therefore not have immediate access to all features on the date of publication.

**Please contact your LivePerson account team for the exact dates on which you will have access to the features.**

{: .important}
The timing and scope of these features or functionalities remain at the sole discretion of LivePerson and are subject to change.

## New functionality

### Post Conversation Survey and Bot Studio

The Post Conversation Survey Bot gives brands the ability to collect feedback from consumers at the end of a conversation, without utilizing the time of a human agent. The bot can ask specialized questions, designed to provide CSAT, FCR and NPS metrics for the brand, questions that reflect a brand’s custom KPIs, or free text questions. This feature is ideal for brands to measure agent and skill performance and identify opportunities to improve on quality targets.

  
![](https://lh6.googleusercontent.com/6XFiYgolPNI6rvdTdp2lNfm_r6A5h3RYvuca42xltxPk2eGqvJmuQ5uN4sIrbquwnsmjZ9TU93AZ_GDh58kYLA5EG8glKzvKREFkMU1NNbAKrj2FvoWG_BmSrj_7RItZVv_3-STM =249x413)

The post conversation survey bot is available for Messaging customers on mobile app, web, ABC, Facebook. SMS is coming soon in September.

### Survey Flow

  
![](https://lh6.googleusercontent.com/qDWKcxiC2EM6MxeYocQaX5HwCzq2ESMi0BdgRvEfBO33Ol5hW_LfMbHsE47Td_DfBWp7R7WZRbxKnpDoGESaHTcgEd2pqRxtRJVDY-HdregQsB9pxAjmg2yN58GpyR8BKq7sry3M =177x310)![](https://lh6.googleusercontent.com/N03qxBjBOMQhvctu9A9Heip9LMvYHJo6s6NB6lPSbnD6XaSnyNGaxHNbkdloZGS-JtHNhQEWDIjaK6RLzlblyinpvvA7RFn_k48-LlL3wKLlDENA1u0lZABGOgK3hiu8c2Rpqe_y =177x311)![](https://lh3.googleusercontent.com/1u7ZtObSnieNGP1qXXx5n4TIrPxkJ9c3BcLfPyIyRKwkvbQAKIP6cXKsCl05hHtUS0jcmzS1W6qazYOdbb-Ze24DycmMZdVmgpdVEF4tqEX-akyodqlyk-DW1nOJAO94k973hp1S =172x304)

1. Once the conversation ends the survey is automatically triggered and Bot sends the greeting message
2. The Bot starts to send the questions one by one based on the brand configuration. Questions can be quick replies, structured content or simple text.
3. Once the consumer finished answering the questions or upon survey timeout, the survey will be closed with a closing message

## How to create a survey using the Bot Studio

### Step 1 - Log in to the Bot Studio

Log in to the Bot Studio using the following link [https://va.routingbot.ext.liveperson.net/login](https://va.routingbot.ext.liveperson.net/login "https://va.routingbot.ext.liveperson.net/login")

Make sure to use your account Admin credentials.

![](https://lh6.googleusercontent.com/0PBXW2dEUdzTiZk67iWQfsJOsKjnRU0OYJR4G4_1mx1IEbZ5LU8uSR-QmOYkqzVwNJh5iL7VBlK3K1_-fA_EiDhN8SVH73BmrykfsS8G2raM-tI5XejLe506vf6Md6IcE2XU9W9b =461x439)

### Step 2 - Create a Bot and first survey

Once logged in to the Studio, create a new Bot under the Survey Bots tab.

![](https://lh4.googleusercontent.com/92YHex55zVbfDs_2YpiR5DqKFoMdwx7agSh3Ixu-uCgJhs8Bi3tuOvIMAomq4NlOpg__A4nkqgB6dsBxufyXVC4p0FyLJX5Hm_GxK5PkHKf6Q5GcLlav4UPBITgZcM2jjSZnzboV =563x299)

Once the bot is created, Enter the Bot’s Survey gallery and press the “Add Survey” button to create a new survey.

Select the skills on which the survey will be triggered once the conversation is closed.  
  
  
![](https://lh4.googleusercontent.com/dOn-c8lzUeb_M_ubjClsACAIv6pYJQoDkIyD757meNdaNvpddX5mBE06HZybdpMi2VGIFvEF3orFc3CshFOgwa4N3gVKORHeL6P_ERcNawuYdBd9zhirtDuMoS6gTuVYcTw-NTEo =617x178)

### Step 3 - Define the survey flow with Sequences and Brick

This step will instruct you on how to create a survey flow using the Bot Studio Editor.

#### **What is a survey?**

A survey is a collection of sequences where each sequence is built out of bricks (questions).

#### **What is a sequence?**

A sequence is essentially a business flow. For example, If I would like to collect the user’s name and age at the beginning of the survey, I would create a sequence and would name it “Personal info”. I would then go and define a few Bricks under my “Personal info” sequence for collecting the required user information.

#### **What are bricks?**

Bricks are visual elements such as Text bubbles, Structured content with Images and buttons and Text bubbles with quick replies.

#### **What are Predefined bricks?**

Predefined bricks are the NPS, CSAT and FCR bricks. They are called predefined since the bot designer can’t edit their structure (for example number of quick replies) but can only edit their content (for example question text or quick reply names). By definition, a survey can have only one predefined of each type in a single survey. (One CSAT, One NPS & One FCR question per a single survey)

#### **What is an Unassigned Sequence?**

An unassigned sequence is a sequence that is not referenced by the main tree of the survey (Orphan sequence). It would appear at the bottom of the Sequence List in the Unassigned Sequences section.

#### **Which actions are available?**

The available actions that could be defined for each quick reply or button can perform one of the following activities:

* **Go to sequence** - If a quick reply is defined to “Go to sequence” when pressed, it would trigger the first brick in the target sequence using a “next” command.
* **Continue sequence** - This would tell the Bot Studio UI that another brick should come right after the brick in which this action is defined.
* **End conversation** - triggers an “end conversation message” that is assigned with the terminate command in the JSON.

### Step 4 - Set the Survey timeout and general settings

#### **Survey timeout**

To set the survey timeout, head to the survey settings and enter the amount of time you wish the survey to be live before the survey bot ends it with a timeout message.

The survey timeout is calculated from the moment the survey starts until it reaches the timeout.

#### **Survey skip phrases**

In the settings, you can set the phrases that could help the consumer to skip the survey. If the consumer would enter one of the set phrases (exact phrase, not case sensitive) the survey skip message would be written to the conversation and the bot would end the survey.![](https://lh4.googleusercontent.com/7L9fWgT9QYG9_fqrOB85K-7fvK_S3fgsDTU_t3unN9j1ZJ25zlHwiKtYFFgieqJXqi_sElWQQz8vKdJCfS8zR_1LSKakAQKeDaGt1HF1_HtdvsWlvxLwUvDv3OWoQS3C6d26Niwu =466x401)

### Step 5 - Reaching a valid survey for Publishing

If you wish to know that your survey is valid for publishing, make sure that the survey has no warning icons on bricks and has no Unassigned Sequences.

In the image below there are a few errors that prevent the survey from being published:

1. Some of the bricks are missing an Action definition (Go to sequence etc’).
2. Some of the bricks are missing essential information such as the question text.
3. The survey has an unassigned sequence.

![](https://lh4.googleusercontent.com/Zgqnxrv3c-1wb2NfL-JF9AeaelVnFN7xoxZNc267FXGLXNWjRXt5yPdFaTP9FjceJ1_22qjbQ-eFvxQacbYALldKqL7mVkdQOXv9GV8kIumQXada0WAkxVl4Jo4VS92TGjQbBSng =624x337)

Attempting to Publish this survey will fail with a Bot Studio error message.

Once the survey contains no warnings, hit the Publish button to have the survey loaded to you LiveEngage account. At this point, if the survey is defined as active, it would already be live for your users.

### Step 6 - Trigger the survey

In order to trigger the survey, start a conversation on the account and skill on which you’ve defined the survey and bring the conversation to an end, either from the consumer or the agent side. Once the conversation closes the survey will be triggered and the agent workspace would show the caption - “Survey in progress”

![](https://lh3.googleusercontent.com/pjfSphxX4_xTE8wxByQmATXL_Z7oq35O760ff2DsjRyz6t7YBOXcrha4fiVR_uZ4786dvS6USALApT0f20lGCqsIREBnJkq7QU_qX9X4hdhgpfuBCLUwGpaNCz6j5mM4FZ5WJwo6 =535x611)

While the survey is active the agent won’t be able to write in the conversation. The survey would end when the consumer finishes entering the survey or when the survey timeout is reached. In cases of an error with the survey flow or the survey bot, LiveEngage will close the survey after 48 hours as part of a conversation cleanup process.

For more information on this feature, please refer to the [User Guide](https://s3-eu-west-1.amazonaws.com/ce-sr/botstudio/Conversation+Survey+-+Configuration+Guide.pdf).

Please also refer to the Release notes for [Post Conversation Survey Reporting](https://s3-eu-west-1.amazonaws.com/ce-sr/Release+Notes/2018/Release+Notes+Week+of+Aug+6th+2018+-+Published+1+Aug+2018.pdf)

# 

### Facebook Messenger and Apple Business Chat support for Post Conversation Survey (LE-90206, LE-89069)

The post conversation survey is now supported for the Facebook Messenger and Apple Business Chat connectors, giving brands the ability to collect feedback from consumers at the end of a conversation. It is delivered in a conversational experience to drive higher completion rates.

**It contains:**

* Special predefined questions - CSAT, FCR & NPS
* Custom brand KPIs
* Free text questions
* Survey logic based on consumer responses
* Full reporting & analytics on survey responses, answer distribution and funnel metrics

**Survey Experience in Facebook Messenger:**

For use in Facebook Messenger, you can configure the survey through the Bot Studio using LE structured content and it will be seamlessly translated into Facebook’s templates (quick replies, cards etc.) Brands can configure one survey and apply it to all channels, or they can configure separate surveys per channel (each channel should have a separate skill).

**Survey Experience in Apple Business Chat:**

LiveEngage automatically translates rich surveys into textual surveys for the ABC channel.

Brands can configure one survey and apply it for all channels or they can configure separate surveys per channel (each channel should have a separate skill).

When configuring the survey in the Bot Studio, the brand must configure the ‘fallback text’ on every rich element, this way they can customize the experience for textual channels.

**Please note:** This feature requires enablement - please contact your LivePerson account team.

**Limitations**

* Quick replies will have the 'alt' property (for text fallback) defined in UMS version 3.15 which will only be rolled out in October - this means that in the first version of surveys for ABC, quick replies will not be supported.

**![](https://lh6.googleusercontent.com/WE3_O40iyu3MUZtWflHWV4hd5faBye0jA0RTxQvY9YMFW2UC_tClRB18oIYVxHq6UjDK9ItbL0mcUkJiij9lk0dXaSzJD-6JQUIXkD6S_aotIMx3qmyzdWW9dS8QLEcVxhkqmFin =207x355)![](https://lh4.googleusercontent.com/HxAYSm5XVB7FrXYdp4-Z0ueZxaQa_vfLHp7ELiFvUI0-mkVhTsMg6rE45zur3SiQj9ZJynT3PDapE8SBTfrt04AJci9VPyoiSsbIvCPjEK3BwQIhfGsn2A6VPBwVFc-PP9_nUhiw =200x355)**

### Audio Message - Facebook Messenger and Apple Business Chat Support (LE-89904)

The Apple Business Chat and Facebook Messenger connectors to LiveEngage now support the following audio message flow:

* Consumer on ABC or FBM records and sends an audio message to an agent on LE
* Agent receives an audio type message and can play the message the consumer has recorded on the agent workspace
* Agent can play and replay audio messages sent by consumers for open and closed conversations (agent cannot record audio messages)
* Consumer can replay his own audio messages (speaker only) - as supported on each channel
* LiveEngage does not convert voice to text

Audio messaging is currently still in beta, due to the fact that the audio files are not yet going through a sanitation process in LiveEngage (sanitation will be added later in September). Customers that are interested in joining the beta program should contact Or Garmolin to sign the beta agreement.

**Supported formats and sizes:**

* Recording length supported by UMS is 2 minutes (a larger file will be rejected and an error message will be sent to the consumer)
* File size supported by UMS is up to 5MB
* Supported formats: connectors will convert the connectors audio file type to MP3

**Limitations**

* Audio files longer than 2 minutes will be rejected - error will be shared with consumers
* Audio message will not be converted to text - agent will only be able to play and listen to the the audio file

**Please note:** This feature requires enablement - please contact your LivePerson account team.

**![](https://lh4.googleusercontent.com/NlgBokOfMkG8JhetWi7yZNIVyLgVHOb1TnfgMm8tFVxQntYLkuJfn7BuqlcISha9KZbW3p1P1DJEkWTu4G5steFD7B3yuzX3xkEsoqcZUnD17WmdkLhI9bF4pl9zGupUJ0PsQnnL =167x296)![](https://lh5.googleusercontent.com/tj026IxJk3SXveUuLi1a7BwkJtnnl21d2P0hhGaPCZwmi3157a4v1nkLr2Iabxf1aX_KKdKgC8qKNoATMBFlpXFx-Zphh1tln1tNGbvguW75UF_9pLM0IhdvktVrafwZWCb0qeIf =167x296)**

### 

### Messaging Operations

### Dynamic text (macros) in Predefined Content for messaging (LE-91252)

This feature enables users to set up dynamic text, such as agent name or skill name, within the predefined content template for messaging conversations. Predefined Content helps automate some of the agent’s freehand typing, which will result in better agent productivity.

#### **Setting**

Accounts may now use the dynamic text option in the “Manage Predefined Content” screen (campaign footer) for messaging as well as chat.

The supported dynamic texts are (as available for chat today):

1. Skill Name - $!{skill.name}
2. Skill Description - $!{skill.description}
3. Agent Name - $!{operator.displayname}
4. Agent Nickname - $!{operator.nickname}
5. Agent Email - $!{operator.email}

The feature is also supported for rich content and quick replies (accounts can use the macros within their code).

#### **Agent experience**

1. Agent can choose a Predefined content template containing a dynamic text, or type a dynamic text freehand
2. Once template with the dynamic text is chosen, its value is inserted within the text editor
3. The dynamic text value will be shown in the transcript area immediately after the agent sends the message.

**Please note:** this functionality is available only through the web agent (LE UI) and not directly through the API.

Configuration of predefined content:

**![](https://lh4.googleusercontent.com/2PLnAuhLcSChiwPmQeP-Qpo2ayNe4U2523UUZa62n3g7Nd-oEGliDxqKSb6ttWT_1cHAG3yJ2VCCow8KGJG_ddm7yp79KPU94MJL8yQJ3BEAoajA9royEpOOCGkrixhauQGBmgIx =295x426)**

The text editor before sending the message:

  
![](https://lh5.googleusercontent.com/icyZ-VyWQBiemUMqBBhbOg8qLfKmBairx5dZ4oIIIPY-g7ltpI5iGunQEOPDjd8KF1rqE4qaFCDrUbloen6l-QNUiGJjyNYBGQxhTJcJl4JrHCiaVVnDhYb4Qw0OBK5LmlWjMaqI =316x529)

The message after it is sent:

  
![](https://lh3.googleusercontent.com/FbSce4Og71ZlboiDmK65ezba6NAQzpyCLEXr3B6b3lZQYbBmi39K9O8VZRe-uLtqCcyjq1va9TbEO3Z9PYzvFsS6d5XMY_Cck7W8Q91UFZtgU9t0R3Eiif25Iz10yHo9VkilmE-k =324x479)

### 

### Resume conversations without time restrictions (LE-83882)

Agents and agent managers now have the ability to resume conversations with consumers at any point in time after the conversation is closed. Previously, the time frame limit for resuming a conversation was just 14 days after the conversation closed. Now, the conversation can be resumed for the length of time it remains on the LiveEngage database (13 months).

Following message shall not appear anymore :

![](https://lh5.googleusercontent.com/TnFokrPgiq-l32DQUNOFjx_T-QagrYebE3RzMarF1d2jxNNa-7V-rDccZLdvraUxMSH_vhz6FJUUDCSuEOSJa2I6NIsYTvCyHYCtLVBfkrBsgH10SafbtaA7TEL_TxONSbbuKkRw =624x291)

### Remove 'description' from Agent Widget SDK setConsumerProfile (AE-374)

The ‘description’ property cannot be updated by an agent using the Consumer Profile API as it is reserved for the consumer’s external ID. When an agent updates the 'description', assuming it is used to describe the user, that property populates the 'Consumer ID' field in the consumer info widget. This causes unexpected behavior for the agent.

In order for brands not to misuse it, we need to prevent agents from setting that property when updating the consumer profile. Therefore, the field ‘description’ is removed from the update API. If it is sent as part of the setUserProfile, it will be ignored.

# Enhancements

## Chat Back-end Server

### Remove interaction content access for LPA users (89500)

Remove access to interaction content by having the following settings/permissions enforced on LPAs upon login: change LPA user privileges from 8, 10, 33 to 9, 10, 33.

### Convert Date to Long with insufficient data (93480)

Some customers send SDEs without last payment date object, that should have a year, month, day fields. When Denver issue a call to IDP it gets LPGWT, without lastPaymentDate.

Denver tries to convert to Long and fail.

Solution: If one of the fields is null - don't convert the object to long, but return null.

### Adding FaaS PostSurvey Implementation (92041)

Enabling the usage of FaaS for the Denver PostSurvey Email Transcript notification.

### GDRS - Ticketing Implementation AppServer (89437,92462,89441,85057)**:**

As part of the “Right to be Forgotten” epic, consumer related data needs to be masked from existing tickets via a new dedicated GDRS API, if a RTBF request arrives from a brand’s consumer. This enhancement is applicable only for legacy account customers with Ticketing system.

* The tickets themselves will not be deleted but rather the metadata which links the tickets to the requesting consumer will be masked: ticket message (email) headers, UDEs (legacy SDEs) and ticket contact info.
* Attachments in relevant tickets should be completely deleted.
* The APIs for masking data will be available only for live accounts.
* Legacy accounts which upgraded to LE (i.e. those who have not created a new site for LE), won't have ticketing ​system available to them. If they moved to a new site, their legacy one will remain live for 13 months and they should be able to mask consumer personal data during that time.

# Bug Fixes

## Chat Back-end Server

### Password policy - update passwords blacklist in PasswordPatterns.txt (91288)

This bug is applicable to the AppServer and enforces by default the prevention of using commonly used password phrases when setting a new password as an authenticated user to LE.

### Open redirect vulnerability - sales/base.liveperson.net (88039)

Remove the risk that attackers could use this link in order to redirect users for malicious sites.

This is part of the effort for limiting the allowed redirection targets to same-origin resources and white-listed domains if needed.

## Agent Workspace

### Real time dashboard not refreshing automatically (LE-92947)

On LiveEngage -> Visitors tab -> Real Time Databar and associated dashboard does not refresh automatically (unless the page has been refreshed manually). This bug is a result of the previous LiveEngage version and is now fixed, so the dashboard will be refreshed automatically every 10 seconds.

![](https://lh4.googleusercontent.com/dKoJ9YTKT2hRzh1hl25wz0pjLw3mMq-Gsl3AYxFN3oxbySKDrZfHib8NkhrIyRCrZnpu8Z1I70_E8Q5QTLEbAJI6RtgWS4WW_RvVimxfwNB0PpAVqTG9rhn4Fu5jeAhzLMpW-lBY =600x353)

### Empty data for AOV and revenue widgets (LE-93425)

On LiveEngage -> Campaigns tab -> Dashboard, the “Average Order Value” and “Revenue After Chats” widgets displayed with empty data.

This bug is a result of the previous LiveEngage version and is now fixed, and the widgets now display both the AOV and revenue after chat real data.

  
  
![](https://lh6.googleusercontent.com/WJZQoBpBAgS7bUxAh49FiCCZ3Ne9gQ3bqt6N0ourxvA_LcBoWKXfar_x5i07kuIv94IybL9d41Cp3b3omw4os15tlmfFJWfABEZaSkfli9uxMNr7AsoqFYLCsTZQPGWmK5luve3k =589x362)

### 

### lpTag overrides lpTag.identities property (LE-92870)

With the introduction of the new Identity function, brands can determine the identity of logged-in (authenticated) users on each page, ensuring a smooth transition between authenticated and unauthenticated pages. With this fix, the identity can be added to the page before the lpTag.

The updated lpTag is available for all customers to implement on their webpages. lpTags, which were already implemented before, will not be updated automatically. In order to benefit from the change customers are requested to reimplement the new lpTag on their pages.

### M[essages sent from agent to consumer are marked as “read” ](https://globaljira.lpdomain.com/browse/LE-88929?src=confmacro)when agent manager joins the conversation (LE-88929)

On “All connections” > summary view:

M[essages sent from agents are marked as “read](https://globaljira.lpdomain.com/browse/LE-88929?src=confmacro)” (with two orange check marks) if they were read by the agent manager who joined the conversation. The status should be changed only when the consumer reads the messages. This bug is now resolved.

### [Conversation engagement attributes shown in chat sometimes if both handled by the same agent](https://globaljira.lpdomain.com/browse/LE-91274) (LE-91274)

On Visit info > consumer info , Visit info > personal info:

When an agent takes both chats and messaging conversations at the same time, personal data information from different conversations may leak to the chat. Once the browser is reloaded, irrelevant information is removed.

The conversation data:

![](https://lh3.googleusercontent.com/4V2eFeq358BIuaVI6olOEpXILPvtwq_kDewUp4r-VNzp-jdELbqz6ZI91a8FIgMAQQesxUou92yJ4uVDwS9D6jiL49tPrdimdQ2QOuyu-ShUTGET19vrJZLcTOFjde9wyCyUqx9l =624x548)

The chat data with the leaked conversation data:

![](https://lh5.googleusercontent.com/49yxfzeImtK2hEXKyC_-MxInRTMTHkW2RicOfQ7UT4RUZJmoc-vJhl36ZMCvFfOGQYya0LpyWG3TY6-GQ6YrEnBsAbqYHgtkSdT7e2PYz1D7skhnZLCPJ4uMj7cvDb6BsEJmSwxA =624x541)

### Wrong wait time behavior for transferred chats (AE-197)

On Visit info > Visitor info > wait time:

When transferring a chat, the wait time should display the duration between the time of the transfer till the agent’s assignment. Instead, it displays the overall chat time. This issue has been resolved.

After the fix, the wait time is reset (in this case auto accept is on, so the wait time is 0 minutes after the transfer. Before the bug the value would have been the total chat time):

![](https://lh5.googleusercontent.com/mQ2FESre1tSi7jLypKSX3-FRfynP46y90zD1m6iOcVOKBK3yVyZS9wg29uar5X0XFBI_7QYQd3Kk9Y42WM7VvnwCxV_ObdspZqqMvFAuNscUJtytf4nQPHYHD1Jn8svtSWF4L7rW =624x552)