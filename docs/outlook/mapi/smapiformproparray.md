---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 471e2accdd925e81c951e195349bf00691dea100
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624182"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[SMAPIFormProp 構造体の配列を格納](smapiformprop.md)します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|関連するマクロ:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a>メンバー

 **cProps**
  
> **aFormProp** メンバーの配列内の名前付きプロパティの数。 
    
 **ulPad**
  
>  正しい配置を保証するために使用される 8 バイトのパディング。 
    
 **aFormProp**
  
> フォーム プロパティの配列。
    
## <a name="remarks"></a>注釈

**SMAPIFormPropArray** 構造体は、パラメーターとして次のメソッドに渡されます。 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>関連項目



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[MAPI の構造](mapi-structures.md)

