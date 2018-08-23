---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578095"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロパティで指定したプロパティの検索を設定します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダーです。  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> [in]プロパティが、 _lpPropArray_パラメーターで指定されたプロパティ セット内で検索するタグです。 
    
 _あう_
  
> [in]_LpPropArray_パラメーターで指定されたプロパティ セットにプロパティの数。 
    
 _lpPropArray_
  
> [in]検索するプロパティを定義する**SPropValue**構造体の配列。 
    
## <a name="return-value"></a>戻り値

**LpValFindProp**関数は、一致がない場合、入力プロパティのタグ、または NULL に一致するプロパティを定義する**SPropValue**構造体を返します。 
  
## <a name="remarks"></a>注釈

**LpValFindProp**関数は、 **PpropFindProp**と同じです。
  
## <a name="see-also"></a>関連項目



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

