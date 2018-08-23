---
title: ラップされた PST ストア プロバイダーのサンプルについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: 399c86d189cfc4160d151f417a6dd20364e60ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563829"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="d9e8f-103">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="d9e8f-103">About the Sample Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="d9e8f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9e8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
## <a name="overview-of-message-store-providers"></a><span data-ttu-id="d9e8f-105">メッセージ ストア プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="d9e8f-105">Overview of Message Store Providers</span></span>

<span data-ttu-id="d9e8f-106">メッセージ ストア プロバイダーは、ストレージとのメッセージとその他の情報は、クライアント アプリケーションのユーザーの取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-106">Message store providers handle the storage and retrieval of messages and other information for the users of client applications.</span></span> <span data-ttu-id="d9e8f-107">メッセージの情報は、メッセージ ・ ストアと呼ばれる階層的なシステムを使用して編成されます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-107">The message information is organized by using a hierarchical system known as a message store.</span></span> <span data-ttu-id="d9e8f-108">メッセージ ・ ストアは、さまざまな種類のメッセージを保持するフォルダーと呼ばれるコンテナーに複数のレベルで実装されます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-108">The message store is implemented in multiple levels, with containers called folders that hold messages of different types.</span></span> <span data-ttu-id="d9e8f-109">メッセージ ・ ストア内のレベルの数に制限はありません。フォルダーには、多くのサブフォルダーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-109">There is no limit to the number of levels in a message store; folders can contain many subfolders.</span></span>
  
<span data-ttu-id="d9e8f-110">メッセージ ストアのデータは、さまざまな方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-110">Message store data can be used in a variety of ways.</span></span> <span data-ttu-id="d9e8f-111">一般的な電子メールの使用状況だけでなくフォルダーはパブリック ディスカッション フォーラムとして、参照ドキュメントのリポジトリとして、または掲示板の情報のコンテナーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-111">In addition to the typical email usage, folders can be used as a forum for public discussion, as a repository for reference documents, or as a container for bulletin board information.</span></span> <span data-ttu-id="d9e8f-112">さまざまな種類については、いくつか変更可能なのと更新されていない、1 つのメッセージ ストアを保持できます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-112">A single message store can hold many types of information, some modifiable and some not.</span></span> <span data-ttu-id="d9e8f-113">複数のクライアントは、簡単なデータを共有することが、同じメッセージ ・ ストアをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-113">Multiple clients can install the same message store, making it easy and fast to share data.</span></span>
  
<span data-ttu-id="d9e8f-114">メッセージ ストアのフォルダーでは、並べ替えおよびフィルター処理するメッセージと、ユーザー インターフェイス (UI) の表示のビューをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-114">Message store folders allow you to sort and filter messages and to customize the view in a user interface (UI) display.</span></span> <span data-ttu-id="d9e8f-115">フィルター処理されたメッセージへのリンクは、検索結果のフォルダー] という名前の特別なフォルダーに保持されます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-115">Links to filtered messages are held in special folders called search-results folders.</span></span> <span data-ttu-id="d9e8f-116">クライアント アプリケーションのユーザーは、MAPI 制限と呼びますし、条件を 1 つまたは複数のフォルダーに格納されているメッセージに適用したフィルターの条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-116">The user of a client application enters filtering criteria, which MAPI refers to as a restriction, and the criteria is applied to the messages stored in one or more folders.</span></span> <span data-ttu-id="d9e8f-117">などは最後の週より新しい到着日のある特定の主題を扱うメッセージのみを表示する場合ことがあります。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-117">For example, a user might want to view only those messages dealing with a particular subject with arrival dates that are more recent than last week.</span></span> <span data-ttu-id="d9e8f-118">条件に一致するメッセージへの参照が検索結果のフォルダーに表示されているし、実際のメッセージは、通常のフォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-118">References to the messages that match the criteria are listed in the search-results folder and the real messages remain in their regular folders.</span></span>
  
<span data-ttu-id="d9e8f-119">メッセージは、1 つのユーザーまたは別のユーザーまたはアプリケーションにアプリケーションから転送されるデータの単位です。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-119">Messages are the units of data transferred from one user or application to another user or application.</span></span> <span data-ttu-id="d9e8f-120">すべてのメッセージには、いくつかのメッセージ テキストおよび伝送のために使用されるメッセージのエンベロープ情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-120">Every message contains some message text and message envelope information that is used for transmission.</span></span> <span data-ttu-id="d9e8f-121">いくつかのメッセージは、1 つまたは複数の添付ファイル、またはその他のデータとファイル、別のメッセージ、または OLE オブジェクトの形式でメッセージの転送に関連します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-121">Some messages include one or more attachments, or additional data related to and transported with a message in the form of a file, another message, or an OLE object.</span></span>
  
