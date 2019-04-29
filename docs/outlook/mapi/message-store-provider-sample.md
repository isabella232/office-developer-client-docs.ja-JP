---
title: メッセージストアプロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436868"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="1e9c8-103">メッセージストアプロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="1e9c8-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="1e9c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e9c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e9c8-105">サンプルのラップされた PST ストアプロバイダーは、データを保存するためのバックエンドとして個人用フォルダーファイル (pst) プロバイダを使用します。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="1e9c8-106">ラップされた PST ストアプロバイダーは、レプリケーション API と一緒に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="1e9c8-107">レプリケーション API を使用すると、バックエンドデータリポジトリから Microsoft Outlook PST ストアにアイテムをレプリケートすることができます。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="1e9c8-108">レプリケーション API を使用して、データを専用の PST ストアにレプリケートし、同期状態を追跡します。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="1e9c8-109">詳細については、「[レプリケーション API につい](about-the-replication-api.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="1e9c8-110">サンプルのラップされた pst ストアプロバイダーの多くの関数は、引数を基になる pst プロバイダーに直接渡します。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="1e9c8-111">特定の機能には特別な実装が必要であり、以下のトピックで説明されています。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e9c8-112">実行可能</span><span class="sxs-lookup"><span data-stu-id="1e9c8-112">Executable:</span></span>  <br/> |<span data-ttu-id="1e9c8-113">WrpPST32</span><span class="sxs-lookup"><span data-stu-id="1e9c8-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="1e9c8-114">ソースコードディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="1e9c8-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="1e9c8-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="1e9c8-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="1e9c8-116">言語</span><span class="sxs-lookup"><span data-stu-id="1e9c8-116">Language:</span></span>  <br/> |<span data-ttu-id="1e9c8-117">+</span><span class="sxs-lookup"><span data-stu-id="1e9c8-117">C++</span></span>  <br/> |
|<span data-ttu-id="1e9c8-118">対象</span><span class="sxs-lookup"><span data-stu-id="1e9c8-118">Platforms:</span></span>  <br/> |<span data-ttu-id="1e9c8-119">windows Vista、windows server 2008、windows XP SP2、および windows server 2003 SP1 用にコンパイルする Microsoft Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="1e9c8-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="1e9c8-120">サポートされる機能</span><span class="sxs-lookup"><span data-stu-id="1e9c8-120">Supported Features</span></span>

<span data-ttu-id="1e9c8-121">このサンプルは、Microsoft outlook 2010 64 ビット版をサポートしており、outlook 2013 用に改訂されました。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="1e9c8-122">追加情報については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="1e9c8-123">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="1e9c8-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="1e9c8-124">ラップされた PST ストアプロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="1e9c8-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="1e9c8-125">ラップされた PST ストアプロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="1e9c8-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="1e9c8-126">ラップされた PST ストアプロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="1e9c8-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="1e9c8-127">ラップされた PST ストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="1e9c8-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="1e9c8-128">**サンプルのラップされた PST ストアプロバイダーをインストールするには**</span><span class="sxs-lookup"><span data-stu-id="1e9c8-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="1e9c8-129">サンプルのラップされた PST プロバイダーをダウンロードするには、「 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="1e9c8-130">Outlook MAPI サンプルを保存したフォルダーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="1e9c8-131">**OutlookMAPISamples-\<version\>番号**の zip フォルダーを右クリックし、[**すべて展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="1e9c8-132">[**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="1e9c8-133">Microsoft Visual Studio 2008 を実行します。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="1e9c8-134">Microsoft Visual Studio 2008 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="1e9c8-135">サンプルを保存した場所を参照し、[ **WrapPST**] をクリックして、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="1e9c8-136">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="1e9c8-137">[名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="1e9c8-138">サンプルを保存したフォルダーで、**インストールする .bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="1e9c8-139">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e9c8-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

