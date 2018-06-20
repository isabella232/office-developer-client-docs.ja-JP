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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 205c9dd28692592ddf133b1b30989ba9fd4236f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800612"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**適用されます**: Outlook 
  
コールバックは、オフラインのオブジェクトによってサポートされている条件を取得します。
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parameters

 _pulCapablities_
  
> [out]以下の機能フラグのビットマスク。
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> オフライン オブジェクトはオフラインの通知を提供することができます。
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> オフラインのオブジェクトでは、オンラインの通知を提供することができます。
    
## <a name="remarks"></a>備考

**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフラインのオブジェクトを開くときにクライアントは、 **IMAPIOffline**インターフェイスへのポインターを取得し、サポートされているコールバックを確認するのには、 **IMAPIOffline::GetCapabilities**を呼び出すには、 [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)に問い合わせることができます。オブジェクトです。 **IMAPIOfflineMgr**を使用してコールバックを設定するクライアントを選択できます。
  
オフライン オブジェクトのメール サーバー、オンラインのコールバックをサポートするオブジェクトは必ずしもサポート コールバック オフラインになるため注意してください。
  
なお、いる間以外のオンラインまたはオフラインの変更のオフライン オブジェクトがコールバックをサポート可能性があります、オフライン状態の API は、オンラインとオフラインの変更のみをサポートしているクライアントは、このような機能だけを確認する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)


[MAPI �萔](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

