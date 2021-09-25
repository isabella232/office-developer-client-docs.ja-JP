---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: 指定したユーザーがフレンドかどうかを指定します。
ms.openlocfilehash: 5f782e998f46485cc5560e13ffbe55394702dbc2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563218"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

指定したユーザーがフレンドかどうかを指定します。
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>パラメーター

_userIds_
  
> [in]ソーシャル ネットワーク上の一連のユーザーに対応するユーザー ID 値の配列を指定する構造体。
    
_結果_
  
> [out]userIds 配列の対応する人物がフレンドであるかどうかを示すブール型  _(Boolean)_ の値の配列を指定する構造体へのポインター。 
    
## <a name="remarks"></a>注釈

_userIds_ パラメーターの入力配列で表される各ユーザーについて、このメソッドは、results パラメーターの出力配列に対応する要素を _設定_ します。 **true** は、そのユーザーが友人であり **、false は** 、そのユーザーが友人ではないと示します。 
  
## <a name="see-also"></a>関連項目

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

