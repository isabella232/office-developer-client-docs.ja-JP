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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407551"
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

 _lppSortCriteria_
  
> [out]現在の並べ替え順序を保持する [SSortOrderSet](ssortorderset.md) 構造体へのポインターを指すポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 現在の並べ替え順序が正常に返されました。
    
MAPI_E_BUSY 
  
> 並べ替え順序の取得操作が開始されるのを防ぐ別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
## <a name="remarks"></a>注釈

**IMAPITable::QuerySortOrder** メソッドは、テーブルの現在の並べ替え順序を取得します。 並べ替え順序については [、SSortOrderSet 構造体で説明](ssortorderset.md) します。 
  
- **SSortOrderSet 構造体** の **cSorts** メンバーは、次の場合に 0 に設定できます。 
    
- テーブルはソートされません。
    
- テーブルの並べ替え方法に関する情報はありません。
    
- **SSortOrderSet** 構造体は、並べ替え順序を記述するには適切ではありません。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

並べ替えキーに 0 列を含む **SSortOrderSet** 構造体を持つ [IMAPITable::SortTable](imapitable-sorttable.md)メソッドに対して呼び出しが行われた場合は、現在の並べ替え順序を削除し、ある場合は既定の順序を適用します。 **QuerySortOrder** への後続の呼び出しでは、並べ替えキーの列を 0 個以上返すかどうかを選択できます。 現在のビューよりも多くの列を返す場合があります。
  
並べ替えの詳細については、「並べ替え [と分類」を参照してください](sorting-and-categorization.md)。
  
## <a name="see-also"></a>関連項目



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

