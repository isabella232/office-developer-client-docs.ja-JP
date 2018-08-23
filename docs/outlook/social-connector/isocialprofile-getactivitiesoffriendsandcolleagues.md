---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Outlook ソーシャル コネクタ 2013 では、このメソッドは廃止されました。
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804378"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Outlook ソーシャル コネクタ 2013 では、このメソッドは廃止されました。
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>注釈

Outlook ソーシャル コネクタ 2013、OSC の活動のみ、オンデマンド同期をサポートしている、キャッシュされていない、または活動のハイブリッド同期を開始します。 OSC では、XML の機能の**cacheActivities**の設定を無視し、不要になったこのメソッドを呼び出します。 参照の動的な活動をサポートするには、 [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 **GetActivities**と**dynamicActivitiesLookupEx**を**true を指定**する代わりに**ISocialSession2::GetActivitiesEx**を呼び出す OSC を求めるメッセージが表示に設定します。 
  
OSC が友人の活動を取得する方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

