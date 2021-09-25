---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0d773b5b9392c5a32ff07bc20ecdd7a1a24cb578
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576115"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳エントリに対して以前に確立された通知登録を取り消します。
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]取り消す登録を表す接続番号。 _ulConnection パラメーターには_[、IAddrBook::Advise](iaddrbook-advise.md)メソッドの前の呼び出しによって返される値を含む必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が正常に取り消されました。
    
## <a name="remarks"></a>注釈

クライアントは **Unadvise メソッドを呼** び出して、特定のアドレス帳エントリへの変更に関する通知の受信を停止します。 通知登録が取り消された場合、アドレス帳プロバイダーは発信者の通知シンクへのポインターを解放します。 ただし、別のスレッドが [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出している間に **、Unadvise** 呼び出し中または後の時点でリリースが発生する可能性があります。 通知が進行中の場合 **、OnNotify** メソッドが返されるまでリリースが遅延します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

