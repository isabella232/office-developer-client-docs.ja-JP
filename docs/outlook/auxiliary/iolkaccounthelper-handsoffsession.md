---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: IOlkAccountHelper::GetMapiSession によって返された MAPI セッション オブジェクトを解放します。
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799458"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッション オブジェクトを解放します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccountHelper](iolkaccounthelper.md)を参照してください。
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |**IOlkAccountHelper**の実装では、 **IOlkAccountHelper::GetMapiSession**で返される、独自の MAPI セッションを作成する場合は、ここでは、セッションを解放してと S_OK を返す必要があります。  <br/> |
|E_NOTIMPL  <br/> |**IOlkAccountHelper**の実装では、独自の MAPI セッションを作成しなかった場合のみ E_NOTIMPL を返す必要があります。 この例では、これは、戻り値はサポートされているだけです。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

