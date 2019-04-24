---
title: サンプルのオフライン状態アドインのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: '最終更新日: 2012 年7月6日'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317214"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="28406-103">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="28406-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="28406-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28406-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28406-105">このトピックでは、サンプルのオフライン状態アドインをダウンロードしてインストールする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="28406-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="28406-106">サンプルのオフライン状態アドインは、オフライン状態のメニューを Outlook に追加し\*\*\*\* 、オフライン状態 API を利用する COM アドインです。</span><span class="sxs-lookup"><span data-stu-id="28406-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="28406-107">オフライン状態メニューを使用すると、状態監視を有効または無効にしたり、現在の状態を確認したり、現在の状態を変更したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="28406-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="28406-108">オフライン状態アドインの実装方法の詳細については、「[オフライン状態アドインの設定](setting-up-an-offline-state-add-in.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28406-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="28406-109">サンプルのオフライン状態アドインをインストールする</span><span class="sxs-lookup"><span data-stu-id="28406-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="28406-110">サンプルのオフライン状態アドインをここでダウンロードします。 [Outlook 2007 の補助リファレンスコードサンプルと再頒布可能なインストーラー](https://www.microsoft.com/en-us/download/details.aspx?id=24102)。</span><span class="sxs-lookup"><span data-stu-id="28406-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="28406-111">管理者として Visual Studio 2005 を実行します。</span><span class="sxs-lookup"><span data-stu-id="28406-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="28406-112">Windows XP を実行しているコンピューターでは、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28406-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="28406-113">Windows Vista を実行しているコンピューターでは、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28406-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="28406-114">[Visual Studio 2005] アイコンを右クリックし、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="28406-115">Visual Studio 2005 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="28406-116">サンプルを保存した場所を参照し、[ **connectionstateaddin**] をクリックして、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="28406-117">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="28406-118">[名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="28406-119">[**スタート**] メニューの [**すべてのプログラム**]、[**アクセサリ**] の順にクリックし、[**コマンドプロンプト**] を右クリックし、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="28406-120">Windows XP を実行している場合は、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28406-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="28406-121">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="28406-122">**コマンドプロンプト**ウィンドウで、サンプルを保存した Debug フォルダーにディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="28406-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="28406-123">たとえば、サンプルを C:\ に保存した場合は、ドライブの場合は、「 **cd "C:\ConnectionStateAddin\Debug"」** と入力し、 **enter**キーを押します。</span><span class="sxs-lookup"><span data-stu-id="28406-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="28406-124">「 **regsvr32 offlinestateaddin** 」と入力し、 **enter**キーを押します。</span><span class="sxs-lookup"><span data-stu-id="28406-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="28406-125">サンプルのオフライン状態アドインをアンインストールするには、「 **regsvr32-u offlinestateaddin** 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="28406-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="28406-126">[ **RegSrv32** ] ダイアログボックスで、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28406-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="28406-127">Outlook を再起動して、**オフライン状態**メニューを表示します。</span><span class="sxs-lookup"><span data-stu-id="28406-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="28406-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="28406-128">See also</span></span>



[<span data-ttu-id="28406-129">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="28406-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="28406-130">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="28406-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="28406-131">サンプルのオフライン状態アドインについて</span><span class="sxs-lookup"><span data-stu-id="28406-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="28406-132">オフライン状態アドインのセットアップ</span><span class="sxs-lookup"><span data-stu-id="28406-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="28406-133">オフライン状態アドインを使用した接続状態変更の監視</span><span class="sxs-lookup"><span data-stu-id="28406-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="28406-134">オフライン状態アドインの切断</span><span class="sxs-lookup"><span data-stu-id="28406-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

