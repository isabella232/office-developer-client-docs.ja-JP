---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf294c7243ddc3b418c1df9de3b6981c1b950fb8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596051"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームで、前回の保存以降に行われた変更を確認します。
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームには、最後に保存された後に行われた変更があります。
    
S_FALSE 
  
> フォームには、最後に保存された後に行われた変更は含めされません。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **、IPersistMessage::IsDirty** メソッドを呼び出して、メッセージに保存されていないデータが含されているかどうかを判断します。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

