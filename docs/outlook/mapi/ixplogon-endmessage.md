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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414159"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーが送信メッセージの処理を完了したとトランスポート プロバイダーに通知します。
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulMsgRef_
  
> [in] [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) メソッドの以前の呼び出しで取得されたメッセージ固有の参照値。 
    
 _lpulFlags_
  
> [out]メッセージで何を行う必要がある MAPI スプーラーに示すフラグのビットマスク。 フラグが設定されていない場合は、メッセージが送信されています。 次のフラグを設定できます。
    
END_DONT_RESEND 
  
> トランスポート プロバイダーには、このメッセージに関して必要なすべての情報が今のところ含まれています。 トランスポート プロバイダーが詳細な情報を必要とする場合、またはメッセージを送信したときに [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを NOTIFY_SENTDEFERRED フラグで呼び出し、メッセージのエントリ識別子を渡すことによって、MAPI スプーラーに通知します。 
    
END_RESEND_LATER 
  
> エラー状態ではない理由により、トランスポート プロバイダーは現在の時刻にメッセージを送信していない。 メッセージを送信するには、後でトランスポート プロバイダーを再度呼び出す必要があります。
    
END_RESEND_NOW 
  
> トランスポート プロバイダーは [、IMessage::SubmitMessage](imessage-submitmessage.md) メソッド呼び出しで渡されたメッセージを再起動する必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、拡張配信または配信以外の情報の提供に関連する処理を完了した後 **、IXPLogon::EndMessage** メソッドを呼び出します。 
  
この呼び出しが返された後  _、ulMsgRef_ パラメーターの値は、このメッセージに対して無効になります。 トランスポート プロバイダーは、将来のメッセージで同じ値を再利用できます。 
  
メッセージの転送中にトランスポート プロバイダーが開くすべてのオブジェクトは、MAPI スプーラーがトランスポート プロバイダーに渡すメッセージ オブジェクトを除き **、EndMessage** 呼び出しが返される前に解放する必要があります。 MAPI スプーラーによって渡されたメッセージ オブジェクトは、EndMessage 呼び出し **後に無効** です。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

