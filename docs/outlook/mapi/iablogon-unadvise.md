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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424078"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IABLogon::Advise](iablogon-advise.md)メソッドへの呼び出しで以前に設定された通知をキャンセルします。 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]アクティブな通知登録に関連付けられている接続番号。 Advise の以前の **呼び出しでは**_、ulConnection の値が返されている必要があります_。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知登録が正常に取り消されました。
    
## <a name="remarks"></a>注釈

MAPI は **Unadvise メソッドを呼** び出して、コンテナー、メッセージング ユーザー、または配布リスト オブジェクトの通知登録を取り消します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**Unadvise の実装は**、MAPI のヘルプを使用して通知をサポートするか手動でサポートするかによって異なります。 MAPI がサポートを提供している場合は [、IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) メソッドを呼び出して登録を取り消します。 別のスレッドがアアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドを呼び出す過程にある場合 **、OnNotify** が返されるまで遅延する可能性があります。 
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。 [IMAPISupport : IUnknown](imapisupportiunknown.md)メソッドを使用して通知をサポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。
  
## <a name="see-also"></a>関連項目



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

