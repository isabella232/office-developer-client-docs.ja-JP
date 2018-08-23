---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579313"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[SMAPIFormProp](smapiformprop.md)構造体の配列が含まれています。 
  
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

## <a name="members"></a>Members

 **cProps**
  
> **AFormProp**メンバーの配列の名前付きプロパティの数。 
    
 **ulPad**
  
>  適切なアライメントを保証するために使用される埋め込みの 8 バイトです。 
    
 **aFormProp**
  
> フォームのプロパティの配列です。
    
## <a name="remarks"></a>注釈

**SMAPIFormPropArray**構造体は次の方法をパラメーターとして渡されます。 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>関連項目



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[MAPI の構造](mapi-structures.md)

