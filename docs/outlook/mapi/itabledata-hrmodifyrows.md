---
title: ITableDataHrModifyRows
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 15d98183548d4b73c35368d690ef63d5c3dfd9af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801233"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**適用されます**: Outlook 
  
既存の行が上書きされる、複数のテーブル行を挿入します。
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpSRowSet_
  
> [in][SRowSet](srowset.md)構造体へのポインターを含む一連の行を追加するには、必要に応じて既存の行を置き換えることです。 値構造体のプロパティでは、 **lpProps**各[SRow](srow.md)構造体のメンバーの行に設定するポイントの 1 つのインデックス列で、[への呼び出し内の_ulPropTagIndexColumn_パラメーターで指定された値と同じ値を含める必要があります。CreateTable](createtable.md)関数です。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行が挿入または変更されました。
    
MAPI_E_INVALID_PARAMETER 
  
> 渡された行の 1 つ以上には、インデックス列がありません。 このエラーが返された場合、行は変更されません。
    
## <a name="remarks"></a>備考

**ITableData::HrModifyRows**メソッドは、 _lpSRowSet_パラメーターが指す[SRowSet](srowset.md)構造体によって記述された行を挿入します。 行セット内の行のインデックス列の値には、テーブル内の既存の行の値が一致すると、既存の行が置き換えられます。 行が存在しない場合**SRowSet**構造体に含まれる 1 つに一致する、 **HrModifyRows**は、テーブルの末尾に行を追加します。 
  
_LpSRowSet_で指定された行を含むテーブルのすべてのビューを変更します。 ただし場合は、ビューでは、行が除外されるように制限がある、ある可能性がありますいないユーザーに表示します。 
  
_LpSRowSet_で指定された行の列をテーブル内の列と同じ順序にする必要はありません。 呼び出し元は、現在のテーブルに存在しない列のプロパティとしても指定できます。 既存のビューの**HrModifyRows**これらの新しい列を使用できるようですが、現在の列セットには含まれません。 将来のビューでは、 **HrModifyRows**には、列セットの新しい列が含まれます。 
  
**HrModifyRows**が行を追加すると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。 MAPI では、8 行まで、行ごとに、TABLE_ROW_ADDED または TABLE_ROW_MODIFIED の通知を送信します。 8 つ以上の行が影響を受ける場合、 **HrModifyRows**呼び出しによって MAPI 通知を送信する 1 つ TABLE_CHANGED 代わりにします。 
  
## <a name="see-also"></a>関連項目



[SRowSet](srowset.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

