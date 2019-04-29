---
title: i社会 alsessiongetアクティビティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: このメソッドは、.osc 1.1 では廃止されました。
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439297"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

このメソッドは、.osc 1.1 では廃止されました。
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>注釈

.osc 1.1 から、.osc は**getactivities**を呼び出すことがなくなりました。 .osc では、 **dynamicActivitiesLookup**の値は無視されます。 動的アクティビティ検索をサポートするには、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 **cacheactivities**を**false**に設定し、 **getactivities**と**dynamicActivitiesLookupEx**を**true**として設定します。これにより、 **ISocialSession2:: GetActivitiesEx**を呼び出すように、.osc に通知されます。 
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

