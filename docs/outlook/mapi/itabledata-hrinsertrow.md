---
title: 挿入行
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435440"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の行を挿入します。 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>パラメーター

 _ウリロウ_
  
> [in]特定の行を表す連続行番号。 新しい行は、番号が示す行の後に配置されます。 _uliRow_ パラメーターには、0 から n までの行番号を含めることができます。 _uliRow_ で n を渡すと、行はテーブルの末尾に追加されます。 
    
 _lpSRow_
  
> [in]挿入する行を記述する [SRow](srow.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行は正常に挿入されました。
    
MAPI_E_INVALID_PARAMETER 
  
> 挿入する行と同じインデックス列の値を持つ行がテーブルに既に存在します。
    
## <a name="remarks"></a>解説

メソッドは **、** 特定の位置のテーブルに行を挿入します。 新しい行は  _、uliRow_ パラメーターで指定された位置にある行の後に挿入されます。 
  
_uliRow_ がテーブルの行数に設定されている場合、新しい行はテーブルの末尾に追加されます。 
  
テーブルのインデックス列として機能するプロパティは _、lpSRow_ パラメーターによって指される [SRow](srow.md)構造体の **lpProps** メンバーに含まれている必要があります。 このインデックス プロパティは、通常 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、今後のメンテナンス タスクの行を一意に識別するために使用されます。
  
**SRow** 構造体のプロパティ列は、テーブル内のプロパティ列と同じ順序である必要はありません。 
  
行が挿入されると、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して通知を登録するすべてのクライアントまたはサービス プロバイダーに通知が送信されます。 制限のため、挿入された行がビューに含まれていない場合は、通知は送信されません。 
  
## <a name="see-also"></a>関連項目



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

