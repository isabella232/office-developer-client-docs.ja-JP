---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419640"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ セット内の指定されたプロパティを検索します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー。  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> [in]  _lpPropArray_ パラメーターで示されるプロパティ セット内で検索するプロパティのタグ。 
    
 _cValues_
  
> [in]  _lpPropArray_ パラメーターで示されるプロパティ セット内のプロパティの数。 
    
 _lpPropArray_
  
> [in]検索する **プロパティを定義する SPropValue** 構造体の配列。 
    
## <a name="return-value"></a>戻り値

**LpValFindProp** 関数は、入力プロパティ タグに一致するプロパティを定義する **SPropValue** 構造体を返します。一致しない場合は NULL を返します。 
  
## <a name="remarks"></a>注釈

**LpValFindProp** 関数は **PpropFindProp と同じです**。
  
## <a name="see-also"></a>関連項目



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

