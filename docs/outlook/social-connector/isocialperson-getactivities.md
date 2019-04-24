---
title: i社会 al個人 getアクティビティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: このメソッドは、Outlook Social Connector 2013 では廃止されました。
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286165"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

このメソッドは、Outlook Social Connector 2013 では廃止されました。
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>解説

Outlook Social Connector 2013 以降では、アクティビティのオンデマンド同期のみをサポートしており、アクティビティのキャッシュまたはハイブリッド同期はサポートされていません。 .osc は、機能 XML の**cacheactivities**設定を無視し、このメソッドを呼び出しません。 動的アクティビティ検索をサポートするには、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 **cacheactivities**を**false**、 **getactivities** 、 **dynamicActivitiesLookupEx**を**true**に設定し、 **ISocialSession2:: GetActivitiesEx**を呼び出すように、.osc に通知されます。 
  
.osc がフレンドのアクティビティを取得する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

