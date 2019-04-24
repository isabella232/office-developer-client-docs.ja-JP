---
title: 単純なメール アイテムを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8b7afa8f3c04cb479906f721db8de90e8cf66f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345194"
---
# <a name="create-a-simple-mail-item"></a>単純なメール アイテムを作成する
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI を使用して、開封確認を要求するメッセージを作成して送信することができます。 開封確認が要求されると、メッセージングシステムは、受信者がメッセージを開いたときに送信者に開封レポートを生成して返します。
  
このトピックで参照されている mfcmapi アプリケーションおよび createoutlookitemsaddin プロジェクトからコードをダウンロード、表示、および実行する方法については、[このセクションで使用しているサンプルをインストール](how-to-install-the-samples-used-in-this-section.md)するを参照してください。


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>開封確認メッセージを要求するメッセージを作成して送信するには

1. 送信メッセージを作成します。 送信メッセージを作成する方法については、「[送信メッセージの処理](handling-an-outgoing-message.md)」を参照してください。
    
2. **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティを追加し、 **true**に設定します。
    
3. **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティを追加します。
    
4. **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) プロパティを追加します。
    
5. [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出して、メッセージを送信します。 
    
createoutlookitemsaddin プロジェクトのメール .cpp ソースファイルの関数は、 `AddMail`これらの手順を示しています。 この`AddMail`関数は、mfcmapi サンプルアプリケーションの [ **Addins** ] メニューの [**メールの追加**] コマンドをクリックしたときに表示される [**メールの追加**] ダイアログボックスのパラメーターを受け取ります。 メール`DisplayAddMailDialog`ボックスの関数は、ダイアログボックスを表示して、ダイアログボックスの値を`AddMail`関数に渡します。 この`DisplayAddMailDialog`関数は MAPI を使用したメールアイテムの作成に直接関連付けられていないため、ここには記載されていません。 `AddMail`関数は以下のとおりです。 
  
メソッドに渡される_lpfolder_パラメーターは、新しいメッセージが作成されるフォルダーを表す[imapifolder](imapifolderimapicontainer.md)インターフェイスへのポインターであることに注意してください。 `AddMail` **imapifolder**インターフェイスを表す_lpfolder_パラメーターを指定すると、コードは[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。 **CreateMessage**メソッドは、成功コードと、 [IMessage: imapiprop](imessageimapiprop.md)インターフェイスへのポインターへのポインターを返します。 

ほとんどの`AddMail`関数コードは、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すための準備として、プロパティを設定する作業を処理します。 **setprops**メソッドの呼び出しが成功した場合、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すと、変更内容がストアにコミットされ、新しいメールアイテムが作成されます。 その後、要求された場合、メッセージを送信するために[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出されます。 
  
`AddMail`関数は、 `BuildConversationIndex` 2 つのヘルパー関数を使用して、 **PR_CONVERSATION_INDEX**プロパティと**PR_REPORT_TAG**プロパティ`AddReportTag`の値 (および関数) を作成します。 createoutlookitemsaddin .cpp にある`BuildConversationIndex`関数は、親の会話インデックスが渡されない場合に、組み込みの MAPI の[ScCreateConversationIndex](sccreateconversationindex.md)関数が実行するのと同じ動作をします。 これらの関数が生成する会話インデックスバッファーの形式については、 [PidTagConversationIndex 標準プロパティ](pidtagconversationindex-canonical-property.md)で説明されています。 

PR_REPORT_TAG `AddReportTag`プロパティの構造を構築するために、メール .cpp に`BuildReportTag`ある関数が呼び出されます。 **** `BuildReportTag`関数によって構築される構造の詳細については、「 [PidTagReportTag 標準プロパティ](pidtagreporttag-canonical-property.md)」を参照してください。
  
次に、 `AddMail`関数の完全な一覧を示します。 
  
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

- [MAPI を使用して Outlook 2007 アイテムを作成する](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

