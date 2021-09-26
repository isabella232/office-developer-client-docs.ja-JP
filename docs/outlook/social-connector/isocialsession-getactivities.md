---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: このメソッドは、OSC 1.1 では推奨されていません。
ms.openlocfilehash: 6cc6137091ec1c10cd2e92f904149597935b094a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608819"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

このメソッドは、OSC 1.1 では推奨されていません。
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>注釈

OSC 1.1 から、OSC は **GetActivities を呼び出しなくなりました**。 OSC は **、dynamicActivitiesLookup の値を無視します**。 動的アクティビティの参照をサポートするには [、ISocialSession2::GetActivitiesEx メソッドを実装](isocialsession2-getactivitiesex.md) します。 **cacheActivities を** **false** に設定し **、getActivities および dynamicActivitiesLookupEx** を true に設定すると、代わりに OSC に **ISocialSession2::GetActivitiesEx** を呼び出すプロンプトが表示されます。   
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

