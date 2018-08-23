---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: OSC 1.1 に、このメソッドは廃止されました。
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804361"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

OSC 1.1 に、このメソッドは廃止されました。
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>注釈

OSC 1.1 以降では、OSC は不要になった、 **GetActivities**を呼び出します。 OSC では、 **dynamicActivitiesLookup**の値を無視します。 参照の動的な活動をサポートするには、 [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 **False**、 **getActivities**と**true を指定**する代わりに**ISocialSession2::GetActivitiesEx**を呼び出す OSC を求めるメッセージが表示、 **dynamicActivitiesLookupEx** 、 **cacheActivities**を設定します。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

