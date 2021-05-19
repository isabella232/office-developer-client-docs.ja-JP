---
title: トランスポート プロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356589"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="6e2f6-103">トランスポート プロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="6e2f6-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="6e2f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e2f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e2f6-105">このサンプルでは、ファイルとディレクトリを使用してメッセージの送受信を行います。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="6e2f6-106">各送信メッセージにテキスト行を追加する非常に単純なプリプロセッサを実装して登録します。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="6e2f6-107">サンプルは、トランスポート ニュートラル カプセル化形式 (TNEF) とテキスト間でメッセージ コンテンツを分割する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="6e2f6-108">また、すべての構成オプション (プロパティ シート、ウィザード、プログラムによる構成) とメッセージ オプションもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="6e2f6-109">リモート トランスポート インターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="6e2f6-110">このサンプルは、メッセージング[API (MAPI) Outlookサンプルからダウンロードできます](https://go.microsoft.com/fwlink/?LinkId=129740)。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e2f6-111">実行可能ファイル:</span><span class="sxs-lookup"><span data-stu-id="6e2f6-111">Executable:</span></span>  <br/> |<span data-ttu-id="6e2f6-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="6e2f6-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="6e2f6-113">ソース コード ディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="6e2f6-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="6e2f6-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="6e2f6-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="6e2f6-115">言語:</span><span class="sxs-lookup"><span data-stu-id="6e2f6-115">Language:</span></span>  <br/> |<span data-ttu-id="6e2f6-116">C++</span><span class="sxs-lookup"><span data-stu-id="6e2f6-116">C++</span></span>  <br/> |
|<span data-ttu-id="6e2f6-117">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="6e2f6-117">Platforms:</span></span>  <br/> |<span data-ttu-id="6e2f6-118">Visual Studio Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 用にコンパイルする 200 Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e2f6-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="6e2f6-119">サポートされている機能</span><span class="sxs-lookup"><span data-stu-id="6e2f6-119">Supported Features</span></span>

<span data-ttu-id="6e2f6-120">このサンプルでは、次の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="6e2f6-121">新しいメッセージの送信、受信、ポーリングなどの基本的な機能。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="6e2f6-122">対話型およびプログラムによる構成。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="6e2f6-123">**プロパティの設定を除く IMAPIStatus** インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="6e2f6-124">詳細については [、「IMAPIStatus : IMAPIProp インターフェイス」を参照](imapistatusimapiprop.md) してください。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="6e2f6-125">スレッドの安全性。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-125">Thread safety.</span></span>
    
- <span data-ttu-id="6e2f6-126">テキスト ファイルへのイベント ログ。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-126">Event logging to a text file.</span></span> <span data-ttu-id="6e2f6-127">ファイルは、指定したサイズに自動的に制限されます。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="6e2f6-128">すべてのトランスポート セッションで同じファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="6e2f6-129">サポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="6e2f6-129">Unsupported Features</span></span>

<span data-ttu-id="6e2f6-130">このサンプルでは、受信メッセージの非同期検出はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="6e2f6-131">**サンプル トランスポート プロバイダーをインストールするには**</span><span class="sxs-lookup"><span data-stu-id="6e2f6-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="6e2f6-132">サンプル トランスポート プロバイダーをダウンロードするには、「MAPI サンプル[のダウンロードOutlookを参照してください](downloading-the-outlook-mapi-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="6e2f6-133">MAPI サンプルに保存したフォルダー Outlook探します。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="6e2f6-134">**OutlookMAPISamples- バージョン \< \>** 番号 zip フォルダーを右クリックし、[すべて抽出]**をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="6e2f6-135">[ **参照] を** クリックし、サンプルを保存する場所を選択し、[抽出] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="6e2f6-136">2008 Visual Studioを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="6e2f6-137">[Visual Studio 2008 で、[ファイル] を **クリック** し、[開く]**を選択し**、[Project/**ソリューション] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="6e2f6-138">サンプルを保存した場所を参照し **、[mrxp32.vcproj]** をクリックし、[開く] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="6e2f6-139">[ビルド] **メニューの [** 構成マネージャー] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="6e2f6-140">[構成 **マネージャー]** ダイアログ ボックスで **、mrxp32** 行に移動し、[構成]列で [リリース] を選択し、[閉じる] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="6e2f6-141">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="6e2f6-142">[ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="6e2f6-143">サンプルを保存したフォルダーで、インストール バッチ ファイルを右クリックし、[管理者として実行] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="6e2f6-144">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6e2f6-145">**install.bat** を既定.dll Microsoft Officeインストール フォルダー C:\Program Files\Microsoft Office\Office12 にコピーします。\.</span><span class="sxs-lookup"><span data-stu-id="6e2f6-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="6e2f6-146">別の場所にOffice製品をインストールしている場合は、[編集] をinstall.bat **クリック\*\*\*\*します**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="6e2f6-147">ファイルが [ファイル] ウィンドウメモ帳。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-147">The file opens in Notepad.</span></span> <span data-ttu-id="6e2f6-148">既定のインストール パスを、コンピューターで使用されるインストール パスに置き換える。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="6e2f6-149">**トランスポート プロバイダーを設定するには、Outlook**</span><span class="sxs-lookup"><span data-stu-id="6e2f6-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="6e2f6-150">[アカウント]**ウィンドウの**[ツール] メニュー Outlook、[アカウント]**をクリック設定。**</span><span class="sxs-lookup"><span data-stu-id="6e2f6-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="6e2f6-151">[アカウント **の設定設定]** ダイアログ ボックスの [電子メール] タブ **で**、[新規] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="6e2f6-152">[メール **サービスの選択] で** [ **その** 他] をクリックし **、[MRXP サンプル トランスポート**] を選択し、[次へ] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="6e2f6-153">**[MRXP トランスポート構成] ダイアログ ボックス** に「ユーザー表示名 **」と入力します**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="6e2f6-154">[ **受信トレイへのパス (UNC 共有) でフォルダー** パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="6e2f6-155">これは、ローカル フォルダーへのパスにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6e2f6-156">このパスが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="6e2f6-157">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="6e2f6-158">[メール アカウント **の追加] ダイアログ ボックスで\*\*\*\*、[OK] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="6e2f6-159">[完了 **] をクリック** し、[閉じる] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="6e2f6-160">MRXP アカウントの使用を開始するには、サーバーを終了して再起動Outlook。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="6e2f6-161">**トランスポート プロバイダーサンプルを使用してメッセージを送信するには、次のOutlook**</span><span class="sxs-lookup"><span data-stu-id="6e2f6-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="6e2f6-162">[ファイル] **メニューの** [新規] を **クリック** し、[メール メッセージ] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="6e2f6-163">[宛先 **] ボックス** に、[MRXP: ADDRESS] という形式を使用して受信者 **の名前 \< を入力 \> します**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="6e2f6-164">アドレスは、受信者の受信トレイへの UNC 共有またはローカル フォルダー パスです。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6e2f6-165">アドレスにコロンまたは円記号がある場合は、各コロンまたは円記号の前に円記号を挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="6e2f6-166">たとえば、[MRXP:C:\Mail\myDir] にメールを送信するには、 を入力する必要があります  `[MRXP:C\:\\Mail\\myDir]` 。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="6e2f6-167">受信者のアドレスが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="6e2f6-168">[アカウント **] を** クリックし **、[MRXP サンプル トランスポート] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="6e2f6-169">メッセージを入力し、[送信] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-169">Type your message and click **Send**.</span></span> <span data-ttu-id="6e2f6-170">メッセージは MRXP トランスポート プロバイダーを使用して送信されます。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="6e2f6-171">**トランスポート プロバイダーのサンプルを使用してメッセージを受信するには、次のOutlook**</span><span class="sxs-lookup"><span data-stu-id="6e2f6-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="6e2f6-172">[ファイル] **メニューの** [新規] を **クリック** し、[メール メッセージ] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="6e2f6-173">メッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-173">Type your message.</span></span>
    
3. <span data-ttu-id="6e2f6-174">[名前を **Microsoft Office]** ボタンをクリックし、[名前を付けて保存] をクリックし、[名前を付けて保存] をクリックして、セットアップ時に指定した受信トレイ フォルダーにファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="6e2f6-175">[名前を **付けて保存** ] ダイアログ ボックスで、受信トレイとして設定した UNC 共有またはローカル フォルダーを参照します。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="6e2f6-176">[名前を **付けて保存] ボックス** の一覧で、[**メッセージOutlook] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="6e2f6-177">ファイルの名前を入力し、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="6e2f6-178">ファイルは共有フォルダーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="6e2f6-179">MRXP トランスポート プロバイダーは、受信トレイにメッセージを配信Outlook。</span><span class="sxs-lookup"><span data-stu-id="6e2f6-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

