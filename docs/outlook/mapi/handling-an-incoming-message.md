---
title: 受信メッセージを処理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5705af6c8efaf42ae27d1b39bb28d162971ebf9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800175"
---
# <a name="handling-an-incoming-message"></a><span data-ttu-id="d733b-103">受信メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="d733b-103">Handling an incoming message</span></span>

<span data-ttu-id="d733b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d733b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d733b-105">受信メッセージは、1 つまたは複数のメッセージング システム間で送信されたメッセージです。</span><span class="sxs-lookup"><span data-stu-id="d733b-105">An incoming message is a message that has been sent across one or more messaging systems.</span></span> <span data-ttu-id="d733b-106">送られた場合にのみ、または他の多くの受信者にします。</span><span class="sxs-lookup"><span data-stu-id="d733b-106">It may have been sent only to you or to many other recipients.</span></span> <span data-ttu-id="d733b-107">受信メッセージは、特定のクラスのメッセージを保持するために指定された受信フォルダーに配置されます。</span><span class="sxs-lookup"><span data-stu-id="d733b-107">Incoming messages are placed in a receive folder designated to hold messages of a particular class.</span></span> <span data-ttu-id="d733b-108">設定することができます、さまざまな処理または、すべてのクラスの 1 つのフォルダーを使用するメッセージ クラスごとにフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d733b-108">You can set up a different receive folder for each message class that you handle or use one folder for all of the classes.</span></span>
  
<span data-ttu-id="d733b-109">場合はメッセージ ・ ストアに新しいメールの通知を登録すると、受信フォルダー内にメッセージを配置するたびに通知されます。</span><span class="sxs-lookup"><span data-stu-id="d733b-109">If you have registered for new mail notifications with the message store, you will be notified whenever a message is placed in a receive folder.</span></span> <span data-ttu-id="d733b-110">新着メール通知を登録していない状態で開く必要があります、適切なフォルダーを手動で新着メッセージの到着を確認するには、定期的に受信します。</span><span class="sxs-lookup"><span data-stu-id="d733b-110">If you have not registered for new mail notifications, you must open the appropriate receive folder periodically to manually check for the arrival of new messages.</span></span>
  
<span data-ttu-id="d733b-111">クライアントは、次のように[IMsgStore::Advise](imsgstore-advise.md)にパラメーターを設定することで新着メール通知の登録します。</span><span class="sxs-lookup"><span data-stu-id="d733b-111">Clients register for new mail notifications by setting the parameters to [IMsgStore::Advise](imsgstore-advise.md) as follows:</span></span> 
  
- <span data-ttu-id="d733b-112">_CbEntryID_を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="d733b-112">Set  _cbEntryID_ to 0.</span></span> 
    
- <span data-ttu-id="d733b-113">_LpEntryID_を NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d733b-113">Set  _lpEntryID_ to NULL.</span></span> 
    
- <span data-ttu-id="d733b-114">_UlEventMask_を fnevNewMail に設定します。</span><span class="sxs-lookup"><span data-stu-id="d733b-114">Set  _ulEventMask_ to fnevNewMail.</span></span> 
    
