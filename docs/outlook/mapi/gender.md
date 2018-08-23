---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588455"
---
# <a name="gender"></a>Gender

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージング ユーザーの性別の値を指定します。
  
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

## <a name="members"></a>Members

 _genderMin_
  
> 性別のサポートされている別の値の最小数です。
    
 _genderUnspecified_
  
> メッセージング ユーザーの性別は指定されていません。
    
 _genderFemale_
  
> メッセージングのユーザーは、(メス) です。
    
 _genderMale_
  
> メッセージングのユーザーは、(オス) です。
    
 _genderCount_
  
> 性別のサポートされている別の値の数。
    
 _genderMax_
  
> 性別のサポートされている別の値の最大数です。
    
## <a name="see-also"></a>関連項目



[PidTagGender 標準プロパティ](pidtaggender-canonical-property.md)

