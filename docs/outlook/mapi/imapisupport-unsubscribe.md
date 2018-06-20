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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9ee071bb303c7518a23c5e57909f8618b7aebdde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800810"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**適用されます**: Outlook 
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)メソッドを呼び出して、以前に設定されている通知を送信するための責任をキャンセルします。 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in]**IMAPISupport::Subscribe**を経由して確立した通知の登録を表す 0 以外の接続数です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知の登録が取り消されました。
    
MAPI_E_NOT_FOUND 
  
> _UlConnection_パラメーターに渡される接続の数は存在しません。 
    
## <a name="remarks"></a>備考

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::Unsubscribe**メソッドを実装します。 サービス プロバイダーでは、**購読**していた設定、通知の登録をキャンセルする**購読の取り消し**を呼び出します。 **購読**は、**購読**の呼び出しで渡されたアドバイズ シンク ポインターを解放して、登録をキャンセルします。 
  
アドバイズ シンクの**リ ス**のメソッドが呼び出される一般的には、**購読の取り消し**の呼び出し中にします。 ただし、別のスレッドがアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

