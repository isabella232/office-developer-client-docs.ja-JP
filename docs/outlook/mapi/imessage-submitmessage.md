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
  
メッセージのすべてのプロパティを保存し、メッセージを送信準備完了としてマークします。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]メッセージの送信方法を制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
FORCE_SUBMIT 
  
> MAPI は、すぐにメッセージを送信する必要があります。 このフラグは現在使用されていない。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_RECIPIENTS 
  
> メッセージの受信者テーブルが空です。
    
## <a name="remarks"></a>注釈

**IMessage::SubmitMessage** メソッドは、メッセージを送信する準備ができているとマークします。 MAPI は、基になるメッセージング システムに、メッセージが送信用にマークされている順序でメッセージを渡します。 この機能により、基になるメッセージング システムがメッセージ を処理する前に、メッセージがメッセージ ストアに一時残る場合があります。 宛先での受信の順序は、基になるメッセージング システムのコントロール内にあるため、メッセージが送信された順序と必ずしも一致しません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出して保存し、メッセージの PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティを確認します。 このフラグMSGFLAG_RESEND設定されている場合は [、IMAPISupport::P repareSubmit を呼び出します](imapisupport-preparesubmit.md)。 **PrepareSubmit は** 、再送信メッセージ内 **PR_RESPONSIBILITY** 受信者の受信者の種類とプロパティ [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)を更新します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SubmitMessage が** 返される場合、メッセージとその関連付けられたサブオブジェクトメッセージ、フォルダー、添付ファイル、ストリーム、テーブルなどへのすべてのポインターは無効になります。 MAPI は **、IUnknown::Release** メソッドを呼び出す以外は、これらのポインターに対するそれ以上の操作を許可しない。 MAPI は **、SubmitMessage** が呼び出された後、メッセージと関連付けられているすべてのサブオブジェクトを解放するように設計されています。 ただし **、SubmitMessage が** 欠落または無効な情報を示すエラー値を返した場合、メッセージは開いたままで、ポインターは有効なままです。 
  
送信操作をキャンセルするには、メッセージが送信される前に、メッセージの PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティへのポインターを取得して格納します。 メッセージのエントリ識別子は、メッセージの送信後に無効になりますので **、SubmitMessage** を呼び出す前に保存する必要があります。 送信をキャンセルするには  _、lpEntryId_ パラメーターをこのエントリ識別子にポイントし [、IMsgStore::AbortSubmit を呼び出します](imsgstore-abortsubmit.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI は **、IMessage::SubmitMessage** メソッドを使用して、選択したメッセージを送信します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

