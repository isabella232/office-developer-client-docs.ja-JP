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
  
MAPI がイベント通知を送信するために呼び出すコールバック関数を定義します。 このコールバック関数は [、HrAllocAdviseSink](hrallocadvisesink.md) 関数を呼び出して作成されたアアドバイス シンク オブジェクトにラップされた場合にのみ使用できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>パラメーター

 _lpvContext_
  
> [in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される任意の値へのポインター。 この値は、クライアント アプリケーションまたはサービス プロバイダーにとって重要なアドレスを表します。 通常、C++ コードの場合  _、lpvContext_ パラメーターは C++ オブジェクトへのポインターを表します。 
    
 _cNotification_
  
> [in]  _lpNotifications_ パラメーターで示される配列内のイベント通知の数。 
    
 _lpNotifications_
  
> [out]この関数がイベント通知を含む [NOTIFICATION](notification.md) 構造体の配列を書き込む場所へのポインター。 
    
## <a name="return-value"></a>戻り値

**NOTIFCALLBACK** 関数プロトタイプの有効な戻り値のセットは、関数がクライアント アプリケーションまたはサービス プロバイダーによって実装されるかどうかによって異なります。 クライアントは常にクライアントを返S_OK。 プロバイダーは、ユーザーまたはS_OKをCALLBACK_DISCONTINUE。 
  
## <a name="remarks"></a>注釈

CALLBACK_DISCONTINUEは、同期コールバック関数の有効な戻り値です。MAPI は、この通知のコールバックの処理を直ちに停止する要求をします。 MAPI CALLBACK_DISCONTINUEが返される場合、MAPI は [IMAPISupport::Notify](imapisupport-notify.md)から返される _lpUlFlags_ パラメーターを NOTIFY_CANCELED に設定します。 
  
同期コールバック関数で実行できる操作に関する制限を次に示します。
  
- 別の同期通知を生成することはできません。
    
- ユーザー インターフェイスを表示できません。
    
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

