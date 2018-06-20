---
title: 性別
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800154"
---
# <a name="gender"></a>性別

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

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



[PidTagGender の標準的なプロパティ](pidtaggender-canonical-property.md)

