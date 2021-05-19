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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335703"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPISession::Advise](imapisession-advise.md)メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]アクティブな通知登録に関連付けられている接続番号。 _ulConnection の値は_**、IMAPISession::Advise** への以前の呼び出しによって返されている必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が正常に取り消されました。
    
## <a name="remarks"></a>注釈

**IMAPISession::Unadvise** メソッドは、通知の登録を取り消します。 **Unadvise は**、登録に使用される Advise 呼び出しで受け取った呼び出し元のアアドバイス シンクへのポインターを解放します。 
  
一般に **、Unadvise は Unadvise** 呼び出し中に、アアドバイス シンクの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) **メソッドを呼び出** します。 ただし、別のスレッドがアアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す過程にある場合 **、OnNotify** メソッドが返されるまで、Release 呼び出しは遅延されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

