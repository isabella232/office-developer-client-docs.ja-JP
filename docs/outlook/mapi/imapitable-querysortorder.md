---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328862"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの現在の並べ替え順序を取得します。
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>パラメーター

 _lppsortcriteria_
  
> 読み上げ現在の並べ替え順序を保持する[ssortorderset](ssortorderset.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 現在の並べ替え順序が正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中であるため、並べ替え順序の取得操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
## <a name="remarks"></a>解説

**IMAPITable:: querysortorder**メソッドは、テーブルの現在の並べ替え順序を取得します。 並べ替え順序は、 [ssortorderset](ssortorderset.md)構造で記述されます。 
  
- 次**** の場合、 **ssortorderset**構造の csortmember は0に設定できます。 
    
- 表は並べ替えられていません。
    
- 表の並べ替え方法に関する情報はありません。
    
- **ssortorderset**構造は、並べ替え順序の記述には適していません。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

[IMAPITable:: sorttable](imapitable-sorttable.md)メソッドに対して、列に0を含む**ssortorderset**構造が設定されている場合は、現在の並べ替え順序を削除し、既定の順序 (存在する場合) を適用します。 以降の**querysortorder**の呼び出しでは、並べ替えキーに0個以上の列を返すかどうかを選択できます。 現在のビューの数を超える列を返すことができます。
  
並べ替えの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

