---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 25f80ddce60ab5a8966a62761d234accafbb54be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800711"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**適用対象**: Outlook 
  
[IMAPISession::Advise](imapisession-advise.md)メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]作業中の通知の登録に関連付けられている接続の数です。 _UlConnection_の値は、 **IMAPISession::Advise**以前の呼び出しで返されている必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 登録は取り消されました。
    
## <a name="remarks"></a>注釈

**IMAPISession::Unadvise**メソッドは、通知の登録をキャンセルします。 **Unadvise**リリースがそのポインターを呼び出し元のシンクの登録に使用される**アドバイス**の呼び出しで、受け取ったに案内します。 
  
一般に、 **Unadvise**は**Unadvise**の呼び出し時にアドバイズ シンクの[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出します。 ただし、別のスレッドがアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

