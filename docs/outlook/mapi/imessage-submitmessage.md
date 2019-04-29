---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437365"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのメッセージのプロパティを保存し、メッセージを送信する準備が整ったことをマークします。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番メッセージの送信方法を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
FORCE_SUBMIT 
  
> MAPI はメッセージを直ちに送信する必要があります。 このフラグは現在使用されていません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_RECIPIENTS 
  
> メッセージの recipient テーブルが空です。
    
## <a name="remarks"></a>注釈

**IMessage:: submitmessage**メソッドは、メッセージを送信する準備が整ったことを示します。 MAPI は、メッセージが送信をマークされている順序で、基になるメッセージングシステムにメッセージを渡します。 この機能により、メッセージは、基礎となるメッセージングシステムが責任を持つ前に、しばらくの間メッセージストアに保持される可能性があります。 宛先での受信の順序は、基になるメッセージングシステムのコントロール内にあり、メッセージが送信された順序とは必ずしも一致しません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して保存し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティを確認します。 MSGFLAG_RESEND フラグが設定されている場合は、次のように呼び出し imapisupport を呼び出します。 [:P reparesubmit](imapisupport-preparesubmit.md)。 **PrepareSubmit**は、再送信メッセージ内のすべての受信者の受信者の種類と**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを更新します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**submitmessage**が戻ると、そのメッセージへのすべてのポインターと、それに関連付けられているサブオブジェクトメッセージ、フォルダー、添付ファイル、ストリーム、テーブルなどが無効になります。 MAPI では、これらのポインターに対して他の操作を行うことはできません。ただし、 **IUnknown:: Release**メソッドを呼び出すことはありません。 MAPI は、 **submitmessage**を呼び出した後、メッセージとすべての関連するサブオブジェクトを解放する必要があるように設計されています。 ただし、 **submitmessage**から不足または無効な情報を示すエラー値が返された場合、メッセージは開いたままになり、ポインターは有効なままとなります。 
  
送信操作を取り消すには、メッセージが送信される前に、メッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティへのポインターを取得して保存します。 メッセージのエントリ id は、メッセージの送信後に無効になるため、 **submitmessage**を呼び出す前に保存する必要があります。 送信を取り消すには、 _lな tryid_パラメーターをこのエントリ識別子にポイントし、 [IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)を呼び出します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|folderdlg  <br/> |**cfolderdlg:: onsubmitmessage** <br/> |mfcmapi は、 **IMessage:: submitmessage**メソッドを使用して、選択されたメッセージを送信します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

