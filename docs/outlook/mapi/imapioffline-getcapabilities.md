---
title: imapiofflinegetcapabilities
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
  
オフラインオブジェクトでサポートされているコールバックの条件を取得します。
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>パラメーター

 _アウト (アウト)_
  
> 読み上げ次の機能フラグのビットマスク。
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> オフラインオブジェクトがオフライン通知を提供できる。
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> オフラインオブジェクトは、オンライン通知を提供できます。
    
## <a name="remarks"></a>注釈

**[hropenofflineobj](hropenofflineobj.md)** を使用してオフラインオブジェクトを開くときに、クライアントは[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)上でクエリを実行して**imapioffline**インターフェイスへのポインターを取得し、 **imapioffline:: getcapabilities**を呼び出して、サポートされているコールバックを検索できます。オブジェクトによって。 クライアントは、 **IMAPIOfflineMgr**を使用してコールバックをセットアップすることを選択できます。
  
オフラインオブジェクトのメールサーバーによっては、オンラインに移行するためのコールバックをサポートするオブジェクトが、必ずしもオフラインへのコールバックをサポートするわけではないことに注意してください。
  
また、オフラインオブジェクトはオンライン/オフライン以外の変更に対するコールバックをサポートしていますが、オフライン状態 API はオンライン/オフライン変更のみをサポートしており、クライアントはそのような機能だけをチェックする必要があることにも注意してください。
  
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