<span data-ttu-id="d733b-115">**IMAPIAdviseSink::OnNotify**メソッドの呼び出し内の_lpNotifications_パラメーターが指す、 **NEWMAIL\_通知**のエントリのメッセージ クラスなど、着信メッセージについての情報を格納する構造体識別子では、その親フォルダーのエントリ id と、 **PR_MESSAGE_FLAGS**プロパティの内容です。</span><span class="sxs-lookup"><span data-stu-id="d733b-115">The  _lpNotifications_ parameter in the call to your **IMAPIAdviseSink::OnNotify** method points to a **NEWMAIL\_NOTIFICATION** structure that contains information about the incoming message, such as its message class, its entry identifier, the entry identifier of its parent folder, and the contents of its **PR_MESSAGE_FLAGS** property.</span></span> <span data-ttu-id="d733b-116">登録して、通知を処理する方法の詳細については、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)、 [NEWMAIL_NOTIFICATION](newmail_notification.md)、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))、および[通知の処理](handling-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-116">For more information about registering for and handling notifications, see [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), and [Handling Notifications](handling-notifications.md).</span></span> 
  
<span data-ttu-id="d733b-117">ユーザーに受信したメッセージを表示する前に、メッセージ クラスは、クライアントをサポートするクラスを決定します。</span><span class="sxs-lookup"><span data-stu-id="d733b-117">Before displaying an incoming message to a user, determine if its message class is a class that your client supports.</span></span> <span data-ttu-id="d733b-118">それ以外の場合は、メッセージを無視します。</span><span class="sxs-lookup"><span data-stu-id="d733b-118">If not, ignore the message.</span></span> <span data-ttu-id="d733b-119">クラスをサポートする場合は、開くし、メッセージのメッセージ クラスに適切なフォームを使用してメッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d733b-119">If the class is one that you support, you can open and display the message with a form that is appropriate for the message class of the message.</span></span> <span data-ttu-id="d733b-120">フォームの選択は、メッセージ クラスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="d733b-120">The choice of forms is based on message class.</span></span> <span data-ttu-id="d733b-121">IPM クラスに属しているメッセージは、MAPI によって実装されている既定のフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="d733b-121">Messages that belong to the IPM class use a default form implemented by MAPI.</span></span> <span data-ttu-id="d733b-122">クライアントが定義されているカスタムのクラスに属しているメッセージには、特別な形式のクライアント定義または MAPI の既定のフォームのいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d733b-122">Messages that belong to custom classes defined by clients can use either client-defined specialized forms or the MAPI default form.</span></span>
  
## <a name="open-and-display-an-incoming-message"></a><span data-ttu-id="d733b-123">開き、受信したメッセージを表示</span><span class="sxs-lookup"><span data-stu-id="d733b-123">Open and display an incoming message</span></span>
  
1. <span data-ttu-id="d733b-124">メッセージのメッセージ クラスに対応する受信フォルダーのエントリ id を取得し、フォルダーを開くには、 **IMsgStore::OpenEntry**にこのエントリの識別子を渡す**IMsgStore::GetReceiveFolder**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d733b-124">Call **IMsgStore::GetReceiveFolder** to retrieve the entry identifier of the receive folder for the message class of the message and pass this entry identifier to **IMsgStore::OpenEntry** to open the folder.</span></span> <span data-ttu-id="d733b-125">詳細については、 [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)、 [IMsgStore::OpenEntry](imsgstore-openentry.md)、および[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-125">For more information, see [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), and [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
2. <span data-ttu-id="d733b-126">コンテンツ テーブルを取得するために、受信フォルダーの**IMAPIContainer::GetContentsTable**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d733b-126">Call the receive folder's **IMAPIContainer::GetContentsTable** method to retrieve its contents table.</span></span> <span data-ttu-id="d733b-127">詳細については、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-127">For more information, see [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span> <span data-ttu-id="d733b-128">テーブル内のすべての行を取得するためにテーブルの**IMAPITable::QueryRows**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d733b-128">Call the table's **IMAPITable::QueryRows** method to retrieve all the rows in the table.</span></span> <span data-ttu-id="d733b-129">詳細については、 [IMAPITable::QueryRows](imapitable-queryrows.md)と[内容のテーブル](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-129">For more information see [IMAPITable::QueryRows](imapitable-queryrows.md) and [Contents Tables](contents-tables.md).</span></span> <span data-ttu-id="d733b-130">コンテンツ テーブルを表示する方法についての詳細については、[フォルダーの内容のテーブルを表示する](displaying-a-folder-contents-table.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-130">For more information about displaying a contents table, see [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span>
    
3. <span data-ttu-id="d733b-131">クライアントが対話型の場合は、テーブルからメッセージを選択し、そのメッセージを表示に使用する形式を決定するユーザーを許可します。</span><span class="sxs-lookup"><span data-stu-id="d733b-131">If your client is interactive, allow the user to select a message from the table and determine the form to be used to display that message.</span></span> <span data-ttu-id="d733b-132">クライアントは、MAPI またはユーザー設定のフォームで提供される既定のフォームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d733b-132">Clients can use the default form provided by MAPI or a custom form.</span></span> <span data-ttu-id="d733b-133">詳細については、 [MAPI フォームの処理](handling-mapi-forms.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-133">For more information, see [Handling MAPI Forms](handling-mapi-forms.md).</span></span>
    
4. <span data-ttu-id="d733b-134">メッセージを開くには、 **IMsgStore::OpenEntry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d733b-134">Call **IMsgStore::OpenEntry** to open the message.</span></span> <span data-ttu-id="d733b-135">詳細については、[メッセージを開く](opening-a-message.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-135">For more information, see [Opening a Message](opening-a-message.md).</span></span>
    
5. <span data-ttu-id="d733b-136">メッセージのテキストを処理します。</span><span class="sxs-lookup"><span data-stu-id="d733b-136">Process the message text.</span></span> <span data-ttu-id="d733b-137">詳細については、[開始メッセージのテキスト](opening-message-text.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-137">For more information, see [Opening Message Text](opening-message-text.md).</span></span>
    
6. <span data-ttu-id="d733b-138">各メッセージの添付ファイルをレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="d733b-138">Render each of the message attachments.</span></span> <span data-ttu-id="d733b-139">詳細については、[テキスト形式の添付ファイルを表示](rendering-an-attachment-in-plain-text.md)または[rtf 形式のテキストの添付ファイルのレンダリング](rendering-an-attachment-in-rtf-text.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-139">For more information, see [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md) or [Rendering an Attachment in RTF Text](rendering-an-attachment-in-rtf-text.md).</span></span>
    
7. <span data-ttu-id="d733b-140">必要な場合は、添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d733b-140">Open an attachment if desired.</span></span> <span data-ttu-id="d733b-141">詳細については、[添付ファイルを開く](opening-an-attachment.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d733b-141">For more information see [Opening an Attachment](opening-an-attachment.md).</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="d733b-142">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="d733b-142">In this section</span></span>

- <span data-ttu-id="d733b-143">[開始メッセージ テキスト](opening-message-text.md): メッセージのテキストを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d733b-143">[Opening Message Text](opening-message-text.md): Describes how to open the message text.</span></span>
    
- <span data-ttu-id="d733b-144">[テキスト形式の添付ファイルを表示](rendering-an-attachment-in-plain-text.md): テキスト形式の添付ファイルをレンダリングする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d733b-144">[Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md): Describes how to render an attachment in plain text.</span></span>
    
- <span data-ttu-id="d733b-145">[Rtf 形式のテキストの添付ファイルを表示](rendering-an-attachment-in-rtf-text.md): 書式設定されたテキストの添付ファイルをレンダリングする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d733b-145">[Rendering an Attachment in RTF Text](rendering-an-attachment-in-rtf-text.md): Describes how to render an attachment in formatted text.</span></span>
    
- <span data-ttu-id="d733b-146">[添付ファイルを開く](opening-an-attachment.md): 添付ファイルを開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d733b-146">[Opening an Attachment](opening-an-attachment.md): Describes how to open an attachment.</span></span>
    

