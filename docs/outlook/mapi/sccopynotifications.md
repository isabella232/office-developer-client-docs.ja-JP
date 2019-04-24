---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357485"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知のグループをメモリの単一のブロックにコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cntf_
  
> 順番_rgntf_パラメーターで指定された、配列内の[通知](notification.md)構造の数。 
    
 _rgntf_
  
> 順番コピーするイベント通知を定義する**通知**構造の配列へのポインター。 
    
 _pvdst_
  
> 読み上げ返された通知へのポインター。 
    
 _設計_
  
> 読み上げ(オプション) _rgntf_パラメーターによって指定された配列のサイズ (バイト単位) が格納されている変数へのポインターです。 NULL でない場合、 _pcb_パラメーターは_pvdst_パラメーターに格納されているバイト数に設定されます。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> イベント通知が正常にコピーされました。
    
E_INVALIDARG
  
> 無効な通知が発生しました。
    
## <a name="remarks"></a>解説

_pcb_パラメーターで NULL が渡された場合、コピーは実行されません。_pcb_で null 以外の値が渡された場合、 **sccopynotifications**関数は、配列のサイズと配列自体をメモリの単一のブロックにコピーします。 _pcb_が NULL でない場合は、 _pvdst_パラメーターに格納されているバイト数に設定されます。 _pvdst_パラメーターは、配列全体を格納するのに十分な大きさでなければなりません。 
  

