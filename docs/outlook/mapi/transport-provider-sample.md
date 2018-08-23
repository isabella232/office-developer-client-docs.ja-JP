---
title: トランスポート プロバイダー サンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b3ae4170cab109ae96a51eae6e70c674895eeae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575785"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="2deb9-103">トランスポート プロバイダー サンプル</span><span class="sxs-lookup"><span data-stu-id="2deb9-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="2deb9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2deb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2deb9-105">このサンプルでは、メッセージを送受信するためのファイルとディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="2deb9-106">実装し、各送信メッセージにテキストの行を追加する非常に単純なプリプロセッサを登録します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="2deb9-107">サンプルでは、トランスポート ニュートラル カプセル化形式 (TNEF) とテキストの間でメッセージの内容を分割する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="2deb9-108">すべての (プロパティ シート、ウィザード、およびプログラムの構成) の構成オプションとメッセージ オプションもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2deb9-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="2deb9-109">リモート トランスポート インターフェイスにサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2deb9-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="2deb9-110">[Outlook メッセージング API (MAPI) のサンプル コード](http://go.microsoft.com/fwlink/?LinkId=129740)からは、このサンプルをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="2deb9-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2deb9-111">実行可能ファイル:</span><span class="sxs-lookup"><span data-stu-id="2deb9-111">Executable:</span></span>  <br/> |<span data-ttu-id="2deb9-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="2deb9-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="2deb9-113">ソース コードのディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="2deb9-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="2deb9-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="2deb9-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="2deb9-115">言語:</span><span class="sxs-lookup"><span data-stu-id="2deb9-115">Language:</span></span>  <br/> |<span data-ttu-id="2deb9-116">C++</span><span class="sxs-lookup"><span data-stu-id="2deb9-116">C++</span></span>  <br/> |
|<span data-ttu-id="2deb9-117">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="2deb9-117">Platforms:</span></span>  <br/> |<span data-ttu-id="2deb9-118">Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 のプログラムをコンパイルするのには、Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="2deb9-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="2deb9-119">サポートされている機能</span><span class="sxs-lookup"><span data-stu-id="2deb9-119">Supported Features</span></span>

<span data-ttu-id="2deb9-120">このサンプルには、次の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2deb9-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="2deb9-121">送信、受信、および新着メッセージのポーリングなどの基本的な機能です。</span><span class="sxs-lookup"><span data-stu-id="2deb9-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="2deb9-122">インタラクティブおよびプログラマティックな構成です。</span><span class="sxs-lookup"><span data-stu-id="2deb9-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="2deb9-123">**IMAPIStatus**インターフェイス、プロパティの設定を除く。</span><span class="sxs-lookup"><span data-stu-id="2deb9-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="2deb9-124">詳細についてを参照してください、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="2deb9-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="2deb9-125">スレッド セーフにします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-125">Thread safety.</span></span>
    
- <span data-ttu-id="2deb9-126">テキスト ファイルにイベント ログを記録します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-126">Event logging to a text file.</span></span> <span data-ttu-id="2deb9-127">ファイルは、自動的に指定したサイズに制限します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="2deb9-128">トランスポートのすべてのセッションでは、同じファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="2deb9-129">サポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="2deb9-129">Unsupported Features</span></span>

<span data-ttu-id="2deb9-130">このサンプルでは、受信メッセージの非同期の検出をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2deb9-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="2deb9-131">**サンプルのトランスポート プロバイダーをインストールするのには**</span><span class="sxs-lookup"><span data-stu-id="2deb9-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="2deb9-132">サンプルのトランスポート プロバイダーをダウンロードするには、 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2deb9-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="2deb9-133">Outlook MAPI サンプルを保存したフォルダーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="2deb9-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="2deb9-134">右クリックし、 **OutlookMAPISamples ・\<バージョン番号\>** フォルダーを zip し、[**すべて展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="2deb9-135">**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="2deb9-136">Visual Studio 2008年を実行します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="2deb9-137">Visual Studio 2008 では、[**ファイル**] をクリックして、[**開いている**、および**プロジェクト/ソリューション**] をクリックし。</span><span class="sxs-lookup"><span data-stu-id="2deb9-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="2deb9-138">サンプルを保存する場所を参照する**mrxp32.vcproj**をクリックし、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="2deb9-139">**[ビルド**] メニューで、[**構成マネージャー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="2deb9-140">**[構成マネージャー** ] ダイアログ ボックスで、 **mrxp32**行に移動して [**構成**] 列には、**リリース**を選択し、[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="2deb9-141">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="2deb9-142">**ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="2deb9-143">サンプルを保存したフォルダーにインストール バッチ ファイルを右クリックし、**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="2deb9-144">**ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2deb9-145">**install.bat**コピー .dll ファイルを既定の Microsoft Office のインストール フォルダー、C:\Program ファイル Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="2deb9-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="2deb9-146">別の場所に Office 製品をインストールした場合は、 **install.bat**を右クリックし、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="2deb9-147">ファイルがメモ帳で開きます。</span><span class="sxs-lookup"><span data-stu-id="2deb9-147">The file opens in Notepad.</span></span> <span data-ttu-id="2deb9-148">既定のインストール パスをお使いのコンピューターで使用されているインストール パスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2deb9-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="2deb9-149">**トランスポート プロバイダーは、outlook を設定するには**</span><span class="sxs-lookup"><span data-stu-id="2deb9-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="2deb9-150">[Outlook の [**ツール**] メニューには、**アカウントの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="2deb9-151">**アカウントの設定**] ダイアログ ボックスの [**電子メール**] タブで [**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="2deb9-152">**電子メール サービスの選択**の下では、[**その他**、 **MRXP サンプルのトランスポート**を選択し、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="2deb9-153">**MRXP トランスポートの構成**] ダイアログ ボックスで、**ユーザーの表示名**を入力します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="2deb9-154">**受信トレイ (UNC 共有) へのパス**の下には、フォルダーのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="2deb9-155">ローカル フォルダーへのパスもできます。</span><span class="sxs-lookup"><span data-stu-id="2deb9-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="2deb9-156">このパスが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2deb9-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="2deb9-157">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="2deb9-158">**電子メール アカウントの追加**] ダイアログ ボックスで [ **OK**を] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="2deb9-159">[**完了**] をクリックし、[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="2deb9-160">MRXP アカウントを使用するには、終了し、Outlook を再起動します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="2deb9-161">**Outlook でメッセージを送信するトランスポート プロバイダーのサンプルを使用するには**</span><span class="sxs-lookup"><span data-stu-id="2deb9-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="2deb9-162">[**ファイル**] メニューで、[**新規**作成] をクリックし、[**メール メッセージ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="2deb9-163">形式を使用して受信者の名前を入力 **] ボックス**に **[MRXP:\<アドレス\>]**。</span><span class="sxs-lookup"><span data-stu-id="2deb9-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="2deb9-164">アドレスは、UNC 共有または受信者の受信トレイにフォルダーのローカル パスです。</span><span class="sxs-lookup"><span data-stu-id="2deb9-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2deb9-165">コロンまたはアドレスには、円記号 () がある場合は、各コロンまたは円記号の前に円記号を挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2deb9-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="2deb9-166">たとえば、メールを送信するのには [MRXP:C:\Mail\myDir] を入力しなければなりません`[MRXP:C\:\\Mail\\myDir]`。</span><span class="sxs-lookup"><span data-stu-id="2deb9-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="2deb9-167">受信者のアドレスが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2deb9-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="2deb9-168">**アカウント**をクリックし、 **MRXP サンプルのトランスポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="2deb9-169">メッセージを入力し、[**送信**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-169">Type your message and click **Send**.</span></span> <span data-ttu-id="2deb9-170">MRXP トランスポート プロバイダーを使用してメッセージが送信されます。</span><span class="sxs-lookup"><span data-stu-id="2deb9-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="2deb9-171">**トランスポート プロバイダーのサンプルを使用して、Outlook でメッセージを受信するのには**</span><span class="sxs-lookup"><span data-stu-id="2deb9-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="2deb9-172">[**ファイル**] メニューで、[**新規**作成] をクリックし、[**メール メッセージ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="2deb9-173">メッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-173">Type your message.</span></span>
    
3. <span data-ttu-id="2deb9-174">**Microsoft Office ボタン**をクリックを**名前を付けて保存**、**名前を付けて**[受信トレイ] フォルダーがセットアップ中に指定するファイルを保存する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="2deb9-175">**名前を付けて**保存] ダイアログ ボックスで、UNC 共有またはローカル フォルダー、受信トレイとして設定するを参照します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="2deb9-176">**ファイルの種類**] ボックスで、 **Outlook のメッセージの形式**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="2deb9-177">ファイルの名前を入力し、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2deb9-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="2deb9-178">ファイルは、共有フォルダーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="2deb9-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="2deb9-179">MRXP トランスポート プロバイダーは、Outlook の受信トレイにメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="2deb9-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

