---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409910"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーに CPU を制御し、必要と見なされるタスクを実行できます。
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> トランスポート プロバイダーが CPU を正常にリリースしました。
    
MAPI_W_CANCEL_MESSAGE 
  
> まだ受信していない受信者へのメッセージの配信を停止するようにトランスポート プロバイダーに指示します。
    
## <a name="remarks"></a>注釈

**IMAPISupport::SpoolerYield** メソッドは、トランスポート プロバイダーのサポート オブジェクトに実装されます。 トランスポート プロバイダーは **、MAPI スプーラーが** 必要な処理を実行するためにスプーラーYield を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

一 **時停止できる長い** 操作を実行する場合は、SpoolerYield を呼び出します。 これにより、ビジー 状態のネットワーク上の大規模な受信者リストへの配信など、長時間の操作中にフォアグラウンド アプリケーションを実行できます。 
  
**SpoolerYield** がメッセージをMAPI_W_CANCEL_MESSAGE場合、MAPI スプーラーはメッセージを送信しなくなると判断しました。 可能MAPI_E_USER_CANCEL呼び出し元のプロセスに戻り、終了します。 
  
MAPI スプーラーに対する処理の詳細については、「MAPI スプーラーとの対話 [」を参照してください](interacting-with-the-mapi-spooler.md)。
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

