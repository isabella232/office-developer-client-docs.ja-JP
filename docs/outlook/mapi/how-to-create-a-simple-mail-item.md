---
title: 簡易メール アイテムを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1bbf80c8f614fc5e69773407c7882f3df8c0c81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800209"
---
# <a name="create-a-simple-mail-item"></a>簡易メール アイテムを作成します。
  
**適用されます**: Outlook 
  
作成し、開封確認メッセージを要求するメッセージを送信するのには、MAPI を使用できます。 開封確認メッセージが要求されると、メッセージング システムが生成し、受信者がメッセージを開いたとき、リードのレポートを送信者に返します。
  
ダウンロード、表示、および、MFCMAPI アプリケーションと CreateOutlookItemsAddin にこのトピックで参照されるプロジェクトからコードを実行する方法の詳細については、[このセクションで使用されるサンプルのインストール](how-to-install-the-samples-used-in-this-section.md)を参照してください。


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>作成し、開封確認メッセージを要求するメッセージを送信するには

1. 送信メッセージを作成します。 送信メッセージを作成する方法の詳細については、[送信メッセージの処理](handling-an-outgoing-message.md)を参照してください。
    
2. **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) のプロパティを追加し、 **true**に設定します。
    
3. **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) のプロパティを追加します。
    
4. **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) のプロパティを追加します。
    
5. [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出すことによって、メッセージを送信します。 
    
`AddMail` CreateOutlookItemsAddin プロジェクトの Mails.cpp のソース ファイル内の関数は、次の手順を示します。 `AddMail`関数は、MFCMAPI サンプル アプリケーションで**アドイン**メニューの [**メールの追加**] をクリックするときに表示される**メールの追加**] ダイアログ ボックスからパラメーターを受け取ります。 `DisplayAddMailDialog` Mails.cpp の関数は、ダイアログ ボックスが表示され、ダイアログ ボックスから値を渡します、`AddMail`関数です。 `DisplayAddMailDialog`関数がここで記載されていないために、MAPI を使用してメール アイテムを作成するのには直接関係ありません。 `AddMail`関数は、下に表示されます。 
  
_LpFolder_パラメーターが渡されることに注意、`AddMail`は、新しいメッセージが作成されるフォルダーを表す[IMAPIFolder](imapifolderimapicontainer.md)インターフェイスへのポインター。 コードは、 **IMAPIFolder**インターフェイスを表す、 _lpFolder_パラメーターを指定するには、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 **メッセージ**を返します成功コードとポインターへのポインターを[IMessage: IMAPIProp](imessageimapiprop.md)インタ フェースです。 

ほとんどの`AddMail`関数のコードは、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出すための準備として、プロパティを設定する作業を処理します。 **SetProps**メソッドの呼び出しが成功すると、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しはストアへの変更をコミットし、新しいメール アイテムを作成します。 次に、要求された場合、メッセージを送信する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドが呼び出されます。 
  
`AddMail`関数では、2 つのヘルパー関数を使用して、 **PR_CONVERSATION_INDEX**および**PR_REPORT_TAG**のプロパティの値を作成:`BuildConversationIndex`と`AddReportTag`の関数です。 `BuildConversationIndex`関数、CreateOutlookItemsAddin.cpp、内にあるは MAPI [ScCreateConversationIndex](sccreateconversationindex.md)の組み込み関数が親の会話のインデックスがない渡されたときに同じ作業です。 これらの関数を生成する会話のインデックス バッファーのフォーマットは、[標準的なプロパティを PidTagConversationIndex](pidtagconversationindex-canonical-property.md)に記載されています。 

`AddReportTag` Mails.cpp、内にある関数を呼び出して、 `BuildReportTag` 、 **PR_REPORT_TAG**プロパティの構造を構築します。 構造に関する情報を`BuildReportTag`ビルドの機能、 [PidTagReportTag の標準的なプロパティ](pidtagreporttag-canonical-property.md)を参照してください。
  
次の完全な一覧では、`AddMail`関数です。 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a>関連項目

- [MAPI を使用して Outlook 2007 のアイテムを作成するには](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

