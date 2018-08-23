---
title: 送信メッセージを処理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ab293ee3813d77c3a954e8364736a89bc2330feb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800171"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="18cd0-103">送信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-103">Handling an outgoing message</span></span>

<span data-ttu-id="18cd0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18cd0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18cd0-105">送信メッセージは、1 つまたは複数のメッセージング システム間で 1 つまたは複数の受信者に送信することができますか、メッセージ ・ ストア内のフォルダーに投稿するメッセージです。</span><span class="sxs-lookup"><span data-stu-id="18cd0-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="18cd0-106">作成し、送信メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="18cd0-107">既定のメッセージ ストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="18cd0-107">Open the default message store.</span></span> <span data-ttu-id="18cd0-108">詳細については、[メッセージ ストアを開く](opening-a-message-store.md)と、[既定のメッセージ ストアを開く](opening-the-default-message-store.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="18cd0-109">[送信トレイ] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="18cd0-109">Open the Outbox folder.</span></span> <span data-ttu-id="18cd0-110">詳細については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="18cd0-111">新しいメッセージを作成するのには、[送信トレイ] フォルダーの**IMAPIFolder::CreateMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="18cd0-112">詳細については、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="18cd0-113">解決された 1 つまたは複数の受信者と受信者のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="18cd0-114">詳細については、[受信者リストを作成する](creating-a-recipient-list.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="18cd0-115">必要に応じて、件名を追加します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-115">Optionally, add a subject.</span></span> <span data-ttu-id="18cd0-116">詳細については、[メッセージの件名を作成する](creating-a-message-subject.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="18cd0-117">メッセージ テキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-117">Add the message text.</span></span> <span data-ttu-id="18cd0-118">詳細については、[メッセージ テキストの作成](creating-message-text.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="18cd0-119">メッセージのテキストがフォーマットされている場合は、レンダリング情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="18cd0-120">詳細については、[テキストの書式設定にレンダリング情報の追加](adding-rendering-information-to-formatted-text.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="18cd0-121">必要に応じて、1 つまたは複数の添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="18cd0-122">詳細については、[メッセージの添付ファイルを作成する](creating-a-message-attachment.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="18cd0-123">必要に応じてその他のメッセージのプロパティを設定し、保存して**IMessage::SubmitMessage**を呼び出すことによって、メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="18cd0-124">詳細については、 [IMessage::SubmitMessage](imessage-submitmessage.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="18cd0-125">場合に送信されるメッセージを削除します**PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE または特定のフォルダーに移動する**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティで。</span><span class="sxs-lookup"><span data-stu-id="18cd0-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="18cd0-126">詳細については、[送信メッセージの処理](processing-a-sent-message.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cd0-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="18cd0-127">Intermittantly したい場合は、メッセージを送信する前に保存、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="18cd0-128">詳細についてを参照してください、[メッセージを保存](saving-a-message.md)または[メッセージを送信](sending-a-message.md)します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="18cd0-129">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="18cd0-129">In this section</span></span>

- <span data-ttu-id="18cd0-130">[受信者リストを作成する](creating-a-recipient-list.md): 受信者のリストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="18cd0-131">[メッセージの件名を作成する](creating-a-message-subject.md): メッセージの任意の件名を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="18cd0-132">[メッセージ テキストを作成する](creating-message-text.md): メッセージのテキストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="18cd0-133">[形式のテキストをレンダリング情報を追加する](adding-rendering-information-to-formatted-text.md): 書式設定されたテキストの添付ファイルが表示されるについて説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="18cd0-134">[メッセージの添付ファイルを作成する](creating-a-message-attachment.md): 添付ファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="18cd0-135">[メッセージを保存する](saving-a-message.md): クライアントがメッセージを保存する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="18cd0-136">[メッセージの送信](sending-a-message.md): メッセージを送信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="18cd0-137">[送信メッセージの処理](processing-a-sent-message.md): メッセージを処理することができますを送信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cd0-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

