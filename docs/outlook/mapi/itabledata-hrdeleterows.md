---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 48810ea68394fa21ad666dfc8464bbf12b2c8359
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584228"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数のテーブル行を削除します。
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]削除を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TAD_ALL_ROWS 
  
> テーブルと対応するビューからすべての行を削除し、1 つのビュー TABLE_RELOADします。
    
 _lprowsetToDelete_
  
> [in]削除する行を記述する行セットへのポインター。 _lprowsetToDelete_ パラメーターは _、ulFlags_ パラメーター TAD_ALL_ROWSフラグが設定されている場合は NULL にできます。 
    
 _cRowsDeleted_
  
> [out]削除された行の数。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブル行が正常に削除されました。
    
## <a name="remarks"></a>注釈

**ITableData::HrDeleteRows** メソッドは、行セット内の各 **aRow** エントリの **lpProps** メンバーが指すプロパティに一致する列を含むテーブル行を検索して削除します。 インデックス列は、各行を識別するために使用されます。この列には [、CreateTable](createtable.md)関数の呼び出しで _ulPropTagIndexColumn_ パラメーターに渡されるプロパティ タグと同じプロパティ タグが必要です。 
  
実際に削除された行の数は  _、cRowsDeleted で返されます_。 1 つ以上の行が見つからない場合、エラーは返されません。 
  
行が削除された後、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。 
  
行を削除しても、削除された行が特定の列の値を持つ最後の行である場合でも、既存のテーブル ビューまたは後で開いたテーブル ビューで使用できる列は減らされません。
  
## <a name="see-also"></a>関連項目



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

