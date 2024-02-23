
# Sendbird Chat SDK for Unreal

[![Platform](https://img.shields.io/badge/platform-unreal-black.svg)](https://github.com/sendbird/sendbird-chat-sdk-unreal)
[![Languages](https://img.shields.io/badge/language-c++-black.svg)](https://github.com/sendbird/sendbird-chat-sdk-unreal)

## Introduction

You can add Chat to your app, including support for logging in, open channels, group channels, and all the other rich features that Sendbird offers, by integrating our SDK and only a few lines of code. Chat involves both clients and servers.  The Sendbird SDK enables development on your client side. On the server-side, Sendbird provides a fully-managed chat backend that interfaces with your app via the SDK. This **README** outlines the Chat SDK's structure, supplementary features, and installation instructions.

### How it works 

When the Sendbird Chat SDK is built into your app, the following user experience is possible: a user logs in, sees a list of channels, selects or creates an [Open Channel](https://sendbird.com/docs/chat/v3/unreal/channels/creating-a-channel/create-an-open-channel) or a [Group Channel](https://sendbird.com/docs/chat/v3/unreal/channels/creating-a-channel/create-a-group-channel), and, through the use of the [Channel Event Handlers](https://sendbird.com/docs/chat/v3/unreal/event-handler/event-handler-overview), sends messages to the channel, while also receiving them from other users within the channel.

### More about Sendbird Chat SDK for Unreal

Find out more about the Sendbird Chat SDK for Unreal in the [Sendbird Unreal Documentation](https://sendbird.com/docs/chat/v3/unreal/overview). If you have any comments or questions regarding bugs and feature requests, visit the [Sendbird Community](https://community.sendbird.com).

<br />

## Before getting started

Please verify the following prerequisites before getting started with the Sendbird Chat SDK for Unreal.

### Supported Platforms

- `Android`, `iOS`, `Windows`, `Mac`


## Getting started

This section gives you the information you need to get started with Sendbird Chat SDK for Unreal. Follow the  steps below to build the Chat SDK into your client app.

### Try the sample app

The fastest way to test the Chat SDK is to build your chat app on top of our sample app. To create a project for the sample app, download this app from our github repository:

- https://github.com/sendbird/sendbird-chat-sample-unreal

### Step 1: Create a Sendbird application from your dashboard

A Sendbird application manages everything required in a chat service including users, messages, and channels. To create an application:

1. Go to the [Sendbird Dashboard](https://dashboard.sendbird.com/auth/signup) and enter your email and password, and create a new account. You can also sign up with a Google account.
2. When prompted by the setup wizard, enter your organization information so you can manage your Sendbird applications.
3. Lastly, when your dashboard home appears after completing setup, click **Create +** at the top-right corner.

Regardless of the platform, only one Sendbird application can be integrated per app; however, the application supports communication with users across all Sendbird's supported platforms without any additional setup.

**Note**: Chat data is limited to the scope of a single application. Users from different Sendbird applications are therefore unable to chat with each other. 

### Step 2: Copy the `Sendbird` folder into the `Plugins_UE_version`(ex Plugins_UE_5.2) folder in your unreal project.

### Step 3: Add `Sendbird` the plugin in your *.uproject file.
```
{
  ...,
  "Plugins": [
    {
      "Name": "Sendbird",
      "Enabled": true
    }
  ]
}
```

### Step 4: Add `OpenSSL`, `Sendbird` module names in `*.Build.cs` file.
```
PrivateDependencyModuleNames.AddRange(new string[] { "OpenSSL", "Sendbird" });
```

### Step 5: Add the Sendbird header file in your `cpp` file.
```
#include "Sendbird.h"
```

## Warnings
- SDK functions and objects must be used in `GameThread`.
- After invoking `SBDMain::Disconnect([]() {})`, SDK functions and objects must not be used.
- You can use `SBDMain::GetCurrentUser()` to check if the SDK is available after disconnecting.
- `SBDError` object must be used in the invoked function.
