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

 _uliRow_
  
> 順番特定の行を表す連続した行番号を指定します。 新しい行は、番号が示す行の後に配置されます。 _uliRow_パラメーターには、0 ~ n の行番号を含めることができます。ここで、n はテーブル内の行の合計数です。 _uliRow_で n を渡すと、行は表の末尾に追加されます。 
    
 _lpsrow_
  
> 順番挿入する行を記述する[srow](srow.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に挿入されました。
    
MAPI_E_INVALID_PARAMETER 
  
> 挿入された行がテーブルに既に存在する場合、そのインデックス列の値が同じ行。
    
## <a name="remarks"></a>注釈

**itabledata:: HrInsertRow**メソッドは、特定の位置にあるテーブルに行を挿入します。 _uliRow_パラメーターで指定された位置にある行の後に新しい行が挿入されます。 
  
_uliRow_が表の行数に設定されている場合、新しい行は表の末尾に追加されます。 
  
テーブルのインデックス列として機能するプロパティは、 _lpsrow_パラメーターで指定される[srow](srow.md)構造の**lpprops**メンバに含まれている必要があります。 通常、このインデックスプロパティ ( **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))) は、今後のメンテナンス作業のために行を一意に識別するために使用されます。
  
**srow**構造のプロパティ列は、テーブル内のプロパティ列と同じ順序である必要はありません。 
  
行が挿入されると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知を登録するためにテーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出します。 制限のために挿入された行がビューに含まれていない場合、通知は送信されません。 
  
## <a name="see-also"></a>関連項目



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

