---
title: このセクションで使用されるサンプルをインストールする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345550"
---
# <a name="install-the-samples-used-in-this-section"></a><span data-ttu-id="c986f-103">このセクションで使用されるサンプルをインストールする</span><span class="sxs-lookup"><span data-stu-id="c986f-103">Install the samples used in this section</span></span>

<span data-ttu-id="c986f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c986f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c986f-105">mfcmapi アプリケーションと createoutlookitemsaddin プロジェクトをインストールするには、「 [MAPI を使用した Outlook アイテムの作成](creating-outlook-items-by-using-mapi.md)」セクションのトピックで参照されているサンプルコードを表示して実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c986f-105">To install the MFCMAPI application and CreateOutlookItemsAddin project to view and run the sample code referenced by the topics in the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section, follow these steps.</span></span> 

<span data-ttu-id="c986f-106">「MAPI を使用して Outlook アイテムを作成する」セクションで使用されている例をダウンロードしてインストールするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c986f-106">To download and install the examples used in the "Using MAPI to create Outlook items" section, follow these steps.</span></span>

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a><span data-ttu-id="c986f-107">mfcmapi アプリケーションをダウンロードしてインストールし、createoutlookitemsaddin プロジェクトを開くには</span><span class="sxs-lookup"><span data-stu-id="c986f-107">To download and install the MFCMAPI application and open CreateOutlookItemsAddin project</span></span>

