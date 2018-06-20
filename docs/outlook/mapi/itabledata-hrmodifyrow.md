---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a1388545597cf0000f270bf693c93f9349fb6426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801239"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**適用されます**: Outlook 
  
既存の行が上書きされる、テーブルの新しい行を挿入します。
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameters

 _lpSRow_
  
> [in]行を追加する既存の行を置換するかを説明する[SRow](srow.md)構造体へのポインター。 CreateTable の[への呼び出し内の_ulPropTagIndexColumn_パラメーターで指定された値と同じ値であるインデックス列が含まれている必要があります、 **lpProps** 、 **SRow**構造体のメンバーで指定されたプロパティ値の構造体のいずれか](createtable.md)関数です。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行を挿入または変更に成功しました。
    
MAPI_E_INVALID_PARAMETER 
  
> 渡された行には、インデックス列がありません。
    
## <a name="remarks"></a>備考

**ITableData::HrModifyRow**メソッドは、 _lpSRow_パラメーターが指す**SRow**の構造体によって記述された行を挿入します。 テーブル内に既に存在する場合は、その_lpSRow_ポイントの行とそのインデックス列に対して同じ値を持つ行を既存の行が置き換えられます。 行が存在しない場合、 **SRow**構造体に含まれる 1 つに一致する、 **HrModifyRow**は、テーブルの末尾に行を追加します。 
  
テーブルのすべてのビューは、 _lpSRow_で指定された行を含むように変更されます。 ただし場合は、ビューでは、行が除外されるように制限がある、ある可能性がありますいないユーザーに表示します。 
  
_LpSRow_で指定された行の列をテーブル内の列と同じ順序にする必要はありません。 呼び出し元は、現在のテーブルに存在しない列のプロパティとしても指定できます。 既存のビューの**HrModifyRow**これらの新しい列を使用できるようですが、現在の列セットには含まれません。 将来のビューでは、 **HrModifyRow**には、列セットの新しい列が含まれます。 
  
**HrModifyRow**は、行を追加した後にすべてのクライアントまたはサービス プロバイダーのテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが通知が送信されます。 
  
## <a name="see-also"></a>関連項目



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

