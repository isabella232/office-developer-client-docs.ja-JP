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
  
MAPI を使用して、受信確認を要求するメッセージを作成して送信できます。 受信確認が要求された場合、メッセージング システムは、受信者がメッセージを開くと、送信者に読み取りレポートを生成して返します。
  
このトピックで参照されている MFCMAPI アプリケーションおよび CreateOutlookItemsAddin プロジェクトからコードをダウンロード、表示、実行する方法については、「このセクションで使用されるサンプルのインストール」を参照 [してください](how-to-install-the-samples-used-in-this-section.md)。


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>受信確認を要求するメッセージを作成して送信するには

1. 送信メッセージを作成します。 送信メッセージを作成する方法については、「送信メッセージの処理 [」を参照してください](handling-an-outgoing-message.md)。
    
2. プロパティを **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティを追加し、true に設定 **します**。
    
3. [プロパティ] **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティを追加します。
    
4. [プロパティ] **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) プロパティを追加します。
    
5. [IMessage::SubmitMessage メソッドを呼び出してメッセージを送信](imessage-submitmessage.md)します。 
    
`AddMail`CreateOutlookItemsAddin プロジェクトの Mails.cpp ソース ファイルの関数は、次の手順を示しています。 この関数は、MFCMAPI サンプル アプリケーションの [Addins] メニューの [メールの追加] コマンドをクリックすると表示される [メールの追加] ダイアログ ボックスからパラメーター `AddMail` を受け取ります。    `DisplayAddMailDialog`Mails.cpp の関数はダイアログ ボックスを表示し、ダイアログ ボックスから関数に値を渡 `AddMail` します。 この関数は、MAPI を使用したメール アイテムの作成とは直接関係ないので、ここに  `DisplayAddMailDialog` は表示されません。 関数  `AddMail` の一覧を以下に示します。 
  
メソッドに  _渡される lpFolder_ パラメーターは、新しいメッセージが作成されるフォルダーを表す  `AddMail` [IMAPIFolder](imapifolderimapicontainer.md) インターフェイスへのポインターです。 _IMAPIFolder インターフェイスを_ 表す **lpFolder** パラメーターを指定すると、このコードは [IMAPIFolder::CreateMessage メソッドを呼び出](imapifolder-createmessage.md)します。 **CreateMessage メソッド** は、成功コードと [IMessage : IMAPIProp](imessageimapiprop.md)インターフェイスへのポインターを返します。 

ほとんどの関数コード  `AddMail` は [、IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出す準備としてプロパティを設定する作業を処理します。 **SetProps** メソッドの呼び出しが成功すると [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの呼び出しがストアに対する変更をコミットし、新しいメール アイテムを作成します。 次に、要求された場合は、メッセージを送信するために [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドが呼び出されます。 
  
この `AddMail` 関数は、2 つのヘルパー関数を使用して、PR_CONVERSATION_INDEXプロパティとPR_REPORT_TAGプロパティの **値** `BuildConversationIndex` を作成 `AddReportTag` します。 `BuildConversationIndex`CreateOutlookItemsAddin.cpp にある関数は、組み込みの MAPI [ScCreateConversationIndex](sccreateconversationindex.md)関数が親会話インデックスが渡されない場合と同じ作業を行います。 これらの関数が生成する会話インデックス バッファーの形式は [、PidTagConversationIndex 標準プロパティに記載されています](pidtagconversationindex-canonical-property.md)。 

Mails.cpp にある関数は、関数を呼び出して、PR_REPORT_TAG  `AddReportTag`  `BuildReportTag` プロパティ **の構造を構築** します。 関数が構築する構造の詳細については  `BuildReportTag` [、「PidTagReportTag 標準プロパティ」を参照してください](pidtagreporttag-canonical-property.md)。
  
関数の完全な一覧を次に示  `AddMail` します。 
  
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

