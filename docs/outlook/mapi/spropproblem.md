---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573286"
---
# <a name="spropproblem"></a>SPropProblem

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロパティを含む操作に関連するエラーについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a>Members

 **ulIndex**
  
> プロパティ タグの配列のインデックス。
    
 **ulPropTag**
  
> エラーを持つプロパティのプロパティ タグです。
    
 **scode**
  
> エラー値がプロパティを使用して問題を説明します。 この値は、任意の MAPI [SCODE](scode.md)の値を指定できます。 
    
## <a name="remarks"></a>注釈

**SPropProblem**構造体の配列は次のメソッドから返されます。 
  
- [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
    
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
    
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IPropData::HrAddObjProps](ipropdata-hraddobjprops.md)
    
**SPropProblem**構造体には、変更または MAPI プロパティを削除しようとしています。 操作に起因する**SCODE**エラー値が含まれています。 
  
エラーのプロパティに関連する**SPropProblem**構造体のしくみに関する詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)
  
[SPropProblemArray](spropproblemarray.md)


[MAPI の構造](mapi-structures.md)

