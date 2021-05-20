---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: 名、名、プロファイル画像の URL など、人物の詳細を表す文字列を取得します。
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427333"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

名、名、プロファイル画像の URL など、人物の詳細を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>パラメーター

_details_
  
> [out]ユーザーの詳細を表す XML 文字列値。
    
## <a name="remarks"></a>注釈

返 _される詳細_ XML 文字列は、Outlook Social Connector (OSC) プロバイダーの機能拡張のスキーマで定義されている、ユーザーのスキーマ定義に準拠している必要があります。
  
OSC プロバイダーがソーシャル ネットワーク上の友人のキャッシュまたはハイブリッド同期をサポートしている場合、OSC は **GetDetails** を呼び出します。 OSC は、ログオンしているユーザーのフレンドのアクティビティを最初に取得すると[、ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)を呼び出し、ログオンしているユーザーの既定の Outlook ストア内のソーシャル ネットワーク固有の連絡先フォルダーに友人の情報を格納します。 その後、キャッシュの更新間隔が経過していない限り **、OSC は GetFriendsAndColleagues** または **GetDetails** を呼び出します。 OSC が連絡先フォルダーに友人の情報をキャッシュする方法の詳細については、「友人とアクティビティの同期」 [を参照してください](synchronizing-friends-and-activities.md)。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

