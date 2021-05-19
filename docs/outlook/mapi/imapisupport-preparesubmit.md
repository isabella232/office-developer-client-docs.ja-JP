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
  
MAPI スプーラーに送信するメッセージを準備します。
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]準備するメッセージへのポインター。
    
 _lpulFlags_
  
> [in, out]入力では  _、lpulFlags_ パラメーターは予約済みで、ゼロである必要があります。 出力では  _、lpulFlags は_ NULL である必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常に準備されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::P repareSubmit** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは [、IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの実装で **PrepareSubmit** を呼び出して、MAPI スプーラーに送信するメッセージを準備します。 
  
 **PrepareSubmit を** 使用して、MSGFLAG_RESEND ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに PR_MESSAGE_FLAGS フラグが設定 **されている** メッセージを処理します。 MSGFLAG_RESEND送信が失敗した場合に再送信する要求を含むメッセージに対して設定されます。 **PrepareSubmit は** 、受信者リスト内の受信者がメッセージを正常に受信し、受信しなかった受信者を決定します。 
  
受信者リストにアクセスするには **、PrepareSubmit は** メッセージの [IMessage::GetRecipientTable メソッドを呼び出](imessage-getrecipienttable.md) します。 受信者データを取得するには **、PrepareSubmit は** 受信者テーブルの [IMAPITable::QueryRows メソッドを呼び出](imapitable-queryrows.md) します。 テーブル内の各行について **、PrepareSubmit** は PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティをチェックし、次のいずれかのアクションを実行します。
  
- このフラグMAPI_SUBMITTED設定されている場合 **、PrepareSubmit** はフラグをクリアし、PR_RESPONSIBILITY **(** [PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを FALSE に設定します。
    
- このフラグMAPI_SUBMITTED設定されていない場合は **、PrepareSubmit** は設定PR_RECIPIENT_TYPEにMAPI_P1し、PR_RESPONSIBILITY **TRUE** に設定します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareSubmit** を呼び出す前に [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出し _、ulFlags_ パラメーターに NOTIFY_READYTOSEND フラグを設定してください。 **SpoolerNotify 呼び出し** は **、PrepareSubmit** の呼び出しの前にセッションごとに 1 回行う必要があります。 **SpoolerNotify** は MAPI スプーラーを同期し、必要なすべてのトランスポート プロバイダーがログオンし、そのアドレスの種類が登録されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

