---
title: ラップされた PST ストアプロバイダーのサンプルについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: '最終更新日: 2012 年7月3日'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329765"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="5b0a7-103">ラップされた PST ストアプロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="5b0a7-103">About the Sample Wrapped PST Store Provider</span></span>

 
  
<span data-ttu-id="5b0a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b0a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
## <a name="overview-of-message-store-providers"></a><span data-ttu-id="5b0a7-105">メッセージストアプロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="5b0a7-105">Overview of Message Store Providers</span></span>

<span data-ttu-id="5b0a7-106">メッセージストアプロバイダーは、メッセージの保存と取得、およびクライアントアプリケーションのユーザーに対するその他の情報の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-106">Message store providers handle the storage and retrieval of messages and other information for the users of client applications.</span></span> <span data-ttu-id="5b0a7-107">メッセージ情報は、メッセージストアと呼ばれる階層システムを使用して編成されます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-107">The message information is organized by using a hierarchical system known as a message store.</span></span> <span data-ttu-id="5b0a7-108">メッセージストアは複数のレベルで実装されており、異なる種類のメッセージを保持するフォルダーと呼ばれるコンテナーがあります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-108">The message store is implemented in multiple levels, with containers called folders that hold messages of different types.</span></span> <span data-ttu-id="5b0a7-109">メッセージストア内のレベル数に制限はありません。フォルダーには多数のサブフォルダーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-109">There is no limit to the number of levels in a message store; folders can contain many subfolders.</span></span>
  
<span data-ttu-id="5b0a7-110">メッセージストアデータは、さまざまな方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-110">Message store data can be used in a variety of ways.</span></span> <span data-ttu-id="5b0a7-111">一般的な電子メールの使用に加えて、フォルダーは、公開ディスカッションのフォーラム、参照ドキュメントのリポジトリとして、または掲示板情報のコンテナーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-111">In addition to the typical email usage, folders can be used as a forum for public discussion, as a repository for reference documents, or as a container for bulletin board information.</span></span> <span data-ttu-id="5b0a7-112">1つのメッセージストアでは、さまざまな種類の情報を保持できます。一部は変更可能で、一部は保持できません。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-112">A single message store can hold many types of information, some modifiable and some not.</span></span> <span data-ttu-id="5b0a7-113">複数のクライアントで同じメッセージストアをインストールすることにより、データの共有が容易かつ高速になります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-113">Multiple clients can install the same message store, making it easy and fast to share data.</span></span>
  
<span data-ttu-id="5b0a7-114">メッセージストアフォルダーを使用すると、メッセージを並べ替えたり、フィルター処理したり、ユーザーインターフェイス (UI) の表示で表示をカスタマイズしたりできます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-114">Message store folders allow you to sort and filter messages and to customize the view in a user interface (UI) display.</span></span> <span data-ttu-id="5b0a7-115">フィルター処理されたメッセージへのリンクは、"検索結果フォルダー" と呼ばれる特別なフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-115">Links to filtered messages are held in special folders called search-results folders.</span></span> <span data-ttu-id="5b0a7-116">クライアントアプリケーションのユーザーがフィルター条件を入力すると、MAPI は制限として参照され、条件は1つまたは複数のフォルダーに格納されているメッセージに適用されます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-116">The user of a client application enters filtering criteria, which MAPI refers to as a restriction, and the criteria is applied to the messages stored in one or more folders.</span></span> <span data-ttu-id="5b0a7-117">たとえば、特定の件名を扱っているメッセージのみに対して、先週よりも新しい到着日が表示されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-117">For example, a user might want to view only those messages dealing with a particular subject with arrival dates that are more recent than last week.</span></span> <span data-ttu-id="5b0a7-118">条件に一致するメッセージへの参照が検索結果フォルダーに一覧表示され、実際のメッセージは通常のフォルダーに残ります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-118">References to the messages that match the criteria are listed in the search-results folder and the real messages remain in their regular folders.</span></span>
  
<span data-ttu-id="5b0a7-119">メッセージは、あるユーザーまたはアプリケーションから別のユーザーまたはアプリケーションに転送されるデータの単位です。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-119">Messages are the units of data transferred from one user or application to another user or application.</span></span> <span data-ttu-id="5b0a7-120">すべてのメッセージには、送信に使用されるメッセージテキストとメッセージエンベロープ情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-120">Every message contains some message text and message envelope information that is used for transmission.</span></span> <span data-ttu-id="5b0a7-121">一部のメッセージには、1つまたは複数の添付ファイルが含まれているか、ファイル、別のメッセージ、または OLE オブジェクトの形式でメッセージに関連付けられているメッセージを転送します。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-121">Some messages include one or more attachments, or additional data related to and transported with a message in the form of a file, another message, or an OLE object.</span></span>
  