1. <span data-ttu-id="c986f-108">現在のバージョンの[mfcmapi](https://go.microsoft.com/fwlink/?LinkID=124154)実行可能ファイルを、システム上のフォルダーにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c986f-108">Download the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) executable to a folder on your system.</span></span> 
    
2. <span data-ttu-id="c986f-109">mfcmapi の mfcmapi .exe ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="c986f-109">Extract the MFCMapi.exe file in MFCMapi.exe.</span></span> <span data-ttu-id="c986f-110">__ ハードドライブの空のフォルダーに .zip を圧縮します。</span><span class="sxs-lookup"><span data-stu-id="c986f-110">_version_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="c986f-111">[createoutlookitemsaddin](https://go.microsoft.com/fwlink/?LinkID=127828)プロジェクトの現在のバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c986f-111">Download the current version of the [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) project.</span></span> 
    
4. <span data-ttu-id="c986f-112">手順2で mfcmapi の .exe ファイルを抽出したフォルダーに、createoutlookitemsaddin .zip ファイル内のすべてのファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="c986f-112">Extract all the files in the CreateOutlookItemsAddin.zip file to the folder where you extracted the MFCMapi.exe file in Step 2.</span></span>
    
5. <span data-ttu-id="c986f-113">手順2で使用したフォルダーから、createoutlookitemsaddin プロジェクト (\CreateOutlookItemsAddin\Debug) のビルドディレクトリに mfcmapi をコピーします。</span><span class="sxs-lookup"><span data-stu-id="c986f-113">Copy MFCMapi.exe from the folder used in Step 2 to the build directory for the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\Debug).</span></span>
    
6. <span data-ttu-id="c986f-114">Visual Studio で createoutlookitemsaddin プロジェクト (\ createoutlookitemsaddin¥ createoutlookitemsaddin¥ .vcproj) を開き、ソースコードを調べます。</span><span class="sxs-lookup"><span data-stu-id="c986f-114">Open the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio to examine the source code.</span></span> <span data-ttu-id="c986f-115">開くソースファイルを確認するには、「 [MAPI を使用して Outlook アイテムを作成](creating-outlook-items-by-using-mapi.md)する」セクションのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c986f-115">Refer to the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section to determine which source files to open.</span></span> 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a><span data-ttu-id="c986f-116">mfcmapi および createoutlookitemsaddin プロジェクトを実行する</span><span class="sxs-lookup"><span data-stu-id="c986f-116">Run MFCMAPI and the CreateOutlookItemsAddin project</span></span>

<span data-ttu-id="c986f-117">次の手順では、前の手順で説明したように、現在のバージョンの mfcmapi 実行可能ファイルおよび createoutlookitemsaddin プロジェクトをダウンロードしてインストールしていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c986f-117">The following steps assume that you have downloaded and installed the current version of the MFCMAPI executable and the CreateOutlookItemsAddin project as described in the preceding procedure.</span></span> <span data-ttu-id="c986f-118">次の手順では、mfcmapi アプリケーションと createoutlookitemsaddin プロジェクトを使用して Outlook アイテムを作成できる**Addins**メニューの項目について説明します。</span><span class="sxs-lookup"><span data-stu-id="c986f-118">These steps will guide you to the **Addins** menu items that enable you to create Outlook items using the MFCMAPI application and the CreateOutlookItemsAddin project.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c986f-119">手順8で選択するフォルダーと手順9で選択するコマンドは、「 [MAPI を使用した Outlook アイテムの作成](creating-outlook-items-by-using-mapi.md)」セクションに記載されているアイテムの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c986f-119">The folder you select in step 8, and the command you select in step 9, depends on the item type discussed in one of the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section.</span></span> 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a><span data-ttu-id="c986f-120">mfcmapi アプリケーションと Addins メニューコマンドを実行するには</span><span class="sxs-lookup"><span data-stu-id="c986f-120">To run the MFCMAPI application and Addins menu commands</span></span>

1. <span data-ttu-id="c986f-121">インストール手順に従って作成された CreateOutlookItemsAddin\Debug フォルダーで、mfcmapi を起動します。</span><span class="sxs-lookup"><span data-stu-id="c986f-121">Start Mfcmapi.exe in the CreateOutlookItemsAddin\Debug folder that is created when you follow the installation instructions.</span></span>
    
2. <span data-ttu-id="c986f-122">[ **OK]** をクリックして、mfcmapi のスプラッシュ画面を閉じます。</span><span class="sxs-lookup"><span data-stu-id="c986f-122">Click **OK** to dismiss the MFCMAPI splash screen.</span></span> 
    
3. <span data-ttu-id="c986f-123">[**セッション**] メニューの [**ログオンおよび表示ストアテーブル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c986f-123">On the **Session** menu, click **Logon and Display Store Table**.</span></span>
    
4. <span data-ttu-id="c986f-124">[**プロファイルの選択**] ダイアログボックスで、適切なプロファイルを選択し、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c986f-124">In the **Choose Profile** dialog box, select the correct profile, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="c986f-125">[store table] リストビューで、[\*\*メールボックス- _[ユーザー名]_ \*\*をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="c986f-125">Double-click **Mailbox -  _[User Name]_** in the store table list view.</span></span> 
    
6. <span data-ttu-id="c986f-126">フォルダーツリービューで、ルートノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="c986f-126">In the folder tree view, expand the root node.</span></span> <span data-ttu-id="c986f-127">ルートノードに表示される名前は、選択されているプロファイルの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c986f-127">The name displayed for the root node varies depending on the type of profile selected.</span></span> <span data-ttu-id="c986f-128">通常、このノードは**ルートメールボックス**として表示されます。</span><span class="sxs-lookup"><span data-stu-id="c986f-128">Typically this node is displayed as **Root - Mailbox**.</span></span>
    
7. <span data-ttu-id="c986f-129">フォルダーツリービューで、インフォメーションストアが格納されているノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="c986f-129">In the folder tree view, expand the node that contains the information store.</span></span> <span data-ttu-id="c986f-130">このノードに表示される名前は、選択されているプロファイルの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c986f-130">The name displayed for this node varies depending on the type of profile selected.</span></span> <span data-ttu-id="c986f-131">通常、このノードは**IPM_SUBTREE**または**インフォメーションストアのトップ**として表示されます。</span><span class="sxs-lookup"><span data-stu-id="c986f-131">Typically this node is displayed as **IPM_SUBTREE** or **Top of Information Store**.</span></span>
    
8. <span data-ttu-id="c986f-132">作成するアイテムの種類のフォルダーをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="c986f-132">Double-click the folder for the item type to create.</span></span> <span data-ttu-id="c986f-133">たとえば、予定を作成するには、[**予定**] フォルダーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c986f-133">For example, to create an appointment, click the **Appointments** folder.</span></span> 
    
9. <span data-ttu-id="c986f-134">[ **Addins** ] メニューで、作成するアイテムに適したコマンドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c986f-134">On the **Addins** menu, click the appropriate command for the item to create.</span></span> 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a><span data-ttu-id="c986f-135">mfcmapi アプリケーションからコードをダウンロードして表示する</span><span class="sxs-lookup"><span data-stu-id="c986f-135">Download and view code from the MFCMAPI application</span></span>

<span data-ttu-id="c986f-136">一部のトピックでは、mfcmapi アプリケーション自体のソースコードを参照しています。</span><span class="sxs-lookup"><span data-stu-id="c986f-136">Some topics refer to source code from the MFCMAPI application itself.</span></span> <span data-ttu-id="c986f-137">次の手順では、mfcmapi ソースコードをダウンロードして Visual Studio で表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c986f-137">The following steps describe how to download the MFCMAPI source code and view it in Visual Studio.</span></span> 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a><span data-ttu-id="c986f-138">mfcmapi アプリケーションのソースコードをダウンロードして表示するには</span><span class="sxs-lookup"><span data-stu-id="c986f-138">To download and view the MFCMAPI application source code</span></span>

1. <span data-ttu-id="c986f-139">現在のバージョンの[mfcmapi](https://go.microsoft.com/fwlink/?LinkID=124154)アプリケーションのソースコードを、システム上のフォルダーにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c986f-139">Download the source code for the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) application to a folder on your system.</span></span> 
    
2. <span data-ttu-id="c986f-140">mfcmapi-_変更セット_.zip 内のファイルを、ハードドライブ上の空のフォルダーに抽出します。</span><span class="sxs-lookup"><span data-stu-id="c986f-140">Extract the files in MFCMAPI- _changeset_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="c986f-141">Visual Studio で mfcmapi プロジェクト (\ _foldername_/mfcmapi .vcproj) を開き、ソースコードを調べます。</span><span class="sxs-lookup"><span data-stu-id="c986f-141">Open the MFCMapi project (\ _foldername_\ MFCMapi.vcproj) in Visual Studio to examine the source code.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c986f-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="c986f-142">See also</span></span>

- [<span data-ttu-id="c986f-143">簡単なメールアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="c986f-143">Create a Simple Mail Item</span></span>](how-to-create-a-simple-mail-item.md)
- [<span data-ttu-id="c986f-144">単純な定期的なタスクアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="c986f-144">Create a Simple Recurrent Task Item</span></span>](how-to-create-a-simple-recurrent-task-item.md)
- [<span data-ttu-id="c986f-145">複雑な定期的な予定アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="c986f-145">Create a Complex Recurrent Appointment Item</span></span>](how-to-create-a-complex-recurrent-appointment-item.md)
- [<span data-ttu-id="c986f-146">定期的なパターンの読み取りと解析</span><span class="sxs-lookup"><span data-stu-id="c986f-146">Read and Parse a Recurrence Pattern</span></span>](how-to-read-and-parse-a-recurrence-pattern.md)

