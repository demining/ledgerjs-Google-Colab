<img src="https://user-images.githubusercontent.com/211411/34776833-6f1ef4da-f618-11e7-8b13-f0697901d6a8.png" height="100" />

[Github](https://github.com/LedgerHQ/ledgerjs/),
[Ledger Devs Slack](https://ledger-dev.slack.com/)

## @ledgerhq/hw-transport-node-hid-noevents

Allows to communicate with Ledger Hardware Wallets.

**\[Node]**/Electron **(HID)** – uses **only** `node-hid`. Does not provide USB events.

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

*   [TransportNodeHidNoEvents](#transportnodehidnoevents)
    *   [Parameters](#parameters)
    *   [Examples](#examples)
    *   [exchange](#exchange)
        *   [Parameters](#parameters-1)
    *   [close](#close)
    *   [isSupported](#issupported)
    *   [list](#list)
    *   [listen](#listen)
        *   [Parameters](#parameters-2)
    *   [open](#open)
        *   [Parameters](#parameters-3)

### TransportNodeHidNoEvents

**Extends Transport**

node-hid Transport minimal implementation

#### Parameters

*   `device` **HID.HID** 

#### Examples

```javascript
import TransportNodeHid from "@ledgerhq/hw-transport-node-hid-noevents";
...
TransportNodeHid.create().then(transport => ...)
```

#### exchange

Exchange with the device using APDU protocol.

##### Parameters

*   `apdu` **[Buffer](https://nodejs.org/api/buffer.html)** 

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[Buffer](https://nodejs.org/api/buffer.html)>** a promise of apdu response

#### close

release the USB device.

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<void>** 

#### isSupported

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)>** 

#### list

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<any>** 

#### listen

##### Parameters

*   `observer` **Observer\<DescriptorEvent\<any>>** 

Returns **Subscription** 

#### open

if path="" is not provided, the library will take the first device

##### Parameters

*   `path` **([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) | null | [undefined](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/undefined))** 
