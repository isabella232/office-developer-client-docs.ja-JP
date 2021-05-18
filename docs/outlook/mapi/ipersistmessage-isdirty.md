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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407572"
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

