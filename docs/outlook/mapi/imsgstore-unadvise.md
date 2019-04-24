---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309724"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMsgStore:: Advise](imsgstore-advise.md)メソッドへの呼び出しによって、以前に設定された通知の送信をキャンセルします。 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulconnection_
  
> 順番アクティブな通知登録に関連付けられている接続番号。 _ulconnection_の値は、 **IMsgStore:: Advise**メソッドへの以前の呼び出しによって返されたものである必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が正常にキャンセルされました。
    
## <a name="remarks"></a>解説

**IMsgStore:: アドバイズ**中止メソッドは、通知の登録をキャンセルします。 **アドバイズ**中止は、登録に使用された**アドバイズ**呼び出しで受け取った発信者のアドバイズシンクへのポインターを解放します。 
  
通常、 **** アドバイズ中止呼び出し中にアドバイズシンクの[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッド**** を呼び出します。 ただし、アドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出しているプロセスに別のスレッドがある場合は、 **onnotify**メソッドが戻るまで**リリース**呼び出しが遅延します。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

