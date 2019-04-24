---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341266"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[imapisupport:: Subscribe](imapisupport-subscribe.md)メソッドの呼び出しによって、以前に確立された通知を送信する責任を取り消します。 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulconnection_
  
> 順番**imapisupport:: Subscribe**によって既に確立された通知登録を表す0以外の接続番号。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録が取り消されました。
    
MAPI_E_NOT_FOUND 
  
> _ulconnection_パラメーターで渡された接続番号が存在しません。 
    
## <a name="remarks"></a>解説

**imapisupport:: 講読解除**メソッドは、すべてのサービスプロバイダサポートオブジェクトに実装されています。 サービスプロバイダーは**** 、**サブスクライブ**を呼び出して、以前に設定した通知登録を取り消します。 登録**解除****サブスクライブ**呼び出しで渡されたアドバイズシンクポインターを解放することによって、登録を取り消します。 
  
通常、アドバイズシンクの**IUnknown:: Release**メソッドは、登録**解除**通話中に呼び出されます。 ただし、別のスレッドがアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合、 **Release**呼び出しは**onnotify**メソッドが戻るまで遅延します。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

