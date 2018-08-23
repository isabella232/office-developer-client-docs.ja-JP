---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: プロフィールの画像に、名、姓、名、URL など、個人の詳細情報を表す文字列を取得します。
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804339"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

プロフィールの画像に、名、姓、名、URL など、個人の詳細情報を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>パラメーター

_詳細情報_
  
> [out]個人の詳細情報を表す XML 文字列値。
    
## <a name="remarks"></a>注釈

返される_詳細情報_の XML 文字列は、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能拡張のスキーマで定義されている**人**の場合は、スキーマ定義に従う必要があります。
  
OSC は、ソーシャル ネットワーク上の**GetDetails** OSC プロバイダーをサポートしていますがキャッシュされている場合、またはハイブリッドの同期の友人を呼び出します。 OSC は、最初にログオンしたユーザーの友人の活動を取得、それは[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)と友人の情報をソーシャル ネットワークにログオンしたユーザーの既定の Outlook ストアに特定の連絡先フォルダーに格納. その後、OSC を呼び出しません**GetFriendsAndColleagues**または**GetDetails**キャッシュの更新間隔の有効期限が切れていない限り。 OSC が連絡先フォルダー内の友人の情報をキャッシュする方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

