---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。
ms.openlocfilehash: c225cd19c2e3d02ebddae70ccd98ad5d59f783ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563246"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>注釈

ソーシャル コネクタ 2013 Outlookから、OSC は、アクティビティのオンデマンド同期のみをサポートし、アクティビティのキャッシュまたはハイブリッド同期はサポートされません。 OSC では、機能 XML の **cacheActivities** 設定は無視され、このメソッドは呼び出されません。 動的アクティビティの参照をサポートするには [、ISocialSession2::GetActivitiesEx メソッドを実装](isocialsession2-getactivitiesex.md) します。 **cacheActivities を** false、getActivities、**および dynamicActivitiesLookupEx** を **true** に設定すると、代わりに OSC が **ISocialSession2::GetActivitiesEx** を呼び出すプロンプトが表示されます。   
  
OSC がフレンドのアクティビティを取得する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。 
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

