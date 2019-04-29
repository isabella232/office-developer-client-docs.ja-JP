---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434019"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知を送信するために MAPI が呼び出すコールバック関数を定義します。 このコールバック関数は、 [HrAllocAdviseSink](hrallocadvisesink.md)関数を呼び出すことによって作成されたアドバイズシンクオブジェクトでラップされている場合にのみ使用できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|定義された関数の実装:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>パラメーター

 _lpvcontext_
  
> 順番MAPI がコールバック関数に渡す任意の値へのポインター。 この値は、クライアントアプリケーションまたはサービスプロバイダーにとって重要なアドレスを表すことができます。 通常、c++ コードの場合、 _lpvcontext_パラメーターは c++ オブジェクトへのポインターを表します。 
    
 _cnotification_
  
> 順番lpnotifications パラメーターで指定された、配列__ 内のイベント通知の数。 
    
 _lpnotifications_
  
> 読み上げこの関数がイベント通知を含む[通知](notification.md)構造の配列を書き込む場所へのポインター。 
    
## <a name="return-value"></a>戻り値

**NOTIFCALLBACK**関数プロトタイプに対して有効な戻り値のセットは、関数がクライアントアプリケーションまたはサービスプロバイダーで実装されているかどうかによって異なります。 クライアントは常に S_OK を返します。 プロバイダーは、S_OK または CALLBACK_DISCONTINUE のいずれかを返すことができます。 
  
## <a name="remarks"></a>注釈

CALLBACK_DISCONTINUE は、同期コールバック関数に対してのみ有効な戻り値です。この通知のコールバックの処理を直ちに停止するように MAPI に要求します。 CALLBACK_DISCONTINUE が返されると、MAPI は[imapisupport:: NOTIFY](imapisupport-notify.md)から戻るときに_lNOTIFY_CANCELED flags_パラメーターをに設定します。 
  
以下に、同期コールバック関数で可能な処理に関する制限を示します。
  
- 別の同期通知が生成されることはありません。
    
- ユーザーインターフェイスを表示することはできません。
    
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

