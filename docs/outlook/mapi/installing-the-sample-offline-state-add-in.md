---
title: サンプル オフライン状態アドインのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317214"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="24119-103">サンプル オフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="24119-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="24119-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24119-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24119-105">このトピックでは、サンプル オフライン状態アドインをダウンロードしてインストールする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="24119-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="24119-106">サンプル オフライン状態アドインは、オフライン状態メニューを追加し、オフライン状態API を使用Outlook COM アドインです。</span><span class="sxs-lookup"><span data-stu-id="24119-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="24119-107">[オフライン状態] メニューを使用すると、状態の監視を有効または無効にしたり、現在の状態を確認したり、現在の状態を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="24119-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="24119-108">オフライン状態アドインの実装方法の詳細については、「オフライン状態アドインのセットアップ」 [を参照してください](setting-up-an-offline-state-add-in.md)。</span><span class="sxs-lookup"><span data-stu-id="24119-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="24119-109">サンプル オフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="24119-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="24119-110">サンプル オフライン状態アドインは[、2007](https://www.microsoft.com/en-us/download/details.aspx?id=24102)Outlookリファレンス コード サンプルと再頒布可能インストーラーからダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="24119-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="24119-111">管理者Visual Studio 2005 を実行します。</span><span class="sxs-lookup"><span data-stu-id="24119-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="24119-112">XP でコンピューターがWindowsしている場合は、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="24119-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="24119-113">Vista でコンピューターがWindowsしている場合は、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="24119-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="24119-114">[2005 年 2005 年Visual Studio右クリックし、[管理者として **実行] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="24119-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="24119-115">[Visual Studio 2005 で、[ファイル] をクリックし、[開く]**を選択して\*\*\*\*、[Project/ソリューション] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="24119-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="24119-116">サンプルを保存した場所を参照し **、[ConnectionStateAddin]** をクリックし、[開く] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="24119-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="24119-117">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="24119-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="24119-118">[ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="24119-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="24119-119">[スタート]**メニューをクリック** し、[**すべての** プログラム] をクリックし、[アクセサリ] をクリックし、[コマンド プロンプト] を右クリックして、[管理者として実行]**をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="24119-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="24119-120">XP を実行しているWindows管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="24119-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="24119-121">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="24119-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="24119-122">[コマンド **プロンプト] ウィンドウ** で、ディレクトリをサンプルを保存した Debug フォルダーに変更します。</span><span class="sxs-lookup"><span data-stu-id="24119-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="24119-123">たとえば、サンプルを C:\ に保存した場合ドライブでは **、cd "C:\ConnectionStateAddin\Debug"** と入力し **、Enter** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="24119-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="24119-124">**regsvr32 と入力OfflineStateAddin.dll** Enter キーを **押します**。</span><span class="sxs-lookup"><span data-stu-id="24119-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="24119-125">サンプル オフライン状態アドインをアンインストールするには **、「regsvr32 -u」と入力OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="24119-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="24119-126">**[RegSrv32] ダイアログ** ボックスで **、[OK] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="24119-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="24119-127">[オフラインOutlookを再起動して、[**オフライン状態] メニューを表示** します。</span><span class="sxs-lookup"><span data-stu-id="24119-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="24119-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="24119-128">See also</span></span>



[<span data-ttu-id="24119-129">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="24119-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="24119-130">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="24119-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="24119-131">サンプルのオフライン状態アドインについて</span><span class="sxs-lookup"><span data-stu-id="24119-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="24119-132">オフライン状態アドインのセットアップ</span><span class="sxs-lookup"><span data-stu-id="24119-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="24119-133">オフライン状態アドインを使用した接続状態変更の監視</span><span class="sxs-lookup"><span data-stu-id="24119-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="24119-134">オフライン状態アドインの切断</span><span class="sxs-lookup"><span data-stu-id="24119-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

