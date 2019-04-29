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
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="76611-103">送信メッセージの処理</span><span class="sxs-lookup"><span data-stu-id="76611-103">Handling an outgoing message</span></span>

<span data-ttu-id="76611-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76611-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76611-105">送信メッセージは、1つまたは複数のメッセージングシステムで1人または複数の受信者に送信されるメッセージ、またはメッセージストア内のフォルダーに投稿されるメッセージです。</span><span class="sxs-lookup"><span data-stu-id="76611-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="76611-106">送信メッセージを作成および送信する</span><span class="sxs-lookup"><span data-stu-id="76611-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="76611-107">既定のメッセージストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="76611-107">Open the default message store.</span></span> <span data-ttu-id="76611-108">詳細については、「[メッセージストアを開く](opening-a-message-store.md)」および「[既定のメッセージストアを開く](opening-the-default-message-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="76611-109">[送信トレイ] フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="76611-109">Open the Outbox folder.</span></span> <span data-ttu-id="76611-110">詳細については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="76611-111">送信トレイフォルダーの**imapifolder:: CreateMessage**メソッドを呼び出して、新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="76611-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="76611-112">詳細については、「 [imapifolder:: CreateMessage](imapifolder-createmessage.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="76611-113">1つまたは複数の解決された受信者を含む受信者リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="76611-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="76611-114">詳細については、「[受信者リストを作成](creating-a-recipient-list.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="76611-115">必要に応じて、件名を追加します。</span><span class="sxs-lookup"><span data-stu-id="76611-115">Optionally, add a subject.</span></span> <span data-ttu-id="76611-116">詳細については、「[メッセージの件名の作成](creating-a-message-subject.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="76611-117">メッセージテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="76611-117">Add the message text.</span></span> <span data-ttu-id="76611-118">詳細については、「[メッセージテキストを作成する](creating-message-text.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="76611-119">メッセージテキストが書式設定されている場合は、レンダリング情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="76611-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="76611-120">詳細については、「[レンダリング情報を書式設定されたテキストに追加する](adding-rendering-information-to-formatted-text.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="76611-121">必要に応じて、1つまたは複数の添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="76611-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="76611-122">詳細については、「[メッセージの添付ファイルを作成](creating-a-message-attachment.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="76611-123">必要に応じて他のメッセージプロパティを設定し、 **IMessage:: submitmessage**を呼び出してメッセージを保存して送信します。</span><span class="sxs-lookup"><span data-stu-id="76611-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="76611-124">詳細については、「 [IMessage:: submitmessage](imessage-submitmessage.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="76611-125">**PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、送信されたメッセージを削除するか、または**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティで指定されたフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="76611-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="76611-126">詳細については、「[送信済みメッセージの処理](processing-a-sent-message.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="76611-127">メッセージを送信する前に intermittantly 保存する場合は、メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="76611-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="76611-128">詳細については、「[メッセージを保存する](saving-a-message.md)」または「[メッセージを送信](sending-a-message.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76611-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="76611-129">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="76611-129">In this section</span></span>

- <span data-ttu-id="76611-130">[受信者リストを作成](creating-a-recipient-list.md)する: 受信者リストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="76611-131">[メッセージの件名の作成](creating-a-message-subject.md): メッセージの任意の件名を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="76611-132">[メッセージテキストの作成](creating-message-text.md): メッセージテキストを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="76611-133">[書式設定されたテキストへのレンダリング情報の追加](adding-rendering-information-to-formatted-text.md): 書式付きテキストのどこで添付ファイルがレンダリングされるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="76611-134">[メッセージ添付ファイルの](creating-a-message-attachment.md)作成: 添付ファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="76611-135">[メッセージを保存](saving-a-message.md)する: クライアントがメッセージを保存する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="76611-136">[メッセージの送信](sending-a-message.md): メッセージを送信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="76611-137">[送信済みメッセージの処理](processing-a-sent-message.md): 送信メッセージを処理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="76611-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

