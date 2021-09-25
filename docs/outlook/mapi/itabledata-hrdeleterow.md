---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dc516d8792fe87e6b9caf282146ad8ef996715c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587847"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル行を削除します。
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValue_
  
> [in]削除する行のインデックス列を記述するプロパティ値構造へのポインター。 プロパティ **値構造体の ulPropTag** メンバーには、CreateTable 関数の呼び出しから  _ulPropTagIndexColumn_ パラメーターと同じプロパティ タグを [含む必要](createtable.md) があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> _lpSPropValue_ パラメーターが示すプロパティは、テーブル内の行を識別します。 
    
## <a name="remarks"></a>注釈

**ITableData::HrDeleteRow** メソッドは _、lpSPropValue_ パラメーターが指すプロパティに一致する列を含むテーブル行を削除します。 行のデータが削除され、開いているすべてのビューから行が削除されます。 
  
行が削除された後、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。 
  
行を削除しても、削除された行が特定の列の値を持つ最後の行である場合でも、既存のビューまたは後で開いたビューで使用できる列セットは減らされません。
  
## <a name="see-also"></a>関連項目



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

