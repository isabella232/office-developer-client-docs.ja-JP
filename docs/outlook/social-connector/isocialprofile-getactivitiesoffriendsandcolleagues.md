---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: このメソッドは、Outlook Social Connector 2013 では廃止されました。
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406893"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

このメソッドは、Outlook Social Connector 2013 では廃止されました。
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>注釈

Outlook Social Connector 2013 以降では、アクティビティのオンデマンド同期のみをサポートしており、アクティビティのキャッシュまたはハイブリッド同期はサポートされていません。 .osc は、機能**** XML の cacheactivities 設定を無視し、このメソッドを呼び出すことがなくなります。 動的アクティビティ検索をサポートするには、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 **getactivities**と**dynamicActivitiesLookupEx**を**true**に設定します。この場合、 **ISocialSession2:: GetActivitiesEx**を呼び出すよう、.osc に通知されます。 
  
.osc がフレンドのアクティビティを取得する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

