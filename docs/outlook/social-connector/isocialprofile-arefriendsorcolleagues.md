---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: 指定したユーザーがフレンドかどうかを指定します。
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412563"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

指定したユーザーがフレンドかどうかを指定します。
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>パラメーター

_UserIds_
  
> [in]ソーシャル ネットワーク上の一連のユーザーに対応するユーザー ID 値の配列を指定する構造体。
    
_結果_
  
> [out]userIds 配列の対応する人物がフレンドであるかどうかを示すブール型  _(Boolean)_ の値の配列を指定する構造体へのポインター。 
    
## <a name="remarks"></a>注釈

_userIds_ パラメーターの入力配列で表される各ユーザーについて、このメソッドは、results パラメーターの出力配列に対応する要素を _設定_ します。 **true** は、そのユーザーが友人であり **、false は** 、そのユーザーが友人ではないと示します。 
  
## <a name="see-also"></a>関連項目

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

