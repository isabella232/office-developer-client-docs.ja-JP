---
title: ラップされた PST ストア プロバイダーのサンプルについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432724"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="16e6c-103">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="16e6c-103">About the Sample Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="16e6c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16e6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
## <a name="overview-of-message-store-providers"></a><span data-ttu-id="16e6c-105">メッセージ ストア プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="16e6c-105">Overview of Message Store Providers</span></span>

<span data-ttu-id="16e6c-106">メッセージ ストア プロバイダーは、クライアント アプリケーションのユーザーのメッセージなどの情報の保存と取得を処理します。</span><span class="sxs-lookup"><span data-stu-id="16e6c-106">Message store providers handle the storage and retrieval of messages and other information for the users of client applications.</span></span> <span data-ttu-id="16e6c-107">メッセージ情報は、メッセージ ストアと呼ばれる階層システムを使用して整理されます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-107">The message information is organized by using a hierarchical system known as a message store.</span></span> <span data-ttu-id="16e6c-108">メッセージ ストアは、さまざまな種類のメッセージを保持するフォルダーと呼ばれるコンテナーを使用して、複数のレベルで実装されます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-108">The message store is implemented in multiple levels, with containers called folders that hold messages of different types.</span></span> <span data-ttu-id="16e6c-109">メッセージ ストア内のレベルの数に制限はありません。フォルダーには、多数のサブフォルダーを含めできます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-109">There is no limit to the number of levels in a message store; folders can contain many subfolders.</span></span>
  
<span data-ttu-id="16e6c-110">メッセージ ストア のデータは、さまざまな方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-110">Message store data can be used in a variety of ways.</span></span> <span data-ttu-id="16e6c-111">フォルダーは、一般的な電子メールの使用法に加えて、パブリック ディスカッションのフォーラム、参照ドキュメントのリポジトリ、掲示板情報のコンテナーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-111">In addition to the typical email usage, folders can be used as a forum for public discussion, as a repository for reference documents, or as a container for bulletin board information.</span></span> <span data-ttu-id="16e6c-112">1 つのメッセージ ストアには、多くの種類の情報を保持できます。変更可能な情報や変更できない情報があります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-112">A single message store can hold many types of information, some modifiable and some not.</span></span> <span data-ttu-id="16e6c-113">複数のクライアントが同じメッセージ ストアをインストールし、データを簡単かつ迅速に共有できます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-113">Multiple clients can install the same message store, making it easy and fast to share data.</span></span>
  
<span data-ttu-id="16e6c-114">メッセージ ストア フォルダーを使用すると、メッセージの並べ替えとフィルター処理を行い、ユーザー インターフェイス (UI) 表示でビューをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-114">Message store folders allow you to sort and filter messages and to customize the view in a user interface (UI) display.</span></span> <span data-ttu-id="16e6c-115">フィルター処理されたメッセージへのリンクは、検索結果フォルダーと呼ばれる特別なフォルダーに保持されます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-115">Links to filtered messages are held in special folders called search-results folders.</span></span> <span data-ttu-id="16e6c-116">クライアント アプリケーションのユーザーは、MAPI が制限として参照するフィルター条件を入力し、1 つ以上のフォルダーに格納されているメッセージに条件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-116">The user of a client application enters filtering criteria, which MAPI refers to as a restriction, and the criteria is applied to the messages stored in one or more folders.</span></span> <span data-ttu-id="16e6c-117">たとえば、先週より新しい到着日を持つ特定の件名を扱うメッセージのみを表示する場合があります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-117">For example, a user might want to view only those messages dealing with a particular subject with arrival dates that are more recent than last week.</span></span> <span data-ttu-id="16e6c-118">条件に一致するメッセージへの参照は検索結果フォルダーに一覧表示され、実際のメッセージは通常のフォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-118">References to the messages that match the criteria are listed in the search-results folder and the real messages remain in their regular folders.</span></span>
  
<span data-ttu-id="16e6c-119">メッセージは、あるユーザーまたはアプリケーションから別のユーザーまたはアプリケーションに転送されるデータの単位です。</span><span class="sxs-lookup"><span data-stu-id="16e6c-119">Messages are the units of data transferred from one user or application to another user or application.</span></span> <span data-ttu-id="16e6c-120">すべてのメッセージには、送信に使用されるメッセージ テキストとメッセージ エンベロープ情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="16e6c-120">Every message contains some message text and message envelope information that is used for transmission.</span></span> <span data-ttu-id="16e6c-121">一部のメッセージには、1 つ以上の添付ファイル、またはファイル、別のメッセージ、または OLE オブジェクトの形式でメッセージに関連して転送される追加のデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-121">Some messages include one or more attachments, or additional data related to and transported with a message in the form of a file, another message, or an OLE object.</span></span>
  
