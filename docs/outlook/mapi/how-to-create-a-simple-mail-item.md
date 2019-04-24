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
# <a name="create-a-simple-mail-item"></a><span data-ttu-id="ffd69-103">単純なメール アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="ffd69-103">Create a simple mail item</span></span>
  
<span data-ttu-id="ffd69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffd69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffd69-105">MAPI を使用して、開封確認を要求するメッセージを作成して送信することができます。</span><span class="sxs-lookup"><span data-stu-id="ffd69-105">MAPI can be used to create and send a message that requests a read receipt.</span></span> <span data-ttu-id="ffd69-106">開封確認が要求されると、メッセージングシステムは、受信者がメッセージを開いたときに送信者に開封レポートを生成して返します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-106">When a read receipt is requested, the messaging system generates and returns a read report to the sender when the recipient opens the message.</span></span>
  
<span data-ttu-id="ffd69-107">このトピックで参照されている mfcmapi アプリケーションおよび createoutlookitemsaddin プロジェクトからコードをダウンロード、表示、および実行する方法については、[このセクションで使用しているサンプルをインストール](how-to-install-the-samples-used-in-this-section.md)するを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffd69-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a><span data-ttu-id="ffd69-108">開封確認メッセージを要求するメッセージを作成して送信するには</span><span class="sxs-lookup"><span data-stu-id="ffd69-108">To create and send a message requesting a read receipt</span></span>

1. <span data-ttu-id="ffd69-109">送信メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-109">Create an outgoing message.</span></span> <span data-ttu-id="ffd69-110">送信メッセージを作成する方法については、「[送信メッセージの処理](handling-an-outgoing-message.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffd69-110">For information about how to create an outgoing message, see [Handling an Outgoing Message](handling-an-outgoing-message.md).</span></span>
    
2. <span data-ttu-id="ffd69-111">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティを追加し、 **true**に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-111">Add the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and set it to **true**.</span></span>
    
3. <span data-ttu-id="ffd69-112">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) プロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-112">Add the **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
4. <span data-ttu-id="ffd69-113">**PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) プロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-113">Add the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="ffd69-114">[IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出して、メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-114">Send the message by calling the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> 
    
<span data-ttu-id="ffd69-115">createoutlookitemsaddin プロジェクトのメール .cpp ソースファイルの関数は、 `AddMail`これらの手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="ffd69-115">The  `AddMail` function in the Mails.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="ffd69-116">この`AddMail`関数は、mfcmapi サンプルアプリケーションの [ **Addins** ] メニューの [**メールの追加**] コマンドをクリックしたときに表示される [**メールの追加**] ダイアログボックスのパラメーターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="ffd69-116">The  `AddMail` function takes parameters from the **Add Mail** dialog box that is displayed when you click the **Add Mail** command on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="ffd69-117">メール`DisplayAddMailDialog`ボックスの関数は、ダイアログボックスを表示して、ダイアログボックスの値を`AddMail`関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-117">The  `DisplayAddMailDialog` function in Mails.cpp displays the dialog box and passes the values from the dialog box to the  `AddMail` function.</span></span> <span data-ttu-id="ffd69-118">この`DisplayAddMailDialog`関数は MAPI を使用したメールアイテムの作成に直接関連付けられていないため、ここには記載されていません。</span><span class="sxs-lookup"><span data-stu-id="ffd69-118">The  `DisplayAddMailDialog` function does not relate directly to creating a mail item using MAPI, so it is not listed here.</span></span> <span data-ttu-id="ffd69-119">`AddMail`関数は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ffd69-119">The  `AddMail` function is listed below.</span></span> 
  
