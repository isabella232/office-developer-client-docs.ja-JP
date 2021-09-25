---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 229900a1d00b8764266c45795462deb470762eb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564205"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン オブジェクトでコールバックがサポートされる条件を取得します。
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>パラメーター

 _pulCapablities_
  
> [out]次の機能フラグのビットマスク。
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> オフライン オブジェクトは、オフライン通知を提供できます。
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> オフライン オブジェクトは、オンライン通知を提供できます。
    
## <a name="remarks"></a>注釈

**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフライン オブジェクトを開いた後、クライアントは [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)でクエリを実行して **IMAPIOffline** インターフェイスへのポインターを取得し **、IMAPIOffline::GetCapabilities** を呼び出して、オブジェクトでサポートされるコールバックを検索できます。 その後、クライアントは **IMAPIOfflineMgr** を使用してコールバックを設定できます。
  
オフライン オブジェクトのメール サーバーによっては、オンラインに行くコールバックをサポートするオブジェクトは、オフラインに行くコールバックを必ずしもサポートしていない点に注意してください。
  
また、オフライン オブジェクトはオンライン/オフライン以外の変更のコールバックをサポートする場合があります。オフライン状態 API はオンライン/オフラインの変更のみをサポートし、クライアントはそのような機能のみを確認する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

