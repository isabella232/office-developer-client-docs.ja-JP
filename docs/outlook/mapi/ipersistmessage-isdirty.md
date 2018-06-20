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
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801120"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**適用されます**: Outlook 
  
最後の保存以降に加えた変更のフォームをチェックします。
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parameters

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームには、最後に保存された後に行われた変更があります。
    
S_FALSE 
  
> フォームには、最後に保存された後に加えられた変更はありません。
    
## <a name="remarks"></a>備考

フォームの閲覧者は、メッセージのデータが保存されているかどうかを決定する**IPersistMessage::IsDirty**メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)

