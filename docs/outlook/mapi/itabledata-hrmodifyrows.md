---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 693569c5b7ce6915bc30857445dca5b7e55c63c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613766"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数のテーブル行を挿入し、既存の行を置き換える可能性があります。
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpSRowSet_
  
> [in]追加する行のセットを含む [SRowSet](srowset.md) 構造体へのポインターで、必要に応じて既存の行を置き換える。 行セット内の [各 SRow](srow.md)構造体の **lpProps** メンバーが指すプロパティ値構造の 1 つには [、CreateTable](createtable.md)関数の呼び出しで _ulPropTagIndexColumn_ パラメーターで指定されたのと同じインデックス列が含まれている必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に挿入または変更されました。
    
MAPI_E_INVALID_PARAMETER 
  
> 1 つ以上の渡された行にインデックス列が含まれます。 このエラーが返された場合、行は変更されません。
    
## <a name="remarks"></a>注釈

**ITableData::HrModifyRows** メソッドは _、lpSRowSet_ パラメーターが指す [SRowSet](srowset.md)構造体で記述された行を挿入します。 行セット内の行のインデックス列の値がテーブル内の既存の行の値と一致する場合は、既存の行が置き換えられる。 **SRowSet** 構造体に含まれる行と一致する行が存在しない場合 **、HrModifyRows** は行をテーブルの末尾に追加します。 
  
テーブルのすべてのビューは  _、lpSRowSet_ が指す行を含む変更を行います。 ただし、ビューに行を除外する制限がある場合は、ユーザーに表示されない場合があります。 
  
_lpSRowSet_ が指す行の列は、テーブル内の列と同じ順序である必要があります。 呼び出し元は、現在テーブルに含めされていない列プロパティとして含めすることもできます。 既存のビューの **場合、HrModifyRows** は、これらの新しい列を使用できますが、現在の列セットには含められません。 今後のビューでは **、HrModifyRows には** 列セットに新しい列が含まれます。 
  
**HrModifyRows** が行を追加すると、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。 MAPI は、TABLE_ROW_ADDED行TABLE_ROW_MODIFIED、最大 8 行の通知を送信します。 8 行以上が **HrModifyRows** 呼び出しの影響を受ける場合、MAPI は代わりに 1 つのTABLE_CHANGED送信します。 
  
## <a name="see-also"></a>関連項目



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

