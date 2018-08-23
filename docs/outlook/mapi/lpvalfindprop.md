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
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801281"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**適用対象**: Outlook 
  
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

