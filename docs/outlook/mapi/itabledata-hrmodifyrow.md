---
title: itabledatahrmodifyrow
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409000"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既存の行を置き換える可能性がある新しいテーブル行を挿入します。
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>パラメーター

 _lpsrow_
  
> 順番追加する行を記述する[srow](srow.md)構造体へのポインター、または既存の行を置換するためのポインター。 **srow**構造の**lpprops**メンバーによって参照されるプロパティ値構造の1つに、インデックス列、CreateTable への呼び出しで_ulPropTagIndexColumn_パラメーターで指定したものと同じ値が含まれている必要があります。 [](createtable.md)関数。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に挿入または変更されました。
    
MAPI_E_INVALID_PARAMETER 
  
> 渡された行にインデックス列がありません。
    
## <a name="remarks"></a>注釈

**itabledata:: hrmodifyrow**メソッドは、 _lpsrow_パラメーターで指定された**srow**構造によって示される行を挿入します。 テーブル内に既に存在する_lpsrow_と同じ値のインデックス列の行がある場合、既存の行は置き換えられます。 **srow**構造に含まれるものと一致する行が存在しない場合、 **hrmodifyrow**はテーブルの末尾に行を追加します。 
  
テーブルのすべてのビューが変更され、 _lpsrow_によって示される行が含まれるようになります。 ただし、その行を除外する制限がビューにある場合は、ユーザーに表示されないことがあります。 
  
_lpsrow_によって参照される行の列は、テーブル内の列と同じ順序である必要はありません。 また、呼び出し元には、現在テーブルにない列のプロパティを含めることもできます。 既存のビューの場合、 **hrmodifyrow**によって、これらの新しい列が使用可能になりますが、現在の列のセットには含まれません。 今後のビューの場合、 **hrmodifyrow**には列セットの新しい列が含まれます。 
  
**hrmodifyrow**が行を追加すると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知を登録するためにテーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

