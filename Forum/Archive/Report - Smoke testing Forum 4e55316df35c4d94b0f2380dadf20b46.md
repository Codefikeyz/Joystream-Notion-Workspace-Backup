# Report - Smoke testing: Forum

[https://github.com/Joystream/pioneer/issues/3304](https://github.com/Joystream/pioneer/issues/3304)

### **High level scenarios**

As forum WGL:

1. **Create category**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0xd01d35f3da7cb0653f172a12c0fd8fdcfc0674ea4ac6f20a659037651f7a5b7e](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0xd01d35f3da7cb0653f172a12c0fd8fdcfc0674ea4ac6f20a659037651f7a5b7e)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x5cd630cf376ed72ade1ef3bd14cd8051977d21c896ce9e280093edb98e7d7b4b](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x5cd630cf376ed72ade1ef3bd14cd8051977d21c896ce9e280093edb98e7d7b4b)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x844c4c8434d931f4d8e937af5c36db576403b43366730141a5a1b7a16995e096](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x844c4c8434d931f4d8e937af5c36db576403b43366730141a5a1b7a16995e096)

1. **Create subcategory**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x8ad12570b0a92a8a6146d85093b71604d1979bf37280bf321734fbf444b2fe30](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x8ad12570b0a92a8a6146d85093b71604d1979bf37280bf321734fbf444b2fe30)

1. **Delete subcategory**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x7e9c004ee259f747208e3c53e5c077b838be652a6411f207ed0bf37f30aba001](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x7e9c004ee259f747208e3c53e5c077b838be652a6411f207ed0bf37f30aba001) 

When I delete subcategory, it still exists. When I try delete it one more time, system says it doesn’t exist.

**Here is OK** 

![Screenshot 2022-08-04 at 00.11.45.png](Report%20-%20Smoke%20testing%20Forum/Screenshot_2022-08-04_at_00.11.45.png)

**BUT** it is appear when I click on **test** category

![Screenshot 2022-08-04 at 00.07.44.png](Report%20-%20Smoke%20testing%20Forum/Screenshot_2022-08-04_at_00.07.44.png)

![Screenshot 2022-08-04 at 00.05.28.png](Report%20-%20Smoke%20testing%20Forum/Screenshot_2022-08-04_at_00.05.28.png)

1. **Delete Category**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x3f37acf44db4a61f0ce4510b70862ae246cbb98d52af753c8a3582600ee670fd](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x3f37acf44db4a61f0ce4510b70862ae246cbb98d52af753c8a3582600ee670fd)

1. **Moderate the post (as WGL for Forum)**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x4fe6b2431af7a991ca8cfad875711f22522d7e03940529f8cb26c9a156a96786](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x4fe6b2431af7a991ca8cfad875711f22522d7e03940529f8cb26c9a156a96786)

Regular member:

1. **Create thread (extrinsics)**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x1ed85dc1a6cb9b9afcbb4973196f28982caa7e2fed196161bccbce944801051a](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x1ed85dc1a6cb9b9afcbb4973196f28982caa7e2fed196161bccbce944801051a)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x948db9a848fe8f8d10613fb31c1fb7f6349b3441f51328363be2cf8b5b896572](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x948db9a848fe8f8d10613fb31c1fb7f6349b3441f51328363be2cf8b5b896572)

1. **Create thread (forum)**

When I click Add new thread. Sign and send button doesn’t work.

![Screenshot 2022-08-03 at 23.07.36.png](Report%20-%20Smoke%20testing%20Forum/Screenshot_2022-08-03_at_23.07.36.png)

![Screenshot 2022-08-03 at 23.12.23.png](Report%20-%20Smoke%20testing%20Forum/Screenshot_2022-08-03_at_23.12.23.png)

1. **Post to thread**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0xbc59def2a680d1bf87adca660e789eba0524051801d1f8ecfcf24eb1867c2e30](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0xbc59def2a680d1bf87adca660e789eba0524051801d1f8ecfcf24eb1867c2e30)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x9c891bcfd4d97ea5416ed319d3175e87766bc9458b285802210eaa8f9e65e906](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x9c891bcfd4d97ea5416ed319d3175e87766bc9458b285802210eaa8f9e65e906)

1. **Edit post**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x0e18d34a155008f7bcbd978133159d2111c833a32c74f6faf82b17db82f90644](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x0e18d34a155008f7bcbd978133159d2111c833a32c74f6faf82b17db82f90644)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x11189b91d6a4a33645411ac49f745414511fa4dbe5da189a8ca64884f1e54309](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x11189b91d6a4a33645411ac49f745414511fa4dbe5da189a8ca64884f1e54309)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x2d42c4b9e35630029e173d8d2547f6bd38752a93aaa0c773c5133e48f379252b](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x2d42c4b9e35630029e173d8d2547f6bd38752a93aaa0c773c5133e48f379252b)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0xd8167cffe1aca03ffabc131ecf018e65f58c063dc51c95198702bf81551c7ce5](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0xd8167cffe1aca03ffabc131ecf018e65f58c063dc51c95198702bf81551c7ce5)

1. **Reply**

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x7ef3d44cc54585202782be10d89c1b0358b95bbbfe87f4a9ae47bae517b628e3](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x7ef3d44cc54585202782be10d89c1b0358b95bbbfe87f4a9ae47bae517b628e3)

[https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x6df79e636ed9796f61871992acb63d693267af90df10f80897ed6d6f8913fd84](https://polkadot.js.org/apps/?rpc=wss://54.172.154.45.nip.io/ws-rpc#/explorer/query/0x6df79e636ed9796f61871992acb63d693267af90df10f80897ed6d6f8913fd84)