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
  
MAPI スプーラーに CPU を制御します。これにより、必要なタスクを実行できるようになります。
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約語0である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> トランスポートプロバイダーが CPU を正常に解放しました。
    
MAPI_W_CANCEL_MESSAGE 
  
> トランスポートプロバイダーに対して、まだ受信していない受信者に対するメッセージの配信を停止するように指示します。
    
## <a name="remarks"></a>注釈

**imapisupport:: SpoolerYield**メソッドは、トランスポートプロバイダーのサポートオブジェクトに実装されています。 トランスポートプロバイダーは、 **SpoolerYield**を呼び出して、MAPI スプーラーで必要な処理を実行できるようにします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

一時停止できる長時間の操作を実行している場合は、 **SpoolerYield**を呼び出します。 これにより、混雑したネットワークを介して大きな受信者リストへの配信など、長時間の操作中にフォアグラウンドアプリケーションが実行できるようになります。 
  
**SpoolerYield**が MAPI_W_CANCEL_MESSAGE を返した場合、MAPI スプーラーはメッセージを送信する必要がないと判断しました。 MAPI_E_USER_CANCEL を呼び出しプロセスに返し、可能であれば終了します。 
  
mapi スプーラーへの追加の詳細については、「 [mapi スプーラーとの対話](interacting-with-the-mapi-spooler.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

