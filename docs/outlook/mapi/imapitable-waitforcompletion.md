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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a3343381709b7ce3370ba481ad8dbb935c7d4165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586950"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
1 つまたは複数の非同期操作の進行状況でテーブルに完了するまでの処理を中断します。
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
 _ulTimeout_
  
> [in]非同期操作または操作が完了するまで待機するミリ秒単位の最大数。 完了が発生するまで無期限に待機するには、 _ulTimeout_を 0 xffffffff に設定します。 
    
 _lpulTableStatus_
  
> [で [チェック アウト]有効なポインターまたは NULL のいずれかは、入力します。 出力では、 _lpulTableStatus_が有効なポインターである場合、ポイント テーブルの最新の状態にします。 _LpulTableStatus_が NULL の場合は、ステータス情報は返されません。 **WaitForCompletion**失敗の HRESULT 値が返された場合の_lpulTableStatus_の内容は定義されていません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 待ち操作が正常に完了しました。
    
MAPI_E_NO_SUPPORT 
  
> テーブルは、非同期操作の完了の待機をサポートしていません。
    
MAPI_E_TIMEOUT 
  
> 非同期操作または操作は、指定した時間に完了しませんでした。
    
## <a name="remarks"></a>注釈

**IMAPITable::WaitForCompletion**メソッドは、テーブルのため現在の非同期操作が完了するまでの処理を中断します。 **WaitForCompletion**ことができます、非同期操作のいずれか完全に完了または中断される前に、 _ulTimeout_で示されたミリ秒数を実行します。 進行中の非同期操作を検出するためには、 [IMAPITable::GetStatus](imapitable-getstatus.md)メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

