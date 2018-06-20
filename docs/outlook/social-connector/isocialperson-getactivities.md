---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Outlook ソーシャル コネクタ 2013 では、このメソッドは廃止されました。
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804340"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Outlook ソーシャル コネクタ 2013 では、このメソッドは廃止されました。
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>備考

Outlook ソーシャル コネクタ 2013、OSC の活動のみ、オンデマンド同期をサポートしている、キャッシュされていない、または活動のハイブリッド同期を開始します。 OSC では、XML の機能の**cacheActivities**の設定を無視し、このメソッドを呼び出しません。 参照の動的な活動をサポートするには、 [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 **False**、 **getActivities** **true を指定**する代わりに**ISocialSession2::GetActivitiesEx**を呼び出す OSC を求めるメッセージが表示は、 **dynamicActivitiesLookupEx**と**cacheActivities**を設定します。 
  
OSC が友人の活動を取得する方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)

