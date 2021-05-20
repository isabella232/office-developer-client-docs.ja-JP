---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: このメソッドは、OSC 1.1 では推奨されていません。
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439297"
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

