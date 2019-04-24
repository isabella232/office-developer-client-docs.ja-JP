---
title: MAPI メッセージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f1d1895cc6f9e65929781cb0e966873d2bce197c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345858"
---
# <a name="mapi-messages"></a><span data-ttu-id="74869-103">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="74869-103">MAPI Messages</span></span>

  
  
<span data-ttu-id="74869-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74869-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74869-105">メッセージは、メッセージングシステムによって mapi スプーラーおよびサービスプロバイダーを経由して、1つのクライアントアプリケーションから別のクライアントアプリケーションに転送される mapi オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="74869-105">Messages are MAPI objects that are transmitted from one client application to another through the MAPI spooler and service providers by way of a messaging system.</span></span> <span data-ttu-id="74869-106">MAPI のほとんどすべてのコンポーネントは、メッセージを使用して動作します。</span><span class="sxs-lookup"><span data-stu-id="74869-106">Nearly every component in MAPI works with messages.</span></span> <span data-ttu-id="74869-107">クライアントを使用すると、フォルダー間でメッセージをコピーして移動するだけでなく、メッセージの作成、保存、送信、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="74869-107">Clients let users create, save, send, and delete messages in addition to copy and move them from one folder to another.</span></span> <span data-ttu-id="74869-108">メッセージストアプロバイダーは、メッセージ管理を行い、MAPI スプーラーまたはトランスポートプロバイダーにメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="74869-108">Message store providers are responsible for message management and for delivering messages to the MAPI spooler or a transport provider.</span></span> <span data-ttu-id="74869-109">MAPI スプーラーはメッセージを適切なトランスポートプロバイダーに移動しますが、トランスポートプロバイダーはメッセージングシステムとの間のメッセージの送受信と、受信者およびメッセージのオプションプロパティの設定を処理します。</span><span class="sxs-lookup"><span data-stu-id="74869-109">The MAPI spooler moves messages to an appropriate transport provider, whereas transport providers handle the delivery and receipt of messages to and from a messaging system and set recipient and message option properties.</span></span> <span data-ttu-id="74869-110">アドレス帳プロバイダーは、メッセージを使用して間接的に機能し、メッセージの受信者を記述するプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="74869-110">Address book providers work indirectly with messages, supporting properties that describe message recipients.</span></span>
  
<span data-ttu-id="74869-111">メッセージは、メッセージストア内のフォルダーに格納されます。通常は、個人間メッセージ (IPM) ルートフォルダー内に作成されるフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="74869-111">Messages are stored in folders throughout a message store, typically folders created in the interpersonal message (IPM) root folder.</span></span> <span data-ttu-id="74869-112">通常、メッセージは、標準の IPM 受信トレイ、送信済みアイテム、削除済みアイテム、および送信トレイフォルダーと同じレベルで、または階層内の下位レベルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="74869-112">Messages are usually stored at the same level as the standard IPM Inbox, Sent Items, Deleted Items, and Outbox folders, or at lower levels in the hierarchy.</span></span> <span data-ttu-id="74869-113">ただし、メッセージを IPM サブツリーの外部に格納することもできます。</span><span class="sxs-lookup"><span data-stu-id="74869-113">However, messages can also be stored outside the IPM subtree.</span></span>
  
<span data-ttu-id="74869-114">標準の IPM サブツリーで作成されたメッセージは、標準コンテンツ (つまり、クライアントアプリケーションのユーザーに対して表示されるコンテンツ) を持ちます。</span><span class="sxs-lookup"><span data-stu-id="74869-114">Messages created in the standard IPM subtree have standard contents (that is, contents that are visible to the user of a client application).</span></span> <span data-ttu-id="74869-115">メモとレポートは、標準的な内容を持つメッセージの例です。</span><span class="sxs-lookup"><span data-stu-id="74869-115">Notes and reports are examples of messages that have standard contents.</span></span> <span data-ttu-id="74869-116">また、関連付けられたコンテンツでメッセージを作成したり、通常のクライアントでは表示されないコンテンツを作成したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="74869-116">Messages can also be created with associated contents, or contents that are not visible in the typical client.</span></span> <span data-ttu-id="74869-117">フォルダーは、さまざまな種類のメッセージを保持するために2つの異なる contents テーブルをサポートしています。標準メッセージの標準の内容テーブルと、関連付けられたメッセージに関連付けられた contents テーブルです。</span><span class="sxs-lookup"><span data-stu-id="74869-117">Folders support two different contents tables to hold the different types of messages: a standard contents table for standard messages, and an associated contents table for associated messages.</span></span> <span data-ttu-id="74869-118">MAPI では、関連付けられたメッセージの内容の標準が設定されていないため、任意の情報を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="74869-118">Because MAPI does not set standards for the content of associated messages, they can contain arbitrary information.</span></span> 
  
