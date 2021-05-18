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
  
テーブルで進行中の 1 つ以上の非同期操作が完了するまで、処理を中断します。
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
 _ulTimeout_
  
> [in]非同期操作または操作が完了するまで待機する最大ミリ秒数。 完了するまで無期限に待機するには  _、ulTimeout_ を 0xFFFFFFFF。 
    
 _lpulTableStatus_
  
> [in, out]入力時に、有効なポインターまたは NULL のいずれか。 出力時に  _、lpulTableStatus_ が有効なポインターである場合は、表の最新の状態を指します。 _lpulTableStatus が_ NULL の場合、状態情報は返されません。 **WaitForCompletion が** 失敗した HRESULT 値を返す場合 _、lpulTableStatus_ の内容は未定義です。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 待機操作が成功しました。
    
MAPI_E_NO_SUPPORT 
  
> この表では、非同期操作の完了を待機する機能はサポートされていません。
    
MAPI_E_TIMEOUT 
  
> 指定された時間内に非同期操作または操作が完了しなかった。
    
## <a name="remarks"></a>注釈

**IMAPITable::WaitForCompletion** メソッドは、テーブルの現在進行中の非同期操作が完了するまで処理を中断します。 **WaitForCompletion** を使用すると、非同期操作を完全に完了するか  _、ulTimeout_ で示されているミリ秒単位で実行してから中断することができます。 進行中の非同期操作を検出するには [、IMAPITable::GetStatus メソッドを呼び出](imapitable-getstatus.md) します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

