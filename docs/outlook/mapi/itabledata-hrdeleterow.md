---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278861"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の行を削除します。
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>パラメーター

 _lpspropvalue_
  
> 順番削除する行のインデックス列を記述するプロパティ値構造へのポインター。 プロパティ値構造の**ulPropTag**メンバーには、 [CreateTable](createtable.md)関数の呼び出しの_ulPropTagIndexColumn_パラメーターと同じプロパティタグが含まれている必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> _lpspropvalue_パラメーターによって示されるプロパティは、テーブル内の行を識別しません。 
    
## <a name="remarks"></a>解説

**itabledata:: HrDeleteRow**メソッドは、 _lpspropvalue_パラメーターによって示されるプロパティに一致する列を含むテーブル行を削除します。 行のデータが削除され、開いているすべてのビューからその行が削除されます。 
  
行が削除されると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知を登録するためにテーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出します。 
  
行を削除しても、削除された行が、特定の列の値を持つ最後の行であっても、既存のビューまたは後で開くことができる列セットは縮小されません。
  
## <a name="see-also"></a>関連項目



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

