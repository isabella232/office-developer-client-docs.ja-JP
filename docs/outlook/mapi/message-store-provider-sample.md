---
title: メッセージ ストア プロバイダー サンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 25c606531aa9a7436306a1b87c32aab49fd975db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593915"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="bf896-103">メッセージ ストア プロバイダー サンプル</span><span class="sxs-lookup"><span data-stu-id="bf896-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="bf896-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf896-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf896-105">サンプル ラップ PST ストア プロバイダーは、データを格納するためのバックエンドとして、個人用フォルダー ファイル (PST) プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf896-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="bf896-106">レプリケーション API とは、ラップされた PST ストア プロバイダーを使用してください。</span><span class="sxs-lookup"><span data-stu-id="bf896-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="bf896-107">レプリケーション API を使用すると、バックエンド ・ データ ・ リポジトリからアイテムを Microsoft Outlook の PST ストアにレプリケートできます。</span><span class="sxs-lookup"><span data-stu-id="bf896-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="bf896-108">レプリケーション API を使用するには専用の PST ストアにデータをレプリケートし同期の状態の追跡します。</span><span class="sxs-lookup"><span data-stu-id="bf896-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="bf896-109">詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf896-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="bf896-110">サンプル ラップ PST ストア プロバイダーの機能のほとんどでは、基になる PST プロバイダーに直接、引数を渡します。</span><span class="sxs-lookup"><span data-stu-id="bf896-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="bf896-111">特定の機能は特別な実装を必要としては、次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="bf896-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf896-112">実行可能ファイル:</span><span class="sxs-lookup"><span data-stu-id="bf896-112">Executable:</span></span>  <br/> |<span data-ttu-id="bf896-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="bf896-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="bf896-114">ソース コードのディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="bf896-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="bf896-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="bf896-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="bf896-116">言語:</span><span class="sxs-lookup"><span data-stu-id="bf896-116">Language:</span></span>  <br/> |<span data-ttu-id="bf896-117">C++</span><span class="sxs-lookup"><span data-stu-id="bf896-117">C++</span></span>  <br/> |
|<span data-ttu-id="bf896-118">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="bf896-118">Platforms:</span></span>  <br/> |<span data-ttu-id="bf896-119">Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 のプログラムをコンパイルするのには、Microsoft Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="bf896-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="bf896-120">サポートされている機能</span><span class="sxs-lookup"><span data-stu-id="bf896-120">Supported Features</span></span>

<span data-ttu-id="bf896-121">このサンプルでは、Microsoft Outlook 2010 の 64年ビットをサポートし、Outlook 2013 が改訂されたようになりました。</span><span class="sxs-lookup"><span data-stu-id="bf896-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="bf896-122">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf896-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="bf896-123">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="bf896-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="bf896-124">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="bf896-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="bf896-125">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="bf896-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="bf896-126">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="bf896-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="bf896-127">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="bf896-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="bf896-128">**サンプル ラップ PST ストア プロバイダーをインストールするのには**</span><span class="sxs-lookup"><span data-stu-id="bf896-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="bf896-129">サンプル ラップ PST プロバイダーをダウンロードするには、 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf896-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="bf896-130">Outlook MAPI サンプルを保存したフォルダーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="bf896-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="bf896-131">右クリックし、 **OutlookMAPISamples ・\<バージョン番号\>** フォルダーを zip し、[**すべて展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf896-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="bf896-132">**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf896-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="bf896-133">Microsoft Visual Studio 2008 を実行します。</span><span class="sxs-lookup"><span data-stu-id="bf896-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="bf896-134">Microsoft Visual Studio 2008 では、[**ファイル**] をクリックして、[**開いている**、および**プロジェクト/ソリューション**] をクリックし。</span><span class="sxs-lookup"><span data-stu-id="bf896-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="bf896-135">サンプルを保存する場所を参照する**WrapPST.vcproj**をクリックし、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf896-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="bf896-136">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf896-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="bf896-137">**ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf896-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="bf896-138">サンプルを保存したフォルダーに**install.bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf896-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="bf896-139">**ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf896-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

