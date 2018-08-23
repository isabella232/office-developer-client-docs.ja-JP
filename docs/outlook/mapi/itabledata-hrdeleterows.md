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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801212"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**適用対象**: Outlook 
  
複数のテーブル行を削除します。
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]削除を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
TAD_ALL_ROWS 
  
> テーブルと 1 つの TABLE_RELOAD 通知を送信する、対応するすべてのビューからすべての行を削除します。
    
 _lprowsetToDelete_
  
> [in]削除する行を表す行セットへのポインター。 _UlFlags_パラメーターに TAD_ALL_ROWS フラグが設定されている場合は、 _lprowsetToDelete_パラメーターを NULL にできます。 
    
 _cRowsDeleted_
  
> [out]削除された行の数。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> テーブルの行は削除されました。
    
## <a name="remarks"></a>注釈

**ITableData::HrDeleteRows**メソッドは、検索し、行の各**aRow**のエントリの**lpProps**のメンバーによって設定するのにはポイントのプロパティに一致する列を含むテーブルの行を削除します。 インデックス列を使用して各行を識別します。この列には、 [CreateTable](createtable.md)関数への呼び出し内の_ulPropTagIndexColumn_パラメーターで渡されたプロパティ タグと同じプロパティ タグが必要です。 
  
_CRowsDeleted_では、実際に削除された行の数が返されます。 1 つまたは複数の行が見つからなかった場合、エラーは返されません。 
  
行が削除されると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。 
  
行を削除するか、テーブルの既存のビューに使用できる列は縮小されません、削除された行が特定の列の値を持つ最後の場合でも以降の表形式ビューに開かれます。
  
## <a name="see-also"></a>関連項目



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

