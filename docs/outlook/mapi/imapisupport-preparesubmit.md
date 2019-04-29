---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425737"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーに送信するためのメッセージを準備します。
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpmessage_
  
> 順番準備するメッセージへのポインター。
    
 _lアウトフラグ_
  
> [入力]入力では、 _lな flags_パラメーターは予約されており、0である必要があります。 出力時には、 _lアウトフラグ_は NULL である必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常に準備されました。
    
## <a name="remarks"></a>注釈

**imapisupport::P reparemethod**は、メッセージストアプロバイダーサポートオブジェクトに実装されています。 メッセージストアプロバイダーは、MAPI スプーラーに送信するためのメッセージを準備するために、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドの実装で**PrepareSubmit**を呼び出します。 
  
 **PrepareSubmit**は、MSGFLAG_RESEND フラグが**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに設定されているメッセージを処理するために使用されます。 MSGFLAG_RESEND は、最初の送信に失敗したときに再送信する要求を含むメッセージに対して設定されます。 **PrepareSubmit**は、受信者一覧の受信者がメッセージを正常に受信したかどうかを判断します。 
  
受信者リストにアクセスするため、 **PrepareSubmit**はメッセージの[IMessage:: getrecipient table](imessage-getrecipienttable.md)メソッドを呼び出します。 受信者のデータを取得するために、 **PrepareSubmit**は受信者テーブルの[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出します。 **PrepareSubmit**は、表の各行に対して**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティをチェックし、次のいずれかの操作を行います。
  
- MAPI_SUBMITTED フラグが設定されている場合、 **PrepareSubmit**はフラグをクリアし、 **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを FALSE に設定します。
    
- MAPI_SUBMITTED フラグが設定されていない場合、 **PrepareSubmit**は**PR_RECIPIENT_TYPE**を MAPI_P1 に変更し、 **PR_RESPONSIBILITY**を TRUE に設定します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareSubmit**を呼び出す前に、 [imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出し、 _ulflags_パラメーターに NOTIFY_READYTOSEND フラグを設定していることを確認してください。 **SpoolerNotify**呼び出しは、 **PrepareSubmit**を呼び出す前に、セッションごとに1回実行する必要があります。 **SpoolerNotify**は、MAPI スプーラーを同期させ、必要なすべてのトランスポートプロバイダーがログオンしており、そのアドレスの種類が登録されていることを確認します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