<span data-ttu-id="74869-119">メッセージには、ファイル、別のメッセージ、または OLE オブジェクトの形式で追加のデータが関連付けられている場合があります。</span><span class="sxs-lookup"><span data-stu-id="74869-119">A message can have additional data — in the form of a file, another message, or an OLE object — associated with it.</span></span> <span data-ttu-id="74869-120">添付ファイルと呼ばれるこの追加データは、メッセージテキストのメタファイルとして、アイコンまたは (RTF メッセージの場合) のいずれかとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="74869-120">This additional data, which is called an attachment, appears either as an icon or, for an RTF message, as a metafile in the message text.</span></span> <span data-ttu-id="74869-121">メッセージには、0、1、または多数の添付ファイルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="74869-121">A message can have zero, one, or many attachments.</span></span> <span data-ttu-id="74869-122">添付ファイルは常にメッセージと共に送信されます。</span><span class="sxs-lookup"><span data-stu-id="74869-122">Attachments are always transmitted with the message.</span></span>
  
<span data-ttu-id="74869-123">送信されるメッセージには、1人または複数の受信者 (特定のメッセージングシステムに関連付けられているアドレス) があります。</span><span class="sxs-lookup"><span data-stu-id="74869-123">A message that is transmitted has one or more recipients (addresses that are associated with a particular messaging system).</span></span> <span data-ttu-id="74869-124">一部の受信者は、現在のプロファイルのアドレス帳プロバイダーに属しているコンテナー内のエントリです。その他の受信者は、メッセージを送信するためにのみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="74869-124">Some recipients are entries in a container that belongs to an address book provider in the current profile; other recipients are created only to transmit the message.</span></span> <span data-ttu-id="74869-125">受信者および添付ファイルには、関連付けられたメッセージを通じてアクセスする必要があるため、メッセージの受信者と添付ファイルは、そのサブオブジェクトと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="74869-125">Because recipients and attachments must be accessed through the message with which they are associated, a message's recipients and attachments are known as its subobjects.</span></span> 
  
<span data-ttu-id="74869-126">メッセージストアプロバイダーは、次の3つのインターフェイスのメソッドを使用して、メッセージ、添付ファイル、および受信者をサポートします。</span><span class="sxs-lookup"><span data-stu-id="74869-126">Message store providers support messages, attachments, and recipients through methods in three interfaces:</span></span> 
  
|<span data-ttu-id="74869-127">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="74869-127">**Interface**</span></span>|<span data-ttu-id="74869-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="74869-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74869-129">IMessage</span><span class="sxs-lookup"><span data-stu-id="74869-129">IMessage</span></span>](imessageimapiprop.md) <br/> |<span data-ttu-id="74869-130">添付ファイルと受信者を管理し、メッセージを送信し、開封の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="74869-130">Manages attachments and recipients, sends messages, sets read status.</span></span>  <br/> |
|[<span data-ttu-id="74869-131">IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="74869-131">IMAPIFolder</span></span>](imapifolderimapicontainer.md) <br/> |<span data-ttu-id="74869-132">メッセージとサブフォルダーを作成、コピー、および移動し、メッセージの状態を管理します。</span><span class="sxs-lookup"><span data-stu-id="74869-132">Creates, copies, and moves messages and subfolders and manages message status.</span></span>  <br/> |
|[<span data-ttu-id="74869-133">iattach</span><span class="sxs-lookup"><span data-stu-id="74869-133">IAttach</span></span>](iattachimapiprop.md) <br/> |<span data-ttu-id="74869-134">添付ファイルのプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="74869-134">Manages attachment properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74869-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="74869-135">See also</span></span>



[<span data-ttu-id="74869-136">MAPI アプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="74869-136">MAPI Application Development</span></span>](mapi-application-development.md)

