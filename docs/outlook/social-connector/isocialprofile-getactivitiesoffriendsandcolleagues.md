---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406893"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>注釈

ソーシャル コネクタ 2013 Outlookから、OSC は、アクティビティのオンデマンド同期のみをサポートし、アクティビティのキャッシュまたはハイブリッド同期はサポートされません。 OSC は、機能 XML の **cacheActivities** 設定を無視し、このメソッドを呼び出しなくなりました。 動的アクティビティの参照をサポートするには [、ISocialSession2::GetActivitiesEx メソッドを実装](isocialsession2-getactivitiesex.md) します。 **getActivities および** **dynamicActivitiesLookupEx** を true に設定すると、代わりに OSC に **ISocialSession2::GetActivitiesEx** を呼び出すメッセージが表示されます。  
  
OSC がフレンドのアクティビティを取得する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。 
  
## <a name="see-also"></a>関連項目

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

