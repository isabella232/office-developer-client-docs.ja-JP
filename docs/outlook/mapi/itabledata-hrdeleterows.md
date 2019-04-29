---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416455"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数の表の行を削除します。
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番削除を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TAD_ALL_ROWS 
  
> 1つの TABLE_RELOAD 通知を送信して、テーブルおよび対応するすべてのビューからすべての行を削除します。
    
 _lprowsetToDelete_
  
> 順番削除する行を説明する行セットへのポインター。 TAD_ALL_ROWS フラグが_ulflags_パラメーターで設定されている場合は、 _lprowsetToDelete_パラメーターを NULL にすることができます。 
    
 _cRowsDeleted_
  
> 読み上げ削除された行のカウント。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブルの行が正常に削除されました。
    
## <a name="remarks"></a>注釈

**itabledata:: HrDeleteRows**メソッドは、行セット内の各**arow**エントリの**lpprops**メンバーによって示されるプロパティに一致する列を含むテーブル行を検索して削除します。 インデックス列は、各行を識別するために使用されます。この列は、 [CreateTable](createtable.md)関数の呼び出しで_ulPropTagIndexColumn_パラメーターで渡されたプロパティタグと同じプロパティタグを持っている必要があります。 
  
実際に削除された行の数は、 _cRowsDeleted_で返されます。 1つまたは複数の行が見つからない場合、エラーは返されません。 
  
行が削除されると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知を登録するためにテーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出します。 
  
行を削除しても、削除された行が特定の列の値を持つ最後の行であっても、既存のテーブルビューまたは後で開くテーブルビューで使用可能な列は減少しません。
  
## <a name="see-also"></a>関連項目



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

