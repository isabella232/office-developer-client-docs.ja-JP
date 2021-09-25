---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: abbbc3e67cb82bec98e136093dc324d761bce956
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613920"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)がカプセル化している基になる IMessage : [IMAPIProp](imessageimapiprop.md)を取得します。 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>パラメーター

 _ppmsg_
  
> [out]セキュリティで保護されたメッセージ オブジェクト。
    
## <a name="return-value"></a>戻り値

S_OK
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

