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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563465"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルの行を削除します。
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValue_
  
> [in]削除する行のインデックス列を説明するプロパティ値の構造体へのポインター。 プロパティ値の構造体の**ulPropTag**メンバーは、 [CreateTable](createtable.md)関数への呼び出しの_ulPropTagIndexColumn_パラメーターと同じプロパティ タグを含める必要があります。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行が正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> _LpSPropValue_パラメーターで指定されたプロパティは、テーブル内の行を識別しません。 
    
## <a name="remarks"></a>注釈

**ITableData::HrDeleteRow**メソッドは、 _lpSPropValue_パラメーターで指定されたプロパティに一致する列を含むテーブルの行を削除します。 行のデータが削除され、行は、開いているすべてのビューから削除されます。 
  
行が削除されると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。 
  
行の削除は減りません列セットが既存のビューを使用するか、ビューを開いた後で削除された行が特定の列の値を持つ最後の行の場合でも。
  
## <a name="see-also"></a>関連項目



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

