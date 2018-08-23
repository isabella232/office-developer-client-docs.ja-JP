---
title: サンプルのオフライン状態アドインのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: 00232f290c367c4bab1854bfe3909abc7b03cef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801092"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="33260-103">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="33260-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="33260-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33260-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33260-105">このトピックでは、ダウンロードしてオフライン状態のサンプル アドインをインストールする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="33260-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="33260-106">オフライン状態のサンプル アドインは、COM アドインを Outlook に、**オフライン状態**のメニューを追加し、オフライン状態 API を利用してします。</span><span class="sxs-lookup"><span data-stu-id="33260-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="33260-107">[オフラインの状態] メニューを有効にするまたは状態の監視を無効にする現在の状態を確認して現在の状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="33260-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="33260-108">オフライン状態のアドインを実装する方法の詳細については、[アドインの設定をオフラインの状態](setting-up-an-offline-state-add-in.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33260-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="33260-109">サンプル オフライン状態アドインのインストールします。</span><span class="sxs-lookup"><span data-stu-id="33260-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="33260-110">オフライン状態のサンプル アドインは、ここをダウンロード: [Outlook 2007 補助リファレンス コード サンプルおよび再頒布可能なインストーラー](http://www.microsoft.com/en-us/download/details.aspx?id=24102)です。</span><span class="sxs-lookup"><span data-stu-id="33260-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="33260-111">管理者として Visual Studio 2005 を実行します。</span><span class="sxs-lookup"><span data-stu-id="33260-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="33260-112">場合は、コンピューターが Windows XP を実行して、必要がありますログインするは、管理者として。</span><span class="sxs-lookup"><span data-stu-id="33260-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="33260-113">場合は、コンピューターが Windows Vista を実行して、必要がありますログインするは、管理者として。</span><span class="sxs-lookup"><span data-stu-id="33260-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="33260-114">Visual Studio 2005] アイコンを右クリックし、**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="33260-115">Visual Studio 2005 では、[**ファイル**] をクリックを選択し、**開く**] を選択し、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="33260-116">サンプルを保存する場所を参照する**ConnectionStateAddin**をクリックし、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="33260-117">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="33260-118">**ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="33260-119">**[スタート**] メニューをクリックして**すべてのプログラム**、[**アクセサリ**] をクリックして、**コマンド プロンプト**を右クリックし、**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="33260-120">Windows XP を実行している場合必要がありますログインするは、管理者として。</span><span class="sxs-lookup"><span data-stu-id="33260-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="33260-121">**ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="33260-122">**コマンド プロンプト**] ウィンドウでは、サンプルを保存するデバッグ フォルダーにディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="33260-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="33260-123">たとえば、C:\ ドライブのサンプルを保存する場合は、 **cd"C:\ConnectionStateAddin\Debug"** を入力し、し、 **ENTER**キーを押します。</span><span class="sxs-lookup"><span data-stu-id="33260-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="33260-124">**Regsvr32 OfflineStateAddin.dll**を入力し、 **ENTER**キーを押します。</span><span class="sxs-lookup"><span data-stu-id="33260-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="33260-125">オフライン状態のサンプル アドインをアンインストールするに **-u regsvr32 OfflineStateAddin.dll**と入力します</span><span class="sxs-lookup"><span data-stu-id="33260-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="33260-126">**RegSrv32** ] ダイアログ ボックスで [ **OK**を] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="33260-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="33260-127">Outlook を再起動して、[**オフライン状態**] メニューを参照してください。</span><span class="sxs-lookup"><span data-stu-id="33260-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="33260-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="33260-128">See also</span></span>



[<span data-ttu-id="33260-129">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="33260-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="33260-130">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="33260-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="33260-131">サンプルのオフライン状態アドインについて</span><span class="sxs-lookup"><span data-stu-id="33260-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="33260-132">オフライン状態アドインの設定</span><span class="sxs-lookup"><span data-stu-id="33260-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="33260-133">オフライン状態アドインを使用した接続状態変更のモニター</span><span class="sxs-lookup"><span data-stu-id="33260-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="33260-134">オフライン状態アドインの切断</span><span class="sxs-lookup"><span data-stu-id="33260-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

