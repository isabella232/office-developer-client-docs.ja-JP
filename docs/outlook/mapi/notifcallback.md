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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801664"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**適用されます**: Outlook 
  
MAPI 呼び出しをイベント通知を送信するコールバック関数を定義します。 このコールバック関数は、 [HrAllocAdviseSink](hrallocadvisesink.md)関数を呼び出すことによって作成されたアドバイズ シンク オブジェクトにラップするときにのみ使用できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装される関数の定義:  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameters

 _lpvContext_
  
> [in]任意の値へのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。 この値は重要では、クライアント アプリケーションまたはサービス プロバイダーにアドレスを表すことができます。 通常、C++ コードでは、 _lpvContext_パラメーターのポインターを表します C++ オブジェクトにします。 
    
 _cNotification_
  
> [in]_LpNotifications_パラメーターで指定された配列内のイベント通知の数です。 
    
 _lpNotifications_
  
> [out]この関数が書き込む場所[通知](notification.md)の構造体の配列をバッファーへのポインターには、イベント通知が含まれています。 
    
## <a name="return-value"></a>�߂�l

**NOTIFCALLBACK**関数のプロトタイプ用の有効な戻り値のセットは、クライアント アプリケーションまたはサービス プロバイダーでこの関数を実装するかどうかによって異なります。 クライアントは、S_OK を返す常にする必要があります。 プロバイダーには、S_OK または CALLBACK_DISCONTINUE のいずれかを返すことができます。 
  
## <a name="remarks"></a>備考

CALLBACK_DISCONTINUE は、有効な戻り値の同期のコールバック関数だけです。MAPI すぐに停止するこの通知のコールバックの処理を要求します。 CALLBACK_DISCONTINUE が返された場合は、MAPI は[IMAPISupport::Notify](imapisupport-notify.md)すると、NOTIFY_CANCELED に_lpUlFlags_パラメーターを設定します。 
  
同期コールバック関数の機能に制約は、次のように。
  
- これが原因で、別の同期通知を生成することはできません。
    
- ユーザー インターフェイスを表示することはできません。
    
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

