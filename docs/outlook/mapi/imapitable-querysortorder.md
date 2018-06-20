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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b5eb671be022a6c3aa22e66f68386691fe23b275
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800842"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**適用されます**: Outlook 
  
テーブルの現在の並べ替え順序を取得します。
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parameters

 _lppSortCriteria_
  
> [out]現在の並べ替え順序を保持する[SSortOrderSet](ssortorderset.md)の構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 現在の並べ替え順序が正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作は、並べ替え順の取得操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
## <a name="remarks"></a>備考

**IMAPITable::QuerySortOrder**メソッドは、テーブルの現在の並べ替え順序を取得します。 [SSortOrderSet](ssortorderset.md)構造体のソート順を説明しています。 
  
- 場合、 **cSorts** 、 **SSortOrderSet**構造体のメンバーを 0 に設定できます。 
    
- 表はソートされていません。
    
- テーブルの並べ替え方法に関する情報はありません。
    
- **SSortOrderSet**構造体は、並べ替えの順序を記述するための適切ではありません。 
    
## <a name="notes-to-implementers"></a>実装者へのメモ

呼び出しされた場合、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドに並べ替えキーの列を含む**SSortOrderSet**構造を持つ、現在の並べ替え順序を削除し、いずれかを使用する必要がある場合は、既定の順序を適用します。 **QuerySortOrder**に以降の呼び出しでは、並べ替えキーの 0 個以上の列を返すかどうかを選択できます。 現在のビューより多くの列を返すことができます。
  
並べ替えの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

