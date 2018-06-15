---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800399"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**適用されます**: Outlook 
  
アドレス帳エントリを以前に確立された通知の登録をキャンセルします。
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in]キャンセルするのには登録を表す接続の数です。 _UlConnection_パラメーターには、 [IAddrBook::Advise](iaddrbook-advise.md)メソッドへの前回の呼び出しによって返される値が含まれている必要があります。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 登録は取り消されました。
    
## <a name="remarks"></a>Remarks

クライアントは、特定のアドレス帳のエントリへの変更に関する通知の受信を停止するのには**Unadvise**メソッドを呼び出します。 通知の登録をキャンセルする場合、呼び出し元へのポインターは、シンクをアドバイスのアドレス帳プロバイダーのリリースです。 ただし、リリース発生**Unadvise**の呼び出し時に、または後で、別のスレッドが、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合。 進行状況の通知がある場合、リリースは**OnNotify**メソッドが戻るまで遅延します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

