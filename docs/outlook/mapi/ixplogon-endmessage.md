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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357352"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーが送信メッセージの処理を完了したことをトランスポートプロバイダーに通知します。
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulmsグリーン f_
  
> 順番[IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドを以前に呼び出したときに取得されたメッセージ固有の参照値。 
    
 _lアウトフラグ_
  
> 読み上げメッセージに対して行うべきことを MAPI スプーラーに示すフラグのビットマスク。 フラグが設定されていない場合は、メッセージが送信されています。 次のフラグを設定できます。
    
END_DONT_RESEND 
  
> この時点で、トランスポートプロバイダーには、このメッセージに関する必要な情報がすべて含まれています。 トランスポートプロバイダーがより多くの情報を必要とする場合や、メッセージを送信した場合は、NOTIFY_SENTDEFERRED フラグを使用して[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出し、メッセージのエントリ識別子を渡すことによって、MAPI スプーラーに通知します。 
    
END_RESEND_LATER 
  
> エラー状態ではない理由により、トランスポートプロバイダーが現時点でメッセージを送信していません。 メッセージを送信するには、後でトランスポートプロバイダーを呼び出す必要があります。
    
END_RESEND_NOW 
  
> トランスポートプロバイダーは、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッド呼び出しで渡されたメッセージを再起動する必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

MAPI スプーラーは、拡張配信または配信不能情報の提供に関係する処理を完了した後、 **IXPLogon:: endmessage**メソッドを呼び出します。 
  
この呼び出しが戻ると、このメッセージの_ulmsグリーン f_パラメーターの値は無効になります。 トランスポートプロバイダーは、今後のメッセージで同じ値を再利用できます。 
  
メッセージの転送中にトランスポートプロバイダが開くすべてのオブジェクトは、 **endmessage**呼び出しが戻る前に解放される必要があります。これは、MAPI スプーラーがトランスポートプロバイダーに渡すメッセージオブジェクトを除きます。 **endmessage**呼び出しの後、MAPI スプーラーによって渡されるメッセージオブジェクトは無効です。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

