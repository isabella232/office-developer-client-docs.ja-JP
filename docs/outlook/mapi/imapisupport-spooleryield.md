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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584955"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
必要と見なされるすべてのタスクを実行できるように、MAPI スプーラーを CPU の制御を提供します。
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> トランスポート プロバイダーでは、CPU が解放されました。
    
MAPI_W_CANCEL_MESSAGE 
  
> トランスポート プロバイダーをまだ受け取っていないことを受信者にメッセージの配信を停止するように指示します。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダーのサポート オブジェクトの**IMAPISupport::SpoolerYield**メソッドを実装します。 トランスポート プロバイダーは、必要な処理を実行するのには MAPI スプーラーを許可するのには**SpoolerYield**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

一時停止することができますが、時間のかかる操作を実行している場合は、 **SpoolerYield**を呼び出します。 これにより、フォア グラウンド アプリケーションがビジー状態のネットワークの間で大きな受信者リストへの配信など、長時間のオペレーション中に実行できます。 
  
**SpoolerYield**は、MAPI_W_CANCEL_MESSAGE で返された場合、メッセージを送信できなくする必要があります、MAPI スプーラーを無効と判断しました。 可能な場合は、呼び出し元のプロセスと終了時に MAPI_E_USER_CANCEL を返します。 
  
MAPI スプーラーを生成の詳細については、 [MAPI スプーラーと対話する](interacting-with-the-mapi-spooler.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

