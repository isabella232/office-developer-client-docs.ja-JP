---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437743"
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

