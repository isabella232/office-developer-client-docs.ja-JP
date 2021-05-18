---
title: ラップされた PST ストア プロバイダーのサンプルのインストール
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
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="93050-103">ラップされた PST ストア プロバイダーのサンプルのインストール</span><span class="sxs-lookup"><span data-stu-id="93050-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="93050-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93050-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93050-105">このトピックでは、サンプル ラップされた PST ストア プロバイダーをダウンロードしてインストールする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="93050-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="93050-106">サンプル ラップされた PST ストア プロバイダー WrapPST は、レプリケーション API と組み合わせて使用することを目的としたラップされた PST ストア プロバイダーを実装します。</span><span class="sxs-lookup"><span data-stu-id="93050-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="93050-107">レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。</span><span class="sxs-lookup"><span data-stu-id="93050-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="93050-108">ラップされた PST ストア プロバイダーのサンプルをインストールする</span><span class="sxs-lookup"><span data-stu-id="93050-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="93050-109">ラップされた PST ストア プロバイダーのサンプルをダウンロードするには[、「Outlook 2007](https://www.microsoft.com/en-us/download/details.aspx?id=24102)補助リファレンス コード サンプルと再頒布可能インストーラー」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93050-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="93050-110">**SampleWrappedPSTStoreProvider フォルダー** を開き、[すべてのファイルの抽出 **] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="93050-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="93050-111">[ **参照]** をクリックし、サンプルを保存する場所を選択し **、[OK] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="93050-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="93050-112">[**展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93050-112">Click **Extract**.</span></span> <span data-ttu-id="93050-113">選択したフォルダーが表示され、抽出されたファイルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="93050-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="93050-114">管理者Visual Studio 2005 を開きます。</span><span class="sxs-lookup"><span data-stu-id="93050-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="93050-115">XP でコンピューターがWindowsしている場合は、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="93050-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="93050-116">コンピューターが Windows Vista を実行している場合は、管理者としてログインし、Visual Studio 2005 アイコンを右クリックし、[管理者として実行] をクリックする必要 **があります**。</span><span class="sxs-lookup"><span data-stu-id="93050-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="93050-117">[Visual Studio 2005 で、[ファイル] をクリックし、[開く]**を選択して\*\*\*\*、[Project/ソリューション] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="93050-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="93050-118">サンプルを保存した場所を参照し **、[WrapPST]** をクリックし、[開く] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="93050-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="93050-119">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93050-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="93050-120">[ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="93050-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="93050-121">サンプルを保存したフォルダーで、ファイルを右クリックし、[管理者として **Install.batを\*\*\*\*クリックします**。</span><span class="sxs-lookup"><span data-stu-id="93050-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="93050-122">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93050-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93050-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="93050-123">See also</span></span>



[<span data-ttu-id="93050-124">ラップされた PST ストア プロバイダーのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="93050-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="93050-125">ラップされた PST ストア プロバイダーの初期化</span><span class="sxs-lookup"><span data-stu-id="93050-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="93050-126">ラップされた PST ストア プロバイダーへのログオン</span><span class="sxs-lookup"><span data-stu-id="93050-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="93050-127">ラップされた PST ストア プロバイダーの使用</span><span class="sxs-lookup"><span data-stu-id="93050-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="93050-128">ラップされた PST ストア プロバイダーのシャットダウン</span><span class="sxs-lookup"><span data-stu-id="93050-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

