---
title: itabledatahrmodifyrows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405360"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数のテーブル行を挿入します。既存の行を置換する場合もあります。
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpsrowset_
  
> 順番追加する行のセットを含む[srowset](srowset.md)構造体へのポインター。必要に応じて既存の行を置き換えます。 行セットの各[srow](srow.md)構造の**lpprops**メンバーによって参照されているプロパティ値構造の1つに、インデックス列が含まれている必要があります。これには、 __ [ulPropTagIndexColumn パラメーターで指定したものと同じ値があります。CreateTable](createtable.md)関数。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に挿入または変更されました。
    
MAPI_E_INVALID_PARAMETER 
  
> 渡された1つ以上の行にインデックス列がありません。 このエラーが返された場合、行は変更されません。
    
## <a name="remarks"></a>注釈

**itabledata:: hrmodifyrows**メソッドは、 _lpsrowset_パラメーターで指定された[srowset](srowset.md)構造によって示される行を挿入します。 行セットの行のインデックス列の値が、テーブル内の既存の行の値と一致する場合は、既存の行が置き換えられます。 **srowset**構造に含まれるものに一致する行が存在しない場合、 **hrmodifyrows**はテーブルの末尾に行を追加します。 
  
テーブルのすべてのビューは、 _lpsrowset_で示される行を含むように変更されます。 ただし、ビューに行を除外する制限がある場合は、ユーザーに表示されないことがあります。 
  
_lpsrowset_で示される行の列は、テーブル内の列と同じ順序である必要はありません。 また、呼び出し元には、現在テーブルにない列のプロパティを含めることもできます。 既存のビューの場合、 **hrmodifyrows**によって、これらの新しい列が使用可能になりますが、現在の列のセットには含まれません。 今後のビューの場合、 **hrmodifyrows**には列セットの新しい列が含まれます。 
  
**hrmodifyrows**が行を追加すると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知のために登録するためにテーブルの[IMAPITable:: アドバイズ](imapitable-advise.md)メソッドを呼び出します。 MAPI は、各行に対して TABLE_ROW_ADDED または TABLE_ROW_MODIFIED の通知を送信します。最大8行。 **hrmodifyrows**呼び出しの処理に8行を超える行が含まれている場合、MAPI は代わりに1つの TABLE_CHANGED 通知を送信します。 
  
## <a name="see-also"></a>関連項目



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