<span data-ttu-id="ffd69-120">メソッドに渡される_lpfolder_パラメーターは、新しいメッセージが作成されるフォルダーを表す[imapifolder](imapifolderimapicontainer.md)インターフェイスへのポインターであることに注意してください。 `AddMail`</span><span class="sxs-lookup"><span data-stu-id="ffd69-120">Note that the  _lpFolder_ parameter passed to the  `AddMail` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new message will be created.</span></span> <span data-ttu-id="ffd69-121">**imapifolder**インターフェイスを表す_lpfolder_パラメーターを指定すると、コードは[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-121">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="ffd69-122">**CreateMessage**メソッドは、成功コードと、 [IMessage: imapiprop](imessageimapiprop.md)インターフェイスへのポインターへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-122">The **CreateMessage** method returns a success code and a pointer to a pointer to an [IMessage : IMAPIProp](imessageimapiprop.md) interface.</span></span> 

<span data-ttu-id="ffd69-123">ほとんどの`AddMail`関数コードは、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すための準備として、プロパティを設定する作業を処理します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-123">Most of the  `AddMail` function code handles the work of setting properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="ffd69-124">**setprops**メソッドの呼び出しが成功した場合、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すと、変更内容がストアにコミットされ、新しいメールアイテムが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ffd69-124">If the call to the **SetProps** method succeeds, a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method commits the changes to the store and creates a new mail item.</span></span> <span data-ttu-id="ffd69-125">その後、要求された場合、メッセージを送信するために[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ffd69-125">Then, if requested, the [IMessage::SubmitMessage](imessage-submitmessage.md) method is called to send the message.</span></span> 
  
<span data-ttu-id="ffd69-126">`AddMail`関数は、 `BuildConversationIndex` 2 つのヘルパー関数を使用して、 **PR_CONVERSATION_INDEX**プロパティと**PR_REPORT_TAG**プロパティ`AddReportTag`の値 (および関数) を作成します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-126">The  `AddMail` function uses two helper functions to build values for the **PR_CONVERSATION_INDEX** and **PR_REPORT_TAG** properties: the  `BuildConversationIndex` and  `AddReportTag` functions.</span></span> <span data-ttu-id="ffd69-127">createoutlookitemsaddin .cpp にある`BuildConversationIndex`関数は、親の会話インデックスが渡されない場合に、組み込みの MAPI の[ScCreateConversationIndex](sccreateconversationindex.md)関数が実行するのと同じ動作をします。</span><span class="sxs-lookup"><span data-stu-id="ffd69-127">The  `BuildConversationIndex` function, located in CreateOutlookItemsAddin.cpp, does the same work that the built-in MAPI [ScCreateConversationIndex](sccreateconversationindex.md) function does when a parent conversation index is not passed to it.</span></span> <span data-ttu-id="ffd69-128">これらの関数が生成する会話インデックスバッファーの形式については、 [PidTagConversationIndex 標準プロパティ](pidtagconversationindex-canonical-property.md)で説明されています。</span><span class="sxs-lookup"><span data-stu-id="ffd69-128">The format of the conversation index buffer that these functions generate is documented in [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md).</span></span> 

<span data-ttu-id="ffd69-129">PR_REPORT_TAG `AddReportTag`プロパティの構造を構築するために、メール .cpp に`BuildReportTag`ある関数が呼び出されます。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ffd69-129">The  `AddReportTag` function, located in Mails.cpp, in turn calls the  `BuildReportTag` function to build a structure for the **PR_REPORT_TAG** property.</span></span> <span data-ttu-id="ffd69-130">`BuildReportTag`関数によって構築される構造の詳細については、「 [PidTagReportTag 標準プロパティ](pidtagreporttag-canonical-property.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffd69-130">For information about the structure that the  `BuildReportTag` function builds, see [PidTagReportTag Canonical Property](pidtagreporttag-canonical-property.md).</span></span>
  
<span data-ttu-id="ffd69-131">次に、 `AddMail`関数の完全な一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="ffd69-131">The following is the complete listing of the  `AddMail` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ffd69-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffd69-132">See also</span></span>

- [<span data-ttu-id="ffd69-133">MAPI を使用して Outlook 2007 アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="ffd69-133">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

