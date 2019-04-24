---
title: トランスポートプロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356589"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="a879b-103">トランスポートプロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="a879b-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="a879b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a879b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a879b-105">この例では、ファイルとディレクトリを使用して、メッセージの送受信を行います。</span><span class="sxs-lookup"><span data-stu-id="a879b-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="a879b-106">これは、各送信メッセージにテキスト行を追加する非常に単純なプリプロセッサを実装して登録します。</span><span class="sxs-lookup"><span data-stu-id="a879b-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="a879b-107">このサンプルは、トランスポートニュートラルカプセル化形式 (TNEF) とテキストの間でメッセージの内容を分割する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a879b-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="a879b-108">また、すべての構成オプション (プロパティシート、ウィザード、およびプログラムの構成) とメッセージオプションもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a879b-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="a879b-109">リモートトランスポートインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a879b-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="a879b-110">このサンプルは、 [Outlook Messaging API (MAPI) コードサンプル](https://go.microsoft.com/fwlink/?LinkId=129740)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="a879b-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a879b-111">実行可能</span><span class="sxs-lookup"><span data-stu-id="a879b-111">Executable:</span></span>  <br/> |<span data-ttu-id="a879b-112">mrxp32</span><span class="sxs-lookup"><span data-stu-id="a879b-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="a879b-113">ソースコードディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="a879b-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="a879b-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="a879b-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="a879b-115">言語</span><span class="sxs-lookup"><span data-stu-id="a879b-115">Language:</span></span>  <br/> |<span data-ttu-id="a879b-116">+</span><span class="sxs-lookup"><span data-stu-id="a879b-116">C++</span></span>  <br/> |
|<span data-ttu-id="a879b-117">対象</span><span class="sxs-lookup"><span data-stu-id="a879b-117">Platforms:</span></span>  <br/> |<span data-ttu-id="a879b-118">windows Vista、windows server 2008、windows XP SP2、および windows server 2003 SP1 用にコンパイルする Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="a879b-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="a879b-119">サポートされる機能</span><span class="sxs-lookup"><span data-stu-id="a879b-119">Supported Features</span></span>

<span data-ttu-id="a879b-120">この例では、次の機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a879b-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="a879b-121">新しいメッセージの送信、受信、ポーリングなどの基本的な機能。</span><span class="sxs-lookup"><span data-stu-id="a879b-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="a879b-122">対話型およびプログラムによる構成。</span><span class="sxs-lookup"><span data-stu-id="a879b-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="a879b-123">**imapistatus**インターフェイス。ただし、プロパティの設定は除きます。</span><span class="sxs-lookup"><span data-stu-id="a879b-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="a879b-124">詳細については、 [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a879b-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="a879b-125">スレッドの安全性。</span><span class="sxs-lookup"><span data-stu-id="a879b-125">Thread safety.</span></span>
    
- <span data-ttu-id="a879b-126">テキストファイルへのイベントログ。</span><span class="sxs-lookup"><span data-stu-id="a879b-126">Event logging to a text file.</span></span> <span data-ttu-id="a879b-127">ファイルは、指定したサイズに自動的に制限されます。</span><span class="sxs-lookup"><span data-stu-id="a879b-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="a879b-128">すべてのトランスポートセッションは同じファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a879b-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="a879b-129">サポートされない機能</span><span class="sxs-lookup"><span data-stu-id="a879b-129">Unsupported Features</span></span>

<span data-ttu-id="a879b-130">このサンプルでは、受信メッセージの非同期検出をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="a879b-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="a879b-131">**サンプルトランスポートプロバイダーをインストールするには**</span><span class="sxs-lookup"><span data-stu-id="a879b-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="a879b-132">サンプルトランスポートプロバイダーをダウンロードするには、「 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a879b-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="a879b-133">Outlook MAPI サンプルを保存したフォルダーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="a879b-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="a879b-134">**OutlookMAPISamples-\<version\>番号**の zip フォルダーを右クリックし、[**すべて抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="a879b-135">[**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="a879b-136">Visual Studio 2008 を実行します。</span><span class="sxs-lookup"><span data-stu-id="a879b-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="a879b-137">Visual Studio 2008 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="a879b-138">サンプルを保存した場所を参照し、[ **mrxp32**] をクリックして、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="a879b-139">[**ビルド**] メニューの [**構成マネージャー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="a879b-140">[**構成マネージャー** ] ダイアログボックスで、 **mrxp32**の行に移動し、[**構成**] 列の [**リリース**] を選択して、[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="a879b-141">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="a879b-142">[名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="a879b-143">サンプルを保存したフォルダーで、インストールバッチファイルを右クリックし、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="a879b-144">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a879b-145">**.bat をインストール**すると、.dll は既定の Microsoft Office インストールフォルダーである C:\Program C:\Program Office\Office12 にコピーされます。\.</span><span class="sxs-lookup"><span data-stu-id="a879b-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="a879b-146">別の場所に Office 製品をインストールした場合は、[**インストール**] を右クリックし、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="a879b-147">ファイルがメモ帳で開きます。</span><span class="sxs-lookup"><span data-stu-id="a879b-147">The file opens in Notepad.</span></span> <span data-ttu-id="a879b-148">既定のインストールパスを、コンピューターで使用されているインストールパスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a879b-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="a879b-149">**Outlook でトランスポートプロバイダーをセットアップするには**</span><span class="sxs-lookup"><span data-stu-id="a879b-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="a879b-150">Outlook の [**ツール**] メニューの [**アカウント設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="a879b-151">[**アカウント設定**] ダイアログボックスの [**電子メール**] タブで、[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="a879b-152">[**電子メールサービスの選択**] で [**その他**] をクリックし、[ **MRXP Sample Transport**] を選択して、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="a879b-153">[ **MRXP Transport Configuration** ] ダイアログボックスで、**ユーザーの表示名**を入力します。</span><span class="sxs-lookup"><span data-stu-id="a879b-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="a879b-154">[ **path to Inbox (UNC 共有)** ] で、フォルダーのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a879b-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="a879b-155">また、ローカルフォルダーへのパスを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a879b-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="a879b-156">このパスは存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a879b-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="a879b-157">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="a879b-158">[**電子メールアカウントの追加**] ダイアログボックスで、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="a879b-159">[**完了**] をクリックし、[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="a879b-160">MRXP アカウントの使用を開始するには、Outlook を終了して再起動します。</span><span class="sxs-lookup"><span data-stu-id="a879b-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="a879b-161">**トランスポートプロバイダーのサンプルを使用して Outlook でメッセージを送信するには**</span><span class="sxs-lookup"><span data-stu-id="a879b-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="a879b-162">[**ファイル**] メニューの [**新規作成**] をクリックし、[**メールメッセージ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="a879b-163">[宛先\*\*\*\* ] ボックスに、受信者の名前を **[MRXP:\<\>ADDRESS]** の形式で入力します。</span><span class="sxs-lookup"><span data-stu-id="a879b-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="a879b-164">このアドレスは、受信者の受信トレイへの UNC 共有またはローカルフォルダーのパスです。</span><span class="sxs-lookup"><span data-stu-id="a879b-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a879b-165">アドレスにコロンまたは円記号がある場合は、各コロンまたは円記号の前にバックスラッシュを挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a879b-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="a879b-166">たとえば、[MRXP: C: \Mail\myDir] にメールを送信するには、 `[MRXP:C\:\\Mail\\myDir]`次のように入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a879b-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="a879b-167">受信者のアドレスが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="a879b-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="a879b-168">[**アカウント**] をクリックし、[ **MRXP Sample Transport**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="a879b-169">メッセージを入力し、[**送信**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-169">Type your message and click **Send**.</span></span> <span data-ttu-id="a879b-170">メッセージは MRXP トランスポートプロバイダーを使用して送信されます。</span><span class="sxs-lookup"><span data-stu-id="a879b-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="a879b-171">**トランスポートプロバイダーのサンプルを使用して Outlook でメッセージを受信するには**</span><span class="sxs-lookup"><span data-stu-id="a879b-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="a879b-172">[**ファイル**] メニューの [**新規作成**] をクリックし、[**メールメッセージ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="a879b-173">メッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="a879b-173">Type your message.</span></span>
    
3. <span data-ttu-id="a879b-174">**Microsoft Office ボタン**をクリックし、[名前を付け**て保存**] をクリックし、[名前を付けて保存] をクリックし**て**、セットアップ時に指定した受信トレイフォルダーにファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="a879b-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="a879b-175">[**名前を付けて保存**] ダイアログボックスで、受信トレイとして設定した UNC 共有またはローカルフォルダーを参照します。</span><span class="sxs-lookup"><span data-stu-id="a879b-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="a879b-176">[**ファイルの種類**] ドロップダウンで、[ **Outlook メッセージ形式**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="a879b-177">ファイルの名前を入力し、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a879b-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="a879b-178">ファイルが共有フォルダーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="a879b-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="a879b-179">MRXP トランスポートプロバイダーは、Outlook の受信トレイにメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="a879b-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

