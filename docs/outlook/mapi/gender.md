---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342582"
---
# <a name="gender"></a>Gender

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングユーザーの性別に対して使用可能な値を指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a>メンバー

 _gendermin_
  
> 性別に対してサポートされている、さまざまな値の最小数。
    
 _genderunspecified_
  
> メッセージユーザーに性別が指定されていません。
    
 _genderfemale_
  
> メッセージングユーザーが女性である。
    
 _gendermale_
  
> メッセージングユーザーが男性である。
    
 _gendercount_
  
> 性別に対してサポートされているさまざまな値の数。
    
 _gendermax_
  
> 性別に対してサポートされているさまざまな値の最大数。
    
## <a name="see-also"></a>関連項目



[PidTagGender 標準プロパティ](pidtaggender-canonical-property.md)

