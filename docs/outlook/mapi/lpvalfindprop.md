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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357429"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティセット内の指定されたプロパティを検索します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー。  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> 順番タグを指定します。このプロパティは、 _lpproparray_パラメーターで示されます。 
    
 _cvalues_
  
> 順番_lpproparray_パラメーターで示される、プロパティセット内のプロパティの数。 
    
 _lpproparray_
  
> 順番検索するプロパティを定義する**spropvalue**構造の配列です。 
    
## <a name="return-value"></a>戻り値

**lpvalfindprop**関数は、入力プロパティタグに一致するプロパティを定義する**spropvalue**構造体を返します。一致しない場合は NULL になります。 
  
## <a name="remarks"></a>解説

**lpvalfindprop**関数は、 **ppropfindprop**と同じです。
  
## <a name="see-also"></a>関連項目



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

