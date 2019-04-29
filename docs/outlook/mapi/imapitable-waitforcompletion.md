---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407061"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルで進行中の1つ以上の非同期操作が完了するまで処理を中断します。
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約語0である必要があります。
    
 _ultimeout_
  
> 順番非同期操作または操作が完了するまでの最大待機時間 (ミリ秒)。 完了するまで無期限に待機するには、 _ultimeout_を0xffffffff に設定します。 
    
 _lpultablestatus_
  
> [入力]入力では、有効なポインターまたは NULL のいずれかです。 出力では、 _lpultablestatus_が有効なポインターの場合は、テーブルの最新の状態を指します。 _lpultablestatus_が NULL の場合、ステータス情報は返されません。 **waitforcompletion**が失敗した HRESULT 値を返す場合、 _lpultablestatus_の内容は未定義です。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 待機操作が正常に完了しました。
    
MAPI_E_NO_SUPPORT 
  
> このテーブルでは、非同期操作の完了を待機することはサポートされていません。
    
MAPI_E_TIMEOUT 
  
> 非同期の操作または操作は、指定された時間内に完了しませんでした。
    
## <a name="remarks"></a>注釈

**IMAPITable:: waitforcompletion**メソッドは、テーブルに対して現在実行されているすべての非同期操作が完了するまで処理を中断します。 **waitforcompletion**を使用すると、非同期操作を完全に完了するか、または_ultimeout_で指定された回数だけ実行してから中断することができます。 進行中の非同期操作を検出するには、 [IMAPITable:: GetStatus](imapitable-getstatus.md)メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

