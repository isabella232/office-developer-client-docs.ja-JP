---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801211"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**適用対象**: Outlook 
  
テーブルの行を挿入します。 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>パラメーター

 _uliRow_
  
> [in]特定の行を表す連続した行の数です。 ローの数を示す新しい行に配置されます。 _UliRow_パラメーターは、0 から n 行番号が含まれていますが、n は、テーブル内の行の合計数です。 N を_uliRow_に渡すと、テーブルの末尾に行が追加されます。 
    
 _lpSRow_
  
> [in]挿入する行を説明する[SRow](srow.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行は正しく挿入されました。
    
MAPI_E_INVALID_PARAMETER 
  
> テーブルに既に挿入する行が存在するとそのインデックス列に対して同じ値を持つ行です。
    
## <a name="remarks"></a>注釈

**ITableData::HrInsertRow**メソッドでは、特定の位置にあるテーブルに行を挿入します。 _UliRow_パラメーターによって指定された位置にある行の後に、新しい行が挿入されます。 
  
_UliRow_は、テーブル内の行の数に設定されている場合は、テーブルの末尾に新しい行が追加されます。 
  
**LpProps** 、 [SRow](srow.md)構造体のメンバー、 _lpSRow_パラメーターが指すは、テーブルのインデックス列として機能するプロパティを含める必要があります。 このインデックスのプロパティ、 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) を通常は、将来の保守タスクの行を一意に識別されます。
  
**SRow**構造体のプロパティ列をテーブル内のプロパティの列と同じ順序にする必要はありません。 
  
行が挿入されると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。 制限があるため、ビューに挿入された行が含まれていない場合、通知は送信されません。 
  
## <a name="see-also"></a>関連項目



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

