---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c6a68c4f1d2861dee4d111ee2a193ba0c7aa8cd6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549918"
---
# <a name="smapiforminfoarray"></a>SMAPIFormInfoArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム情報オブジェクトへのポインターの配列を格納します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|関連するマクロ:  <br/> |[CbMAPIFormInfoArray](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a>メンバー

 **cForms**
  
> **aFormInfo** メンバーが指す配列内のポインターの数。 
    
 **aFormInfo**
  
> フォーム情報オブジェクトへのポインターの配列へのポインター。
    
## <a name="remarks"></a>注釈

**SMAPIFormInfoArray** 構造体は、次のメソッドでパラメーターとして渡されます。 
  
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormMgr::SelectMultipleForms](imapiformmgr-selectmultipleforms.md)
    
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

