---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801084"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**適用対象**: Outlook 
  
同期を開始しようとしていますが、ローカル メッセージ ストアに通知します。
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]同期中に、適切な動作を決定するフラグを設定します。 Outlook は、クライアントに提供する情報を決定するのにレプリケーションの状態マシンの各状態でこれらのフラグを使用します。 たとえば、クライアントでは、 **SYNC_ONLY_ASSOCIATED**が成功した場合 Outlook はのみを返す関連付けられている (非表示) の項目に関連する情報です。 
    
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI �萔](mapi-constants.md)

