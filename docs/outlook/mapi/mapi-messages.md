---
title: MAPI メッセージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f1d1895cc6f9e65929781cb0e966873d2bce197c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423378"
---
# <a name="mapi-messages"></a><span data-ttu-id="09497-103">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="09497-103">MAPI Messages</span></span>

  
  
<span data-ttu-id="09497-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09497-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09497-105">メッセージは、メッセージング システムを介して MAPI スプーラーとサービス プロバイダーを介して、あるクライアント アプリケーションから別のクライアント アプリケーションに送信される MAPI オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="09497-105">Messages are MAPI objects that are transmitted from one client application to another through the MAPI spooler and service providers by way of a messaging system.</span></span> <span data-ttu-id="09497-106">MAPI のほぼ全コンポーネントがメッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="09497-106">Nearly every component in MAPI works with messages.</span></span> <span data-ttu-id="09497-107">クライアントを使用すると、ユーザーはメッセージを作成、保存、送信、および削除できます。また、メッセージをコピーして別のフォルダーに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="09497-107">Clients let users create, save, send, and delete messages in addition to copy and move them from one folder to another.</span></span> <span data-ttu-id="09497-108">メッセージ ストア プロバイダーは、メッセージ管理と、MAPI スプーラーまたはトランスポート プロバイダーにメッセージを配信する責任があります。</span><span class="sxs-lookup"><span data-stu-id="09497-108">Message store providers are responsible for message management and for delivering messages to the MAPI spooler or a transport provider.</span></span> <span data-ttu-id="09497-109">MAPI スプーラーはメッセージを適切なトランスポート プロバイダーに移動しますが、トランスポート プロバイダーはメッセージング システムとの間でメッセージの配信と受信を処理し、受信者とメッセージ オプションのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="09497-109">The MAPI spooler moves messages to an appropriate transport provider, whereas transport providers handle the delivery and receipt of messages to and from a messaging system and set recipient and message option properties.</span></span> <span data-ttu-id="09497-110">アドレス帳プロバイダーは、メッセージを間接的に処理し、メッセージ受信者を表すプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="09497-110">Address book providers work indirectly with messages, supporting properties that describe message recipients.</span></span>
  
