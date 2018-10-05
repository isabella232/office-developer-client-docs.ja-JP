---
title: ラップされた PST ストア プロバイダーのサンプルのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397766"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="b0b58-103">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="b0b58-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="b0b58-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0b58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0b58-105">このトピックでは、ダウンロードしてサンプル ラップ PST ストア プロバイダーをインストールする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0b58-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="b0b58-106">サンプル ラップ PST ストア プロバイダー、WrapPST は、レプリケーション API と連携して使用するものでは、ラップされた PST ストア プロバイダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="b0b58-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="b0b58-107">レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0b58-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="b0b58-108">サンプルのラップされた PST ストア プロバイダーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="b0b58-109">サンプル ラップ PST ストア プロバイダーをダウンロードするには、 [Outlook 2007 の補助リファレンス コード サンプルおよび再頒布可能なインストーラー](https://www.microsoft.com/en-us/download/details.aspx?id=24102)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0b58-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="b0b58-110">**SampleWrappedPSTStoreProvider**フォルダーを開き、[**すべてのファイルの抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="b0b58-111">[**参照**] をクリックして、サンプルを保存する場所を選択し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="b0b58-112">[**展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-112">Click **Extract**.</span></span> <span data-ttu-id="b0b58-113">選択したフォルダーが表示され、展開されたファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0b58-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="b0b58-114">管理者として Visual Studio 2005 を開きます。</span><span class="sxs-lookup"><span data-stu-id="b0b58-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b0b58-115">場合は、コンピューターが Windows XP を実行して、必要がありますログインするは、管理者として。</span><span class="sxs-lookup"><span data-stu-id="b0b58-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="b0b58-116">場合は、コンピューターが Windows Vista を実行して、する必要がありますに記録される管理者とする必要があります、Visual Studio 2005] アイコンを右クリックし、**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="b0b58-117">Visual Studio 2005 では、[**ファイル**] をクリックを選択し、**開く**] を選択し、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="b0b58-118">サンプルを保存する場所を参照する**WrapPST**をクリックし、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="b0b58-119">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="b0b58-120">**ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="b0b58-121">サンプルを保存したフォルダーに**Install.bat**ファイルを右クリックし、**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="b0b58-122">**ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b0b58-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0b58-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0b58-123">See also</span></span>



[<span data-ttu-id="b0b58-124">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="b0b58-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b0b58-125">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="b0b58-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b0b58-126">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="b0b58-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b0b58-127">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="b0b58-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b0b58-128">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="b0b58-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

