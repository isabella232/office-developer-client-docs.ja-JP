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
ms.openlocfilehash: 37d0ce65e125b2420af775d61ead51db189758ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801216"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**適用されます**: Outlook 
  
テーブルの行を削除します。
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValue_
  
> [in]削除する行のインデックス列を説明するプロパティ値の構造体へのポインター。 プロパティ値の構造体の**ulPropTag**メンバーは、 [CreateTable](createtable.md)関数への呼び出しの_ulPropTagIndexColumn_パラメーターと同じプロパティ タグを含める必要があります。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行が正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> _LpSPropValue_パラメーターで指定されたプロパティは、テーブル内の行を識別しません。 
    
## <a name="remarks"></a>備考

**ITableData::HrDeleteRow**メソッドは、 _lpSPropValue_パラメーターで指定されたプロパティに一致する列を含むテーブルの行を削除します。 行のデータが削除され、行は、開いているすべてのビューから削除されます。 
  
行が削除されると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。 
  
行の削除は減りません列セットが既存のビューを使用するか、ビューを開いた後で削除された行が特定の列の値を持つ最後の行の場合でも。
  
## <a name="see-also"></a>関連項目



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData: IUnknown](itabledataiunknown.md)
