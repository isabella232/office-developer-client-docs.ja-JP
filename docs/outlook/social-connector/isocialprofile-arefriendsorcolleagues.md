---
title: iこの alprofilearefriendsor仕事仲間
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: 指定したユーザーがフレンドであるかどうかを判断します。
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412563"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

指定したユーザーがフレンドであるかどうかを判断します。
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>パラメーター

_UserIds_
  
> 順番ソーシャルネットワーク上の一連のユーザーに対応するユーザー ID 値の配列を指定する構造体。
    
_出力_
  
> 読み上げブール値の配列を指定する構造体へのポインター。これは、 _userIds_配列内の対応する人物がフレンドであるかどうかを示します。 
    
## <a name="remarks"></a>注釈

_userIds_パラメーターの入力配列に表示される各ユーザーについて、このメソッドは、 _results_パラメーターの出力配列の対応する要素を設定します。 **true**は、ユーザーがフレンドであることを示し、 **false**は、その人物がフレンドではないことを示します。 
  
## <a name="see-also"></a>関連項目

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

