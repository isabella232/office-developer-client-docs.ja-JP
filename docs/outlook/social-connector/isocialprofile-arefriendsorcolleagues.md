---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: 指定したユーザーを友人かどうかを判断します。
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804345"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

指定したユーザーを友人かどうかを判断します。
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>パラメーター

_ユーザー Id_
  
> [in]ソーシャル ネットワーク上のユーザーのセットに対応するユーザー ID の値の配列を指定する構造体です。
    
_結果_
  
> [out]_ユーザー Id_の配列で対応する人が友人であるかどうかを示すブール型の値の配列を指定する構造体へのポインター。 
    
## <a name="remarks"></a>注釈

人ごとに、_ユーザー Id_のパラメーターの入力配列で表されるは、このメソッドは、_結果_のパラメーターの出力配列の対応する要素を設定します。 **true**は、人、友人は、 **false の場合、人が友人ではないこと**を示します。 
  
## <a name="see-also"></a>関連項目

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

