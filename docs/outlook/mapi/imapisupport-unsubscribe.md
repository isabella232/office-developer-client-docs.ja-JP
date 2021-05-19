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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421215"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)メソッドへの呼び出しで以前に確立された通知の送信の責任を取り消します。 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in] **IMAPISupport::Subscribe** を介して以前に確立された通知登録を表す 0 以外の接続番号。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録が取り消されました。
    
MAPI_E_NOT_FOUND 
  
> _ulConnection_ パラメーターで渡された接続番号が存在しません。 
    
## <a name="remarks"></a>注釈

**IMAPISupport::Unsubscribe** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは Unsubscribe **を呼び** 出して、サブスクライブによって以前に設定された通知登録を **取り消します**。 **Unsubscribe** は、Subscribe 呼び出しで渡されたアアドバイス シンク ポインターを解放して、登録を **取り消** します。 
  
通常、アアドバイス シンクの **IUnknown::Release** メソッドは、Unsubscribe 呼び出し中に **呼び出** されます。 ただし、別のスレッドが、アドバイス シンク オブジェクト [の IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す過程にある場合 **、OnNotify** メソッドが返されるまで、Release 呼び出しは遅延されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