<span data-ttu-id="09497-111">メッセージは、メッセージ ストア全体のフォルダー (通常は、対人間メッセージ (IPM) ルート フォルダーに作成されたフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="09497-111">Messages are stored in folders throughout a message store, typically folders created in the interpersonal message (IPM) root folder.</span></span> <span data-ttu-id="09497-112">メッセージは通常、標準の IPM 受信トレイ、送信済みアイテム、削除済みアイテム、送信トレイ フォルダーと同じレベル、または階層内の下位レベルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="09497-112">Messages are usually stored at the same level as the standard IPM Inbox, Sent Items, Deleted Items, and Outbox folders, or at lower levels in the hierarchy.</span></span> <span data-ttu-id="09497-113">ただし、メッセージは IPM サブツリーの外部に保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="09497-113">However, messages can also be stored outside the IPM subtree.</span></span>
  
<span data-ttu-id="09497-114">標準 IPM サブツリーで作成されたメッセージには、標準コンテンツ (つまり、クライアント アプリケーションのユーザーに表示されるコンテンツ) があります。</span><span class="sxs-lookup"><span data-stu-id="09497-114">Messages created in the standard IPM subtree have standard contents (that is, contents that are visible to the user of a client application).</span></span> <span data-ttu-id="09497-115">メモとレポートは、標準コンテンツを含むメッセージの例です。</span><span class="sxs-lookup"><span data-stu-id="09497-115">Notes and reports are examples of messages that have standard contents.</span></span> <span data-ttu-id="09497-116">メッセージは、関連付けられたコンテンツ、または一般的なクライアントに表示されないコンテンツと一緒に作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="09497-116">Messages can also be created with associated contents, or contents that are not visible in the typical client.</span></span> <span data-ttu-id="09497-117">フォルダーでは、さまざまな種類のメッセージを保持する 2 つの異なるコンテンツ テーブルがサポートされています。標準メッセージの標準コンテンツ テーブルと、関連付けられたメッセージに関連付けられたコンテンツ テーブル。</span><span class="sxs-lookup"><span data-stu-id="09497-117">Folders support two different contents tables to hold the different types of messages: a standard contents table for standard messages, and an associated contents table for associated messages.</span></span> <span data-ttu-id="09497-118">MAPI は関連付けられたメッセージのコンテンツの標準を設定しないので、任意の情報を含めできます。</span><span class="sxs-lookup"><span data-stu-id="09497-118">Because MAPI does not set standards for the content of associated messages, they can contain arbitrary information.</span></span> 
  
<span data-ttu-id="09497-119">メッセージには、ファイル、別のメッセージ、または OLE オブジェクトの形式で、追加のデータを関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="09497-119">A message can have additional data — in the form of a file, another message, or an OLE object — associated with it.</span></span> <span data-ttu-id="09497-120">添付ファイルと呼ばれるこの追加データは、アイコンとして、または RTF メッセージの場合は、メッセージ テキスト内のメタファイルとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="09497-120">This additional data, which is called an attachment, appears either as an icon or, for an RTF message, as a metafile in the message text.</span></span> <span data-ttu-id="09497-121">メッセージには、0、1、または多数の添付ファイルを含めできます。</span><span class="sxs-lookup"><span data-stu-id="09497-121">A message can have zero, one, or many attachments.</span></span> <span data-ttu-id="09497-122">添付ファイルは常にメッセージと一緒に送信されます。</span><span class="sxs-lookup"><span data-stu-id="09497-122">Attachments are always transmitted with the message.</span></span>
  
<span data-ttu-id="09497-123">送信されるメッセージには、1 つ以上の受信者 (特定のメッセージング システムに関連付けられているアドレス) があります。</span><span class="sxs-lookup"><span data-stu-id="09497-123">A message that is transmitted has one or more recipients (addresses that are associated with a particular messaging system).</span></span> <span data-ttu-id="09497-124">一部の受信者は、現在のプロファイルのアドレス帳プロバイダーに属するコンテナー内のエントリです。他の受信者は、メッセージを送信するためにのみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="09497-124">Some recipients are entries in a container that belongs to an address book provider in the current profile; other recipients are created only to transmit the message.</span></span> <span data-ttu-id="09497-125">受信者と添付ファイルは、関連付けられているメッセージを介してアクセスする必要があります。そのため、メッセージの受信者と添付ファイルはサブオブジェクトと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="09497-125">Because recipients and attachments must be accessed through the message with which they are associated, a message's recipients and attachments are known as its subobjects.</span></span> 
  
<span data-ttu-id="09497-126">メッセージ ストア プロバイダーは、次の 3 つのインターフェイスのメソッドを使用して、メッセージ、添付ファイル、受信者をサポートします。</span><span class="sxs-lookup"><span data-stu-id="09497-126">Message store providers support messages, attachments, and recipients through methods in three interfaces:</span></span> 
  
|<span data-ttu-id="09497-127">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="09497-127">**Interface**</span></span>|<span data-ttu-id="09497-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="09497-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09497-129">IMessage</span><span class="sxs-lookup"><span data-stu-id="09497-129">IMessage</span></span>](imessageimapiprop.md) <br/> |<span data-ttu-id="09497-130">添付ファイルと受信者を管理し、メッセージを送信し、読み取り状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="09497-130">Manages attachments and recipients, sends messages, sets read status.</span></span>  <br/> |
|[<span data-ttu-id="09497-131">IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="09497-131">IMAPIFolder</span></span>](imapifolderimapicontainer.md) <br/> |<span data-ttu-id="09497-132">メッセージとサブフォルダーを作成、コピー、移動し、メッセージの状態を管理します。</span><span class="sxs-lookup"><span data-stu-id="09497-132">Creates, copies, and moves messages and subfolders and manages message status.</span></span>  <br/> |
|[<span data-ttu-id="09497-133">IAttach</span><span class="sxs-lookup"><span data-stu-id="09497-133">IAttach</span></span>](iattachimapiprop.md) <br/> |<span data-ttu-id="09497-134">添付ファイルのプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="09497-134">Manages attachment properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09497-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="09497-135">See also</span></span>



[<span data-ttu-id="09497-136">MAPI アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="09497-136">MAPI Application Development</span></span>](mapi-application-development.md)

