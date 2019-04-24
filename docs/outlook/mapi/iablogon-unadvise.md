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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348882"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IABLogon:: Advise](iablogon-advise.md)メソッドの呼び出しで以前に設定された通知をキャンセルします。 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulconnection_
  
> 順番アクティブな通知登録に関連付けられている接続番号。 **アドバイズ**の前の呼び出しでは、 _ulconnection_の値が返されている必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知登録が正常にキャンセルされました。
    
## <a name="remarks"></a>解説

MAPI は、**アドバイズ**中止メソッドを呼び出して、コンテナー、メッセージングユーザー、または配布リストオブジェクトの通知の登録を取り消します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**アドバイズ**の実装は、MAPI のヘルプまたは手動で通知をサポートしているかどうかによって異なります。 MAPI がサポートを提供する場合は、 [imapisupport:: 講読解除](imapisupport-unsubscribe.md)メソッドを呼び出して、登録を取り消します。 別のスレッドがアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出しているプロセス内にある場合は、 **onnotify**が返されるまで遅延させることができます。 
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 [imapisupport:](imapisupportiunknown.md)通知をサポートするための IUnknown メソッドの使用方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

