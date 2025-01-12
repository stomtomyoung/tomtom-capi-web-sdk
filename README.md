# capi-web-sdk-common

[English](README.md) | [简体中文](README.zh-CN.md)

## Overview

Based on [tencentcloud-sdk-nodejs](https://github.com/TencentCloud/tencentcloud-sdk-nodejs), this package encapsulates the TencentCloud API Web SDK Common version, providing the ability to directly request Tencent Cloud APIs in a Web Standard environment.

## Installation

```shell
npm i capi-web-sdk-common
```

## Usage

```js
import { CapiClient } from 'capi-web-sdk-common';

const capiEndpoint = 'xxx.tencentcloudapi.com';
const capiVersion = 'xxxx-xx-xx';

const capiConfig = {
  region: 'ap-xxxxx',
  credential: {
    secretId: 'xxxxx',
    secretKey: 'xxxxx',
  },
  profile: {
    signMethod: 'TC3-HMAC-SHA256',
    language: 'en-US',
    httpProfile: {
      reqMethod: 'POST',
      reqTimeout: 30,
    },
  },
};

const capiClient = new CapiClient(capiEndpoint, capiVersion, capiConfig);

const response = await capiClient.request('xxxxx', {});
```