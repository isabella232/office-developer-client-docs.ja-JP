---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317277"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMSLogon:: Advise](imslogon-advise.md)メソッドの呼び出しを使用して、以前に作成されたメッセージストア変更の通知用のオブジェクトの登録を削除します。 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulconnection_
  
> 順番**IMSLogon:: Advise**への呼び出しによって返される登録接続の番号。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

メッセージストアプロバイダーは**IMSLogon:: アドバイズ**アドバイスを実装して、前の**IMSLogon:: アドバイズ**の_lpAdviseSink_パラメーターで渡されたアドバイズシンクオブジェクトへのポインターを解放し、通知を取り消します。レジスタ. アドバイズシンクオブジェクトへのポインターを破棄する一環として、オブジェクトの[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドが呼び出されます。 通常、**リリース**は、**アドバイズ**中止呼び出し中に呼び出されます。 ただし、別のスレッドがアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合、 **Release**呼び出しは**onnotify**メソッドが戻るまで遅延します。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

