---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b03d7a18b1013dffde8f9f3d729d655915b01c02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579734"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいテーブル行を挿入し、既存の行を置き換える可能性があります。
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>パラメーター

 _lpSRow_
  
> [in]追加する行または既存の行を置き換える [SRow](srow.md) 構造体へのポインター。 **SRow** 構造体の **lpProps** メンバーが指すプロパティ値構造体の 1 つは [、CreateTable](createtable.md)関数の呼び出しで _ulPropTagIndexColumn_ パラメーターで指定されたのと同じ値のインデックス列を含む必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に挿入または変更されました。
    
MAPI_E_INVALID_PARAMETER 
  
> 渡された行にはインデックス列が含めではありません。
    
## <a name="remarks"></a>注釈

**ITableData::HrModifyRow** メソッドは _、lpSRow_ パラメーターが指す **SRow** 構造で記述された行を挿入します。 インデックス列の値が  _lpSRow_ が示す行と同じ値を持つ行がテーブルに既に存在する場合、既存の行が置き換えられる。 **SRow** 構造に含まれる行と一致する行が存在しない場合 **、HrModifyRow** は行をテーブルの末尾に追加します。 
  
テーブルのすべてのビューが変更され  _、lpSRow_ が指す行が含まれます。 ただし、ビューに行を除外する制限がある場合は、ユーザーに表示されない場合があります。 
  
_lpSRow_ が指す行の列は、テーブル内の列と同じ順序である必要があります。 呼び出し元は、現在テーブルに含めされていない列プロパティとして含めすることもできます。 既存のビューの **場合、HrModifyRow** は新しい列を使用できますが、現在の列セットには含められません。 今後のビューでは **、HrModifyRow には** 列セットに新しい列が含まれます。 
  
**HrModifyRow** が行を追加すると、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。 
  
## <a name="see-also"></a>関連項目



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

