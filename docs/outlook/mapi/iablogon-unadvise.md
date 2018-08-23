---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d9f69098f9c53e75dea6f485248d61d277e181c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800356"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**適用対象**: Outlook 
  
[IABLogon::Advise](iablogon-advise.md)メソッドの呼び出しで以前設定された通知をキャンセルします。 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]作業中の通知の登録に関連付けられている接続の数です。 **アドバイズ**する前回の呼び出しには、 _ulConnection_の値を返す必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知の登録は取り消されました。
    
## <a name="remarks"></a>注釈

MAPI では、メッセージングのユーザーまたは配布リスト オブジェクトのコンテナーであり、通知の登録をキャンセルするのには**Unadvise**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**Unadvise**の実装は、MAPI のヘルプまたは手動での通知をサポートするかどうかに依存します。 MAPI のサポートを提供する場合は、登録をキャンセルする[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)メソッドを呼び出します。 別のスレッドがアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、 **OnNotify**が返されるまで遅延できます。 
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 使用する方法の詳細については、 [IMAPISupport: IUnknown](imapisupportiunknown.md)通知をサポートするメソッドは、[イベント通知をサポートしている](supporting-event-notification.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

