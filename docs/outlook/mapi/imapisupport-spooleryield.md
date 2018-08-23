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
ms.openlocfilehash: 6e917991e109ac04a14ea7d93eebcf9cce835845
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800794"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**適用対象**: Outlook 
  
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

