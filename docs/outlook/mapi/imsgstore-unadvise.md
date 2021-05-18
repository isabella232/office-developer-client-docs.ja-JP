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
  
[IMsgStore::Advise](imsgstore-advise.md)メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]アクティブな通知登録に関連付けられている接続番号。 _ulConnection の値は_**、IMsgStore::Advise** メソッドへの以前の呼び出しによって返されている必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が正常に取り消されました。
    
## <a name="remarks"></a>注釈

**IMsgStore::Unadvise** メソッドは、通知の登録を取り消します。 **Unadvise は**、登録に使用される Advise 呼び出しで受け取った呼び出し元のアアドバイス シンクへのポインターを解放します。 
  
一般に **、Unadvise は Unadvise** 呼び出し中に、アアドバイス シンクの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) **メソッドを呼び出** します。 ただし、別のスレッドがアアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す過程にある場合 **、OnNotify** メソッドが返されるまで、Release 呼び出しは遅延されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