## <a name="the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="d9e8f-122">ラップされた PST ストア プロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="d9e8f-122">The Sample Wrapped PST Store Provider</span></span>

<span data-ttu-id="d9e8f-123">レプリケーション API を使用すると、バックエンド ・ データ ・ リポジトリからアイテムを Outlook の PST ストアにレプリケートできます。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-123">The Replication API allows you to replicate items from a back-end data repository into an Outlook PST store.</span></span> <span data-ttu-id="d9e8f-124">レプリケーション API を使用するには専用の PST ストアにデータをレプリケートし同期の状態の追跡します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-124">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="d9e8f-125">このアプローチでは、作成および保守する複雑なカスタム MAPI ストア プロバイダーを導入する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-125">This approach does not require you to introduce a custom MAPI store provider, which is complex to write and maintain.</span></span> <span data-ttu-id="d9e8f-126">ただし、PST ストア プロバイダーは、レプリケーション API を使用して作業をラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-126">However, the PST store provider does need to be wrapped to work with the Replication API.</span></span>
  
<span data-ttu-id="d9e8f-127">サンプル ラップ PST ストア プロバイダーは、データを格納するためのバックエンドとして、個人用フォルダー ファイル (PST) プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-127">The Sample Wrapped PST Store Provider uses the Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="d9e8f-128">ラップされた PST ストア プロバイダーは、レプリケーション API と連携して使用してください。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-128">The wrapped PST store provider should be used in conjunction with the Replication API.</span></span> <span data-ttu-id="d9e8f-129">詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-129">For more information, see [About the Replication API](about-the-replication-api.md).</span></span> <span data-ttu-id="d9e8f-130">サンプル ラップ PST ストア プロバイダーの機能のほとんどでは、基になる PST プロバイダーに直接、引数を渡します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-130">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="d9e8f-131">特定の機能は特別な実装を必要としては、次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-131">Certain functions require special implementation and are described in the following topics.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="d9e8f-132">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="d9e8f-132">In this section</span></span>

- [<span data-ttu-id="d9e8f-133">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="d9e8f-133">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="d9e8f-134">ダウンロードしてサンプル ラップ PST ストア プロバイダーをインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-134">Explains how to download and install the Sample Wrapped PST Store Provider.</span></span>
    
- [<span data-ttu-id="d9e8f-135">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="d9e8f-135">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="d9e8f-136">ラップされた PST ストア プロバイダーの実装では、まず初期化し、ラップされた PST ストア プロバイダーを構成します。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-136">The first step in implementing a wrapped PST store provider is to initialize and configure the wrapped PST store provider.</span></span>
    
- [<span data-ttu-id="d9e8f-137">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="d9e8f-137">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="d9e8f-138">ラップされた PST ストア プロバイダーを初期化すると後、は、できるように、MAPI スプーラーと MAPI にログオンできるラップの PST ストア プロバイダー関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-138">After a wrapped PST store provider is initialized, you must implement functions so that MAPI and the MAPI spooler can log on to the wrapped PST store provider.</span></span>
    
- [<span data-ttu-id="d9e8f-139">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="d9e8f-139">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="d9e8f-140">ラップされた PST ストアを使用するには、プロバイダーの一般的な実装するために**[IMAPISupport::IUnknown](imapisupportiunknown.md)** インターフェイスをラップする必要があります PST ストア プロバイダーのタスクをラップします。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-140">To use a wrapped PST store provider you must wrap the **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface to implement common wrapped PST store provider tasks.</span></span> 
    
- [<span data-ttu-id="d9e8f-141">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="d9e8f-141">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="d9e8f-142">ラップされた PST ストア プロバイダーを使用してが完了したら後、は、ラップされた PST ストア プロバイダーをシャット ダウンする必要があります正しく。</span><span class="sxs-lookup"><span data-stu-id="d9e8f-142">After you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9e8f-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9e8f-143">See also</span></span>



[<span data-ttu-id="d9e8f-144">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="d9e8f-144">About the Replication API</span></span>](about-the-replication-api.md)
  
<span data-ttu-id="d9e8f-145">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="d9e8f-145">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

