---
title: ラップされた PST ストアプロバイダーのサンプルのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309633"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="d94d0-103">ラップされた PST ストアプロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="d94d0-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="d94d0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d94d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d94d0-105">このトピックでは、サンプルのラップされた PST ストアプロバイダーをダウンロードしてインストールするための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="d94d0-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="d94d0-106">このサンプルのラップされた pst ストアプロバイダー WrapPST は、レプリケーション API と共に使用することを目的とした、ラップされた pst ストアプロバイダーを実装しています。</span><span class="sxs-lookup"><span data-stu-id="d94d0-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="d94d0-107">レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d94d0-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="d94d0-108">サンプルのラップされた PST ストアプロバイダーをインストールする</span><span class="sxs-lookup"><span data-stu-id="d94d0-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="d94d0-109">サンプルのラップされた PST ストアプロバイダーをダウンロードするには、「 [Outlook 2007 の補助リファレンスコードサンプルと再配布可能なインストーラー](https://www.microsoft.com/en-us/download/details.aspx?id=24102)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d94d0-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="d94d0-110">**SampleWrappedPSTStoreProvider**フォルダーを開き、[**すべてのファイルを抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="d94d0-111">[**参照**] をクリックして、サンプルを保存する場所を選択し、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="d94d0-112">[**展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-112">Click **Extract**.</span></span> <span data-ttu-id="d94d0-113">選択したフォルダーが表示され、抽出したファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d94d0-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="d94d0-114">管理者として Visual Studio 2005 を開きます。</span><span class="sxs-lookup"><span data-stu-id="d94d0-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d94d0-115">Windows XP を実行しているコンピューターでは、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d94d0-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="d94d0-116">Windows Vista を実行しているコンピューターでは、管理者としてログインしている必要があり、Visual Studio 2005 アイコンを右クリックして [**管理者として実行**] をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d94d0-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="d94d0-117">Visual Studio 2005 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="d94d0-118">サンプルを保存した場所を参照し、[ **WrapPST**] をクリックして、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="d94d0-119">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="d94d0-120">[名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="d94d0-121">サンプルを保存したフォルダーで、**インストールする .bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="d94d0-122">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d94d0-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d94d0-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="d94d0-123">See also</span></span>



[<span data-ttu-id="d94d0-124">ラップされた PST ストアプロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="d94d0-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d94d0-125">ラップされた PST ストアプロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="d94d0-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d94d0-126">ラップされた PST ストアプロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="d94d0-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d94d0-127">ラップされた PST ストアプロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="d94d0-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="d94d0-128">ラップされた PST ストアプロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="d94d0-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

