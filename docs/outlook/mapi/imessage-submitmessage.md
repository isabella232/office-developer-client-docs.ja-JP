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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1d325c67c836e727d8285bd2dceecf88bf68327c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800900"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**適用対象**: Outlook 
  
すべてのメッセージのプロパティを保存し、メッセージを送信する準備が完了としてマークを付けます。
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]メッセージの送信方法を制御するためのフラグのビットマスクです。 次のフラグを設定することができます。
    
FORCE_SUBMIT 
  
> MAPI では、すぐにメッセージを送信する必要があります。 このフラグは現在使用中です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_RECIPIENTS 
  
> メッセージの受信者テーブルは空です。
    
## <a name="remarks"></a>注釈

**IMessage::SubmitMessage**メソッドは、メッセージを送信する準備が完了としてをマークします。 MAPI は、メッセージを送信するためマークされている順序で基になるメッセージング システムに渡します。 この機能では、しばらくの間は、基になるメッセージング システムにそれを担当するためにメッセージのメッセージ ストアに常に可能性があります。 先に領収書の順序は、基になるメッセージング システムのコントロールし、メッセージの送信に使用された順序と必ずしも一致しません。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

保存し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティをチェックし、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)のメソッドを呼び出します。 MSGFLAG_RESEND フラグが設定されている場合は、 [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)を呼び出します。 **PrepareSubmit**は、再送信メッセージ内の受信者のすべての受信者の種類および**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) のプロパティを更新します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SubmitMessage**が返されると、メッセージとその関連付けられているサブオブジェクトのメッセージをフォルダー、添付ファイル、ストリーム、テーブル、およびように無効になっています。 MAPI では、各自**が**メソッドを呼び出すことを除いて、これらのポインターをその他の操作は許可されていません。 MAPI では、メッセージと関連付けられているすべてのサブオブジェクトを解放する必要があります**SubmitMessage**が呼び出された後になるよう設計されています。 ただし、 **SubmitMessage**には、存在しないか無効な情報を示すエラー値が返された場合メッセージが開いたままになり、ポインターが有効なまま維持します。 
  
送信操作を取り消す場合に、取得し、メッセージの送信前にメッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティへのポインターを格納します。 メッセージが送信された後、メッセージのエントリ id が無効になるためには、 **SubmitMessage**を呼び出す前に保存する必要があります。 送信をキャンセルするには、このエントリの識別子を_lpEntryId_パラメーターをポイントし、 [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)をコールします。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI では、 **IMessage::SubmitMessage**メソッドを使用して、選択したメッセージを送信します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

