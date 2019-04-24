---
title: i社会 al個人 getdetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: 名、姓、プロファイル画像への URL など、個人の詳細を表す文字列を取得します。
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286144"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

名、姓、プロファイル画像への URL など、個人の詳細を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>パラメーター

_details_
  
> 読み上げ個人の詳細を表す XML 文字列型 (string) の値。
    
## <a name="remarks"></a>解説

返される_詳細_XML 文字列は、Outlook Social Connector (.osc) プロバイダー拡張機能のスキーマで定義されているように、 **person**のスキーマ定義に準拠している必要があります。
  
.osc プロバイダーがソーシャルネットワーク上で友人のキャッシュまたはハイブリッド同期をサポートしている場合、.osc は**getdetails**を呼び出します。 .osc が、ログオンしているユーザーのフレンドのアクティビティを最初に取得するときに、 [iGetFriendsAndColleagues alperson:::](isocialperson-getfriendsandcolleagues.md)を呼び出し、ソーシャルネットワーク固有の連絡先フォルダーに友人の情報を格納します。これには、ログオンユーザーの既定の Outlook ストアが含まれます。. その後、.osc は、キャッシュの更新間隔が経過していない限り、 **GetFriendsAndColleagues**または**getdetails**を呼び出しません。 .osc が連絡先フォルダー内のフレンド情報をキャッシュする方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

