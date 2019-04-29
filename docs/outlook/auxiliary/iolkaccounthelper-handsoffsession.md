---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: 'IOlkAccountHelper:: GetMapiSession によって返された MAPI セッションオブジェクトを解放します。'
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418632"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

- [IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッションオブジェクトを解放します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccountHelper](iolkaccounthelper.md)を参照してください。
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |**IOlkAccountHelper**の実装で**IOlkAccountHelper:: GetMapiSession**で返される独自の MAPI セッションを作成する場合は、ここでセッションを解放し、S_OK を返す必要があります。  <br/> |
|E_NOTIMPL  <br/> |**IOlkAccountHelper**の実装で独自の MAPI セッションが作成されていない場合は、E_NOTIMPL のみを返す必要があります。 この場合、サポートされている唯一の戻り値です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

