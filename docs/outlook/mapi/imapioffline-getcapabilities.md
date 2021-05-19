---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433375"
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

