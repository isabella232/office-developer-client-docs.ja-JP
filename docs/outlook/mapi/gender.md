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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428649"
---
# <a name="gender"></a>Gender

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング ユーザーの性別に使用できる値を指定します。
  
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

 _genderMin_
  
> 性別でサポートされる異なる値の最小数。
    
 _genderUnspecified_
  
> メッセージング ユーザーの性別は指定されていません。
    
 _genderFemale_
  
> メッセージング ユーザーは女性です。
    
 _genderMale_
  
> メッセージング ユーザーは男性です。
    
 _genderCount_
  
> 性別でサポートされるさまざまな値の数。
    
 _genderMax_
  
> 性別でサポートされるさまざまな値の最大数。
    
## <a name="see-also"></a>関連項目



[PidTagGender 標準プロパティ](pidtaggender-canonical-property.md)

