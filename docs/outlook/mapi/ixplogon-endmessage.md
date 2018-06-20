---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f81a0c3c9a9ad0a9bcef5c5685aa5b343237f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801245"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**適用されます**: Outlook 
  
トランスポート プロバイダーは、MAPI スプーラーに送信メッセージの処理が完了したことを通知します。
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulMsgRef_
  
> [in][IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドへの以前の呼び出しで取得したメッセージに固有の参照値です。 
    
 _lpulFlags_
  
> [out]メッセージで行う必要があります、MAPI スプーラーを示すフラグのビットマスクです。 フラグが設定されていない場合、メッセージは送信されました。 次のフラグを設定することができます。
    
END_DONT_RESEND 
  
> トランスポート プロバイダーは、ここではこのメッセージが表示に必要なすべての情報を持ちます。 トランスポート プロバイダーは、詳細を必要とする場合、またはメッセージを送信したときは、NOTIFY_SENTDEFERRED フラグを指定して[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出すことによって、メッセージのエントリ id を渡すことによって、MAPI スプーラーを通知します。 
    
END_RESEND_LATER 
  
> トランスポート プロバイダーは、エラー条件ではないため現時点でのメッセージを送信しません。 トランスポート プロバイダーは、呼び出す必要がありますもう一度メッセージを送信するのには後でします。
    
END_RESEND_NOW 
  
> トランスポート プロバイダーは、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの呼び出しで渡されたメッセージを再起動する必要があります。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>備考

MAPI スプーラーは、拡張の配信または配信不能の情報を提供することに関連する処理が完了した後に、 **IXPLogon::EndMessage**メソッドを呼び出します。 
  
この呼び出しが返されると、 _ulMsgRef_パラメーターの値はこのメッセージに対して有効ではありません。 トランスポート プロバイダーは、今後のメッセージに同じ値を再利用できます。 
  
MAPI スプーラーは、トランスポート プロバイダーに渡されるメッセージ オブジェクトを除いて、 **EndMessage**呼び出しが戻る前にトランスポート プロバイダーがメッセージの転送中に表示されるすべてのオブジェクトを解放する必要があります。 MAPI スプーラーによって渡されるメッセージ オブジェクトは、 **EndMessage**の呼び出しの後は有効ではありません。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

