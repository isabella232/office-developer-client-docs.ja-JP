---
title: MAPI メッセージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 417c113f-bd98-4515-85d1-09db7fc3a227
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1146fa0441d0b55a7610368324489bd3a6bb24e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801400"
---
# <a name="mapi-messages"></a><span data-ttu-id="a0124-103">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="a0124-103">MAPI Messages</span></span>

  
  
<span data-ttu-id="a0124-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0124-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0124-105">メッセージは、MAPI スプーラーとメッセージング システムを使用してサービス プロバイダーを介して別の 1 つのクライアント アプリケーションから送信される MAPI オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a0124-105">Messages are MAPI objects that are transmitted from one client application to another through the MAPI spooler and service providers by way of a messaging system.</span></span> <span data-ttu-id="a0124-106">MAPI でのほぼすべてのコンポーネントは、メッセージで動作します。</span><span class="sxs-lookup"><span data-stu-id="a0124-106">Nearly every component in MAPI works with messages.</span></span> <span data-ttu-id="a0124-107">クライアントは、ユーザーを作成、保存、送信、およびさらにコピーし、別のフォルダーに移動するメッセージを削除を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0124-107">Clients let users create, save, send, and delete messages in addition to copy and move them from one folder to another.</span></span> <span data-ttu-id="a0124-108">メッセージ ストア プロバイダーは、メッセージの管理とメッセージを MAPI スプーラーを無効またはトランスポート プロバイダーに提供するために必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0124-108">Message store providers are responsible for message management and for delivering messages to the MAPI spooler or a transport provider.</span></span> <span data-ttu-id="a0124-109">MAPI スプーラーは、トランスポート プロバイダーは、メッセージング システムとの間のメッセージの受信と配信を処理し、受信者、メッセージのオプションのプロパティを設定し、適切なトランスポート プロバイダーでは、メッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="a0124-109">The MAPI spooler moves messages to an appropriate transport provider, whereas transport providers handle the delivery and receipt of messages to and from a messaging system and set recipient and message option properties.</span></span> <span data-ttu-id="a0124-110">アドレス帳プロバイダーない直接のメッセージを処理、メッセージの受信者を記述するプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a0124-110">Address book providers work indirectly with messages, supporting properties that describe message recipients.</span></span>
  
<span data-ttu-id="a0124-111">メッセージは、個人間メッセージ (IPM) のルート フォルダーに作成されたフォルダーでは通常、メッセージ ・ ストア全体でフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a0124-111">Messages are stored in folders throughout a message store, typically folders created in the interpersonal message (IPM) root folder.</span></span> <span data-ttu-id="a0124-112">メッセージは、標準の IPM の受信トレイ、送信済みアイテム、削除済みアイテム、および [送信トレイ] フォルダーと同じレベルまたは階層内の下位レベルに通常格納されます。</span><span class="sxs-lookup"><span data-stu-id="a0124-112">Messages are usually stored at the same level as the standard IPM Inbox, Sent Items, Deleted Items, and Outbox folders, or at lower levels in the hierarchy.</span></span> <span data-ttu-id="a0124-113">ただし、メッセージは IPM サブツリーの外も格納できます。</span><span class="sxs-lookup"><span data-stu-id="a0124-113">However, messages can also be stored outside the IPM subtree.</span></span>
  
<span data-ttu-id="a0124-114">標準の IPM サブツリー内に作成されたメッセージには、標準的な内容 (つまり、クライアント アプリケーションのユーザーに表示される内容) があります。</span><span class="sxs-lookup"><span data-stu-id="a0124-114">Messages created in the standard IPM subtree have standard contents (that is, contents that are visible to the user of a client application).</span></span> <span data-ttu-id="a0124-115">ノートとレポートは、標準的な内容のメッセージの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a0124-115">Notes and reports are examples of messages that have standard contents.</span></span> <span data-ttu-id="a0124-116">関連する内容、または標準的なクライアントで表示されていない内容のメッセージを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a0124-116">Messages can also be created with associated contents, or contents that are not visible in the typical client.</span></span> <span data-ttu-id="a0124-117">フォルダーが別の種類のメッセージを保持するために 2 つの内容が異なるテーブルをサポート: 標準の標準的なメッセージは、テーブルと関連付けられているメッセージの内容が関連付けられているテーブルの内容です。</span><span class="sxs-lookup"><span data-stu-id="a0124-117">Folders support two different contents tables to hold the different types of messages: a standard contents table for standard messages, and an associated contents table for associated messages.</span></span> <span data-ttu-id="a0124-118">MAPI が関連付けられているメッセージのコンテンツの標準を設定していないために、任意の情報が含まれてことができます。</span><span class="sxs-lookup"><span data-stu-id="a0124-118">Because MAPI does not set standards for the content of associated messages, they can contain arbitrary information.</span></span> 
  
