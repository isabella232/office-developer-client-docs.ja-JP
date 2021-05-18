---
title: 送信メッセージの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407628"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="4f231-103">送信メッセージの処理</span><span class="sxs-lookup"><span data-stu-id="4f231-103">Handling an outgoing message</span></span>

<span data-ttu-id="4f231-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f231-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f231-105">送信メッセージとは、1 つ以上のメッセージング システムで 1 つ以上の受信者に送信したり、メッセージ ストア内のフォルダーに投稿したりできるメッセージです。</span><span class="sxs-lookup"><span data-stu-id="4f231-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="4f231-106">送信メッセージの作成と送信</span><span class="sxs-lookup"><span data-stu-id="4f231-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="4f231-107">既定のメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f231-107">Open the default message store.</span></span> <span data-ttu-id="4f231-108">詳細については、「メッセージ ストアを [開く」および「](opening-a-message-store.md) 既定 [のメッセージ ストアを開く」を参照してください](opening-the-default-message-store.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="4f231-109">[送信ボックス] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f231-109">Open the Outbox folder.</span></span> <span data-ttu-id="4f231-110">詳細については、「メッセージ ストア フォルダー [を開く」を参照してください](opening-a-message-store-folder.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="4f231-111">Outbox フォルダーの **IMAPIFolder::CreateMessage** メソッドを呼び出して、新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f231-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="4f231-112">詳細については [、「IMAPIFolder::CreateMessage 」 を参照してください](imapifolder-createmessage.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="4f231-113">1 つ以上の解決済み受信者を含む受信者リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f231-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="4f231-114">詳細については、「受信者リストの [作成」を参照してください](creating-a-recipient-list.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="4f231-115">必要に応じて、件名を追加します。</span><span class="sxs-lookup"><span data-stu-id="4f231-115">Optionally, add a subject.</span></span> <span data-ttu-id="4f231-116">詳細については、「メッセージサブジェクトの [作成」を参照してください](creating-a-message-subject.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="4f231-117">メッセージ テキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f231-117">Add the message text.</span></span> <span data-ttu-id="4f231-118">詳細については、「メッセージ テキストの作成 [」を参照してください](creating-message-text.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="4f231-119">メッセージ テキストが書式設定されている場合は、レンダリング情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="4f231-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="4f231-120">詳細については、「書式設定されたテキスト [にレンダリング情報を追加する」を参照してください](adding-rendering-information-to-formatted-text.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="4f231-121">必要に応じて、1 つ以上の添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f231-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="4f231-122">詳細については、「メッセージ添付ファイルの [作成」を参照してください](creating-a-message-attachment.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="4f231-123">必要に応じて他のメッセージ プロパティを設定し **、IMessage::SubmitMessage** を呼び出してメッセージを保存して送信します。</span><span class="sxs-lookup"><span data-stu-id="4f231-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="4f231-124">詳細については [、「IMessage::SubmitMessage」を参照してください](imessage-submitmessage.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="4f231-125">**PR \_ DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、送信されたメッセージを削除するか **、PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティで識別されるフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="4f231-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="4f231-126">詳細については、「送信されたメッセージ [の処理」を参照してください](processing-a-sent-message.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="4f231-127">メッセージを送信する前にメッセージを相互に保存する場合は、メッセージの [IMAPIProp::SaveChanges メソッドを呼び出](imapiprop-savechanges.md) します。</span><span class="sxs-lookup"><span data-stu-id="4f231-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="4f231-128">詳細については、「メッセージの保存[」または「メッセージの](saving-a-message.md)[送信」を参照してください](sending-a-message.md)。</span><span class="sxs-lookup"><span data-stu-id="4f231-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="4f231-129">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="4f231-129">In this section</span></span>

- <span data-ttu-id="4f231-130">[受信者リストの作成](creating-a-recipient-list.md): 受信者リストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="4f231-131">[メッセージ件名の作成](creating-a-message-subject.md): メッセージのオプションの件名を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="4f231-132">[メッセージ テキストの作成](creating-message-text.md): メッセージ テキストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="4f231-133">[書式設定されたテキストにレンダリング情報を](adding-rendering-information-to-formatted-text.md)追加する : 書式設定されたテキスト内で添付ファイルをレンダリングする場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="4f231-134">[メッセージ添付ファイルの作成](creating-a-message-attachment.md): 添付ファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="4f231-135">[メッセージの保存](saving-a-message.md): クライアントがメッセージを保存する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="4f231-136">[メッセージの送信 :](sending-a-message.md)メッセージを送信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="4f231-137">[送信メッセージの処理](processing-a-sent-message.md): 送信メッセージを処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f231-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

