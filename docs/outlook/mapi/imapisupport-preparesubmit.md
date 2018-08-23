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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800801"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**適用対象**: Outlook 
  
MAPI スプーラーに送信するためには、メッセージを準備します。
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]準備するのには、メッセージへのポインター。
    
 _lpulFlags_
  
> [で [チェック アウト]入力では、 _lpulFlags_パラメーターは予約されており、0 にする必要があります。 出力では、 _lpulFlags_は NULL にする必要があります。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージの準備ができました。
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::PrepareSubmit**メソッドを実装します。 メッセージ ストア プロバイダーは、MAPI スプーラーに送信するためのメッセージを準備するのには[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの実装では、 **PrepareSubmit**を呼び出します。 
  
 **PrepareSubmit**は、MSGFLAG_RESEND フラグが、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティで設定されたメッセージを処理するために使用されます。 MSGFLAG_RESEND は、最初の送信が失敗したときに再送信する要求を含むメッセージに設定されています。 メッセージを正常に受信する受信者の一覧で受信者の指定しませんでしたが、 **PrepareSubmit**が決定します。 
  
受信者の一覧にアクセスするには、 **PrepareSubmit**は、メッセージの[IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出します。 受信者のデータを取得するのには、 **PrepareSubmit**は、受信者テーブルの[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。 テーブル内の各行の**PrepareSubmit**は**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティをチェックし、次の操作のいずれか。
  
- MAPI_SUBMITTED フラグが設定されている場合、 **PrepareSubmit**はフラグをクリアし、**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを FALSE に設定します。
    
- MAPI_SUBMITTED フラグが設定されていない場合、 **PrepareSubmit**は**PR_RECIPIENT_TYPE**を MAPI_P1 に変更し、true を指定する**れない**を設定します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareSubmit**を呼び出すと、前に、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出したあり、 _ulFlags_パラメーターに NOTIFY_READYTOSEND フラグを設定することを確認してください。 **SpoolerNotify**の呼び出しは、 **PrepareSubmit**への呼び出しの前にセッションごとに 1 回行う必要があります。 **SpoolerNotify**では、MAPI スプーラーを同期し、により、ログオンしているすべての必要なトランスポート プロバイダーのアドレスの種類を登録します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