<span data-ttu-id="a0124-119">メッセージは、追加のデータを持つことができます: ファイル、別のメッセージ、または OLE オブジェクトの形式で、それに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a0124-119">A message can have additional data — in the form of a file, another message, or an OLE object — associated with it.</span></span> <span data-ttu-id="a0124-120">添付ファイルを呼び出すと、この追加のデータには、メッセージ ・ テキストのメタファイルとしてのアイコンまたは、rtf 形式のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0124-120">This additional data, which is called an attachment, appears either as an icon or, for an RTF message, as a metafile in the message text.</span></span> <span data-ttu-id="a0124-121">メッセージには、0、1、または多くの添付ファイルを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="a0124-121">A message can have zero, one, or many attachments.</span></span> <span data-ttu-id="a0124-122">添付ファイルは、常にメッセージが送信されます。</span><span class="sxs-lookup"><span data-stu-id="a0124-122">Attachments are always transmitted with the message.</span></span>
  
<span data-ttu-id="a0124-123">送信されるメッセージには、1 つまたは複数の受信者 (特定のメッセージング システムに関連付けられているアドレス) があります。</span><span class="sxs-lookup"><span data-stu-id="a0124-123">A message that is transmitted has one or more recipients (addresses that are associated with a particular messaging system).</span></span> <span data-ttu-id="a0124-124">一部の受信者は、現在のプロファイル内のアドレス帳プロバイダーが所属するコンテナー内のエントリ他の受信者がメッセージを送信する場合のみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0124-124">Some recipients are entries in a container that belongs to an address book provider in the current profile; other recipients are created only to transmit the message.</span></span> <span data-ttu-id="a0124-125">関連付けられたメッセージ受信者や添付ファイルにアクセスする必要があります、ために、メッセージの受信者や添付ファイルがそのサブオブジェクトと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a0124-125">Because recipients and attachments must be accessed through the message with which they are associated, a message's recipients and attachments are known as its subobjects.</span></span> 
  
<span data-ttu-id="a0124-126">メッセージ ストア プロバイダーでは、メッセージ、添付ファイル、および受信者をサポート 3 つのインターフェイスのメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0124-126">Message store providers support messages, attachments, and recipients through methods in three interfaces:</span></span> 
  
|<span data-ttu-id="a0124-127">**インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="a0124-127">**Interface**</span></span>|<span data-ttu-id="a0124-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="a0124-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0124-129">IMessage</span><span class="sxs-lookup"><span data-stu-id="a0124-129">IMessage</span></span>](imessageimapiprop.md) <br/> |<span data-ttu-id="a0124-130">添付ファイルと受信者の管理、メッセージを送信、読み取りの状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0124-130">Manages attachments and recipients, sends messages, sets read status.</span></span>  <br/> |
|[<span data-ttu-id="a0124-131">IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="a0124-131">IMAPIFolder</span></span>](imapifolderimapicontainer.md) <br/> |<span data-ttu-id="a0124-132">作成とのメッセージとサブフォルダーを移動およびコピー メッセージの状態を管理します。</span><span class="sxs-lookup"><span data-stu-id="a0124-132">Creates, copies, and moves messages and subfolders and manages message status.</span></span>  <br/> |
|[<span data-ttu-id="a0124-133">IAttach</span><span class="sxs-lookup"><span data-stu-id="a0124-133">IAttach</span></span>](iattachimapiprop.md) <br/> |<span data-ttu-id="a0124-134">添付ファイルのプロパティを管理します。</span><span class="sxs-lookup"><span data-stu-id="a0124-134">Manages attachment properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0124-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0124-135">See also</span></span>



<span data-ttu-id="a0124-136">[MAPI �A�v���P�[�V�����̊J��](mapi-application-development.md)</span><span class="sxs-lookup"><span data-stu-id="a0124-136">[MAPI Application Development](mapi-application-development.md)</span></span>