## <a name="the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="16e6c-122">ラップされた PST ストア プロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="16e6c-122">The Sample Wrapped PST Store Provider</span></span>

<span data-ttu-id="16e6c-123">レプリケーション API を使用すると、バック エンド データ リポジトリから PST ストアにアイテムOutlookできます。</span><span class="sxs-lookup"><span data-stu-id="16e6c-123">The Replication API allows you to replicate items from a back-end data repository into an Outlook PST store.</span></span> <span data-ttu-id="16e6c-124">レプリケーション API を使用して、専用の PST ストアにデータをレプリケートし、同期状態を追跡します。</span><span class="sxs-lookup"><span data-stu-id="16e6c-124">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="16e6c-125">この方法では、カスタム MAPI ストア プロバイダーを導入する必要が生じ、書き込みと管理が複雑です。</span><span class="sxs-lookup"><span data-stu-id="16e6c-125">This approach does not require you to introduce a custom MAPI store provider, which is complex to write and maintain.</span></span> <span data-ttu-id="16e6c-126">ただし、レプリケーション API を操作するには、PST ストア プロバイダーをラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-126">However, the PST store provider does need to be wrapped to work with the Replication API.</span></span>
  
<span data-ttu-id="16e6c-127">サンプル ラップされた PST ストア プロバイダーは、データを格納するためのバック エンドとして個人用フォルダー ファイル (PST) プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="16e6c-127">The Sample Wrapped PST Store Provider uses the Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="16e6c-128">ラップされた PST ストア プロバイダーは、レプリケーション API と組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-128">The wrapped PST store provider should be used in conjunction with the Replication API.</span></span> <span data-ttu-id="16e6c-129">詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。</span><span class="sxs-lookup"><span data-stu-id="16e6c-129">For more information, see [About the Replication API](about-the-replication-api.md).</span></span> <span data-ttu-id="16e6c-130">サンプル ラップされた PST ストア プロバイダーのほとんどの関数は、基になる PST プロバイダーに直接引数を渡します。</span><span class="sxs-lookup"><span data-stu-id="16e6c-130">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="16e6c-131">一部の関数では、特別な実装が必要であり、次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="16e6c-131">Certain functions require special implementation and are described in the following topics.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="16e6c-132">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="16e6c-132">In this section</span></span>

- [<span data-ttu-id="16e6c-133">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="16e6c-133">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="16e6c-134">サンプル ラップ PST ストア プロバイダーをダウンロードしてインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16e6c-134">Explains how to download and install the Sample Wrapped PST Store Provider.</span></span>
    
- [<span data-ttu-id="16e6c-135">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="16e6c-135">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="16e6c-136">ラップされた PST ストア プロバイダーを実装する最初の手順は、ラップされた PST ストア プロバイダーを初期化して構成します。</span><span class="sxs-lookup"><span data-stu-id="16e6c-136">The first step in implementing a wrapped PST store provider is to initialize and configure the wrapped PST store provider.</span></span>
    
- [<span data-ttu-id="16e6c-137">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="16e6c-137">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="16e6c-138">ラップされた PST ストア プロバイダーを初期化した後、MAPI と MAPI スプーラーがラップされた PST ストア プロバイダーにログオンできるよう、関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-138">After a wrapped PST store provider is initialized, you must implement functions so that MAPI and the MAPI spooler can log on to the wrapped PST store provider.</span></span>
    
- [<span data-ttu-id="16e6c-139">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="16e6c-139">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="16e6c-140">ラップされた PST ストア プロバイダーを使用するには **[、IMAPISupport::IUnknown](imapisupportiunknown.md)** インターフェイスをラップして、一般的なラップされた PST ストア プロバイダー タスクを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-140">To use a wrapped PST store provider you must wrap the **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface to implement common wrapped PST store provider tasks.</span></span> 
    
- [<span data-ttu-id="16e6c-141">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="16e6c-141">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="16e6c-142">ラップされた PST ストア プロバイダーの使用が完了したら、ラップされた PST ストア プロバイダーを適切にシャットダウンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="16e6c-142">After you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16e6c-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="16e6c-143">See also</span></span>



[<span data-ttu-id="16e6c-144">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="16e6c-144">About the Replication API</span></span>](about-the-replication-api.md)
  
<span data-ttu-id="16e6c-145">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="16e6c-145">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

