---
title: iaddrbookunadvise
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286984"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
以前にアドレス帳エントリに対して設定された通知登録を取り消します。
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulconnection_
  
> 順番キャンセルする登録を表す接続番号。 _ulconnection_パラメーターには、以前の[IAddrBook:: Advise](iaddrbook-advise.md)メソッドの呼び出しによって返される値を含める必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が正常にキャンセルされました。
    
## <a name="remarks"></a>解説

クライアントは、**アドバイズ**中止メソッドを呼び出して、特定のアドレス帳エントリへの変更に関する通知を受信しないようにします。 通知登録が取り消されると、アドレス帳プロバイダーは、呼び出し元のアドバイズシンクへのポインターを解放します。 ただし、リリースは、**アドバイズ**中止通話中、またはそれ以降の時点で、別のスレッドが[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合に発生する可能性があります。 通知が進行中の場合、 **onnotify**メソッドが戻るまでリリースは遅延します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