## <a name="the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="5b0a7-122">ラップされた PST ストアプロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="5b0a7-122">The Sample Wrapped PST Store Provider</span></span>

<span data-ttu-id="5b0a7-123">レプリケーション API を使用すると、バックエンドデータリポジトリから Outlook PST ストアにアイテムをレプリケートすることができます。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-123">The Replication API allows you to replicate items from a back-end data repository into an Outlook PST store.</span></span> <span data-ttu-id="5b0a7-124">レプリケーション API を使用して、データを専用の PST ストアにレプリケートし、同期状態を追跡します。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-124">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="5b0a7-125">この方法では、ユーザー設定の MAPI ストアプロバイダーを導入する必要はありません。これは、書き込みと管理が複雑です。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-125">This approach does not require you to introduce a custom MAPI store provider, which is complex to write and maintain.</span></span> <span data-ttu-id="5b0a7-126">ただし、レプリケーション API と共に動作するには、PST ストアプロバイダーがラップされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-126">However, the PST store provider does need to be wrapped to work with the Replication API.</span></span>
  
<span data-ttu-id="5b0a7-127">サンプルのラップされた PST ストアプロバイダーは、データを保存するために、個人用フォルダーファイル (pst) プロバイダをバックエンドとして使用します。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-127">The Sample Wrapped PST Store Provider uses the Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="5b0a7-128">ラップされた PST ストアプロバイダーは、レプリケーション API と組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-128">The wrapped PST store provider should be used in conjunction with the Replication API.</span></span> <span data-ttu-id="5b0a7-129">詳細については、「[レプリケーション API につい](about-the-replication-api.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-129">For more information, see [About the Replication API](about-the-replication-api.md).</span></span> <span data-ttu-id="5b0a7-130">サンプルのラップされた pst ストアプロバイダーの多くの関数は、引数を基になる pst プロバイダーに直接渡します。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-130">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="5b0a7-131">特定の機能には特別な実装が必要であり、以下のトピックで説明されています。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-131">Certain functions require special implementation and are described in the following topics.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5b0a7-132">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="5b0a7-132">In this section</span></span>

- [<span data-ttu-id="5b0a7-133">ラップされた PST ストアプロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="5b0a7-133">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="5b0a7-134">サンプルのラップされた PST ストアプロバイダーをダウンロードしてインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-134">Explains how to download and install the Sample Wrapped PST Store Provider.</span></span>
    
- [<span data-ttu-id="5b0a7-135">ラップされた PST ストアプロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="5b0a7-135">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="5b0a7-136">ラップされた pst ストアプロバイダーを実装する最初の手順は、ラップされた pst ストアプロバイダーを初期化して構成することです。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-136">The first step in implementing a wrapped PST store provider is to initialize and configure the wrapped PST store provider.</span></span>
    
- [<span data-ttu-id="5b0a7-137">ラップされた PST ストアプロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="5b0a7-137">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="5b0a7-138">ラップされた pst ストアプロバイダーを初期化した後、mapi および mapi スプーラーがラップされた pst ストアプロバイダーにログオンできるように、関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-138">After a wrapped PST store provider is initialized, you must implement functions so that MAPI and the MAPI spooler can log on to the wrapped PST store provider.</span></span>
    
- [<span data-ttu-id="5b0a7-139">ラップされた PST ストアプロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="5b0a7-139">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="5b0a7-140">ラップされた pst ストアプロバイダーを使用するには、 **[imapisupport:: IUnknown](imapisupportiunknown.md)** インターフェイスをラップして、ラップされた pst ストアプロバイダーの一般的なタスクを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-140">To use a wrapped PST store provider you must wrap the **[IMAPISupport::IUnknown](imapisupportiunknown.md)** interface to implement common wrapped PST store provider tasks.</span></span> 
    
- [<span data-ttu-id="5b0a7-141">ラップされた PST ストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="5b0a7-141">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
- <span data-ttu-id="5b0a7-142">ラップされた pst ストアプロバイダーの使用が終了したら、ラップされた pst ストアプロバイダーを適切にシャットダウンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b0a7-142">After you finish using a wrapped PST store provider, you must properly shut down the wrapped PST store provider.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b0a7-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b0a7-143">See also</span></span>



[<span data-ttu-id="5b0a7-144">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="5b0a7-144">About the Replication API</span></span>](about-the-replication-api.md)
  
<span data-ttu-id="5b0a7-145">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="5b0a7-145">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

