---
title: メッセージ ストア プロバイダーのサンプル
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
# <a name="message-store-provider-sample"></a><span data-ttu-id="aef58-103">メッセージ ストア プロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="aef58-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="aef58-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aef58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aef58-105">サンプル ラップされた PST ストア プロバイダーは、データを格納するためのバック エンドとして個人用フォルダー ファイル (PST) プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="aef58-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="aef58-106">ラップされた PST ストア プロバイダーは、レプリケーション API と共に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aef58-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="aef58-107">レプリケーション API を使用すると、アイテムをバック エンド データ リポジトリから Microsoft の PST ストアOutlookできます。</span><span class="sxs-lookup"><span data-stu-id="aef58-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="aef58-108">レプリケーション API を使用して、専用の PST ストアにデータをレプリケートし、同期状態を追跡します。</span><span class="sxs-lookup"><span data-stu-id="aef58-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="aef58-109">詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。</span><span class="sxs-lookup"><span data-stu-id="aef58-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="aef58-110">サンプル ラップされた PST ストア プロバイダーのほとんどの関数は、基になる PST プロバイダーに直接引数を渡します。</span><span class="sxs-lookup"><span data-stu-id="aef58-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="aef58-111">一部の関数では、特別な実装が必要であり、次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="aef58-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aef58-112">実行可能ファイル:</span><span class="sxs-lookup"><span data-stu-id="aef58-112">Executable:</span></span>  <br/> |<span data-ttu-id="aef58-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="aef58-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="aef58-114">ソース コード ディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="aef58-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="aef58-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="aef58-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="aef58-116">言語:</span><span class="sxs-lookup"><span data-stu-id="aef58-116">Language:</span></span>  <br/> |<span data-ttu-id="aef58-117">C++</span><span class="sxs-lookup"><span data-stu-id="aef58-117">C++</span></span>  <br/> |
|<span data-ttu-id="aef58-118">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="aef58-118">Platforms:</span></span>  <br/> |<span data-ttu-id="aef58-119">Microsoft Visual Studio Vista、Windows Windows Server 2008、Windows XP SP2、Windows Server 2003 SP1 用にコンパイルする 2008</span><span class="sxs-lookup"><span data-stu-id="aef58-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="aef58-120">サポートされている機能</span><span class="sxs-lookup"><span data-stu-id="aef58-120">Supported Features</span></span>

<span data-ttu-id="aef58-121">このサンプルでは 64 ビットMicrosoft Outlook 2010サポートされ、2013 年に向Outlookされました。</span><span class="sxs-lookup"><span data-stu-id="aef58-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="aef58-122">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aef58-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="aef58-123">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="aef58-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="aef58-124">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="aef58-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="aef58-125">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="aef58-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="aef58-126">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="aef58-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="aef58-127">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="aef58-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="aef58-128">**ラップされた PST ストア プロバイダーのサンプルをインストールするには**</span><span class="sxs-lookup"><span data-stu-id="aef58-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="aef58-129">サンプル ラップされた PST プロバイダーをダウンロードするには、「MAPI サンプル[のダウンロードOutlookを参照してください](downloading-the-outlook-mapi-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="aef58-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="aef58-130">MAPI サンプルに保存したフォルダー Outlook探します。</span><span class="sxs-lookup"><span data-stu-id="aef58-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="aef58-131">**OutlookMAPISamples- バージョン \< \>** 番号 zip フォルダーを右クリックし、[すべて抽出]**をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="aef58-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="aef58-132">[ **参照]** をクリックし、サンプルを保存する場所を選択し、[抽出] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="aef58-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="aef58-133">2008 Microsoft Visual Studioを実行します。</span><span class="sxs-lookup"><span data-stu-id="aef58-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="aef58-134">[Microsoft Visual Studio 2008] で、[ファイル] をクリックし、[開く]**を選択し\*\*\*\*、[Project/ソリューション] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="aef58-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="aef58-135">サンプルを保存した場所を参照し **、[WrapPST.vcproj]** をクリックし、[開く] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="aef58-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="aef58-136">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef58-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="aef58-137">[ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="aef58-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="aef58-138">サンプルを保存したフォルダーで、ファイルを右クリックし、[管理者としてinstall.bat]**をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="aef58-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="aef58-139">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aef58-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

