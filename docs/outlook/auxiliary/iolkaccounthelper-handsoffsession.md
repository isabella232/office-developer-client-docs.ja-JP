---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: IOlkAccountHelper::GetMapiSession によって返された MAPI セッション オブジェクトを解放します。
ms.openlocfilehash: 3909d65d516d2b2da8e215bf5504e0ab64faa374
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617119"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

[IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッション オブジェクトを解放します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccountHelper」を参照してください](iolkaccounthelper.md)。
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |**IOlkAccountHelper** の実装で **、IOlkAccountHelper::GetMapiSession** で返される独自の MAPI セッションを作成する場合は、ここでセッションを解放し、S_OK を返す必要があります。  <br/> |
|E_NOTIMPL  <br/> |**IOlkAccountHelper** の実装で独自の MAPI セッションが作成されていない場合は、その MAPI セッションのみをE_NOTIMPL。 この場合、サポートされている戻り値はこれが唯一です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

