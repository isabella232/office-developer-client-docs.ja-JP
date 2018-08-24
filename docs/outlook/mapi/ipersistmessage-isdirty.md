---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576205"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最後の保存以降に加えた変更のフォームをチェックします。
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームには、最後に保存された後に行われた変更があります。
    
S_FALSE 
  
> フォームには、最後に保存された後に加えられた変更はありません。
    
## <a name="remarks"></a>注釈

フォームの閲覧者は、メッセージのデータが保存されているかどうかを決定する**IPersistMessage::IsDirty**メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

