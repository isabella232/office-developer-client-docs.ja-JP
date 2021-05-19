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
# <a name="install-the-samples-used-in-this-section"></a><span data-ttu-id="c9d73-103">このセクションで使用されるサンプルをインストールする</span><span class="sxs-lookup"><span data-stu-id="c9d73-103">Install the samples used in this section</span></span>

<span data-ttu-id="c9d73-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9d73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9d73-105">MFCMAPI アプリケーションと CreateOutlookItemsAddin プロジェクトをインストールして[、「MAPI](creating-outlook-items-by-using-mapi.md)を使用して Outlook アイテムを作成する」セクションのトピックで参照されているサンプル コードを表示および実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-105">To install the MFCMAPI application and CreateOutlookItemsAddin project to view and run the sample code referenced by the topics in the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section, follow these steps.</span></span> 

<span data-ttu-id="c9d73-106">「MAPI を使用してアイテムを作成する」セクションで使用する例をダウンロードOutlook手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c9d73-106">To download and install the examples used in the "Using MAPI to create Outlook items" section, follow these steps.</span></span>

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a><span data-ttu-id="c9d73-107">MFCMAPI アプリケーションをダウンロードしてインストールし、CreateOutlookItemsAddin プロジェクトを開く方法</span><span class="sxs-lookup"><span data-stu-id="c9d73-107">To download and install the MFCMAPI application and open CreateOutlookItemsAddin project</span></span>

1. <span data-ttu-id="c9d73-108">MFCMAPI 実行可能ファイルの現在 [のバージョンを](https://go.microsoft.com/fwlink/?LinkID=124154) システム上のフォルダーにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c9d73-108">Download the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) executable to a folder on your system.</span></span> 
    
2. <span data-ttu-id="c9d73-109">ファイル内のMFCMapi.exeファイルをMFCMapi.exe。</span><span class="sxs-lookup"><span data-stu-id="c9d73-109">Extract the MFCMapi.exe file in MFCMapi.exe.</span></span> <span data-ttu-id="c9d73-110">_バージョン_.zip、ハード ドライブ上の空のフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-110">_version_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="c9d73-111">[CreateOutlookItemsAddin プロジェクトの現在のバージョンをダウンロード](https://go.microsoft.com/fwlink/?LinkID=127828)します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-111">Download the current version of the [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) project.</span></span> 
    
4. <span data-ttu-id="c9d73-112">手順 2 で CreateOutlookItemsAddin.zip MFCMapi.exeファイルを抽出したフォルダーに、CreateOutlookItemsAddin.zipファイル内のすべてのファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-112">Extract all the files in the CreateOutlookItemsAddin.zip file to the folder where you extracted the MFCMapi.exe file in Step 2.</span></span>
    
5. <span data-ttu-id="c9d73-113">手順 2 でMFCMapi.exeフォルダーから CreateOutlookItemsAddin プロジェクトのビルド ディレクトリにコピーします (\CreateOutlookItemsAddin\Debug)。</span><span class="sxs-lookup"><span data-stu-id="c9d73-113">Copy MFCMapi.exe from the folder used in Step 2 to the build directory for the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\Debug).</span></span>
    
6. <span data-ttu-id="c9d73-114">Visual Studio で CreateOutlookItemsAddin プロジェクト (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) を開き、ソース コードを確認します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-114">Open the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio to examine the source code.</span></span> <span data-ttu-id="c9d73-115">開くソース ファイルを決定するにはOutlook [MAPI](creating-outlook-items-by-using-mapi.md)を使用してアイテムを作成するセクションのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9d73-115">Refer to the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section to determine which source files to open.</span></span> 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a><span data-ttu-id="c9d73-116">MFCMAPI と CreateOutlookItemsAddin プロジェクトを実行する</span><span class="sxs-lookup"><span data-stu-id="c9d73-116">Run MFCMAPI and the CreateOutlookItemsAddin project</span></span>

<span data-ttu-id="c9d73-117">次の手順では、前の手順で説明したように、MFCMAPI 実行可能ファイルと CreateOutlookItemsAddin プロジェクトの現在のバージョンをダウンロードしてインストールしたと仮定します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-117">The following steps assume that you have downloaded and installed the current version of the MFCMAPI executable and the CreateOutlookItemsAddin project as described in the preceding procedure.</span></span> <span data-ttu-id="c9d73-118">次の手順では、MFCMAPI アプリケーションと CreateOutlookItemsAddin プロジェクトを使用して Outlook アイテムを作成できるアドイン メニュー項目について説明します。 </span><span class="sxs-lookup"><span data-stu-id="c9d73-118">These steps will guide you to the **Addins** menu items that enable you to create Outlook items using the MFCMAPI application and the CreateOutlookItemsAddin project.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c9d73-119">手順 8 で選択したフォルダーと、手順 9 で選択するコマンドは[、[MAPI](creating-outlook-items-by-using-mapi.md)を使用して Outlook アイテムを作成する] セクションのいずれかのトピックで説明されている項目の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c9d73-119">The folder you select in step 8, and the command you select in step 9, depends on the item type discussed in one of the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section.</span></span> 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a><span data-ttu-id="c9d73-120">MFCMAPI アプリケーションと Addins メニュー コマンドを実行するには</span><span class="sxs-lookup"><span data-stu-id="c9d73-120">To run the MFCMAPI application and Addins menu commands</span></span>

1. <span data-ttu-id="c9d73-121">インストールMfcmapi.exeに従って作成される CreateOutlookItemsAddin\Debug フォルダーから開始します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-121">Start Mfcmapi.exe in the CreateOutlookItemsAddin\Debug folder that is created when you follow the installation instructions.</span></span>
    
2. <span data-ttu-id="c9d73-122">**[OK] を** クリックして、MFCMAPI スプラッシュ画面を閉じします。</span><span class="sxs-lookup"><span data-stu-id="c9d73-122">Click **OK** to dismiss the MFCMAPI splash screen.</span></span> 
    
3. <span data-ttu-id="c9d73-123">[セッション] **メニューの** [ログオンと **ストアテーブルの表示] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="c9d73-123">On the **Session** menu, click **Logon and Display Store Table**.</span></span>
    
4. <span data-ttu-id="c9d73-124">[プロファイルの **選択] ダイアログ** ボックスで、正しいプロファイルを選択し **、[OK] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="c9d73-124">In the **Choose Profile** dialog box, select the correct profile, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="c9d73-125">[メールボックス] **-  _[ユーザー名] を_** ストア テーブルの一覧ビューでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9d73-125">Double-click **Mailbox -  _[User Name]_** in the store table list view.</span></span> 
    
6. <span data-ttu-id="c9d73-126">フォルダー ツリー ビューで、ルート ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-126">In the folder tree view, expand the root node.</span></span> <span data-ttu-id="c9d73-127">ルート ノードに表示される名前は、選択したプロファイルの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c9d73-127">The name displayed for the root node varies depending on the type of profile selected.</span></span> <span data-ttu-id="c9d73-128">通常、このノードはルート **- メールボックスとして表示されます**。</span><span class="sxs-lookup"><span data-stu-id="c9d73-128">Typically this node is displayed as **Root - Mailbox**.</span></span>
    
7. <span data-ttu-id="c9d73-129">フォルダー ツリー ビューで、情報ストアを含むノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-129">In the folder tree view, expand the node that contains the information store.</span></span> <span data-ttu-id="c9d73-130">このノードに表示される名前は、選択したプロファイルの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c9d73-130">The name displayed for this node varies depending on the type of profile selected.</span></span> <span data-ttu-id="c9d73-131">通常、このノードは **、IPM_SUBTREEまたは** Top of Information **Store として表示されます**。</span><span class="sxs-lookup"><span data-stu-id="c9d73-131">Typically this node is displayed as **IPM_SUBTREE** or **Top of Information Store**.</span></span>
    
8. <span data-ttu-id="c9d73-132">作成するアイテムの種類のフォルダーをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9d73-132">Double-click the folder for the item type to create.</span></span> <span data-ttu-id="c9d73-133">たとえば、予定を作成するには、[予定] **フォルダーをクリック** します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-133">For example, to create an appointment, click the **Appointments** folder.</span></span> 
    
9. <span data-ttu-id="c9d73-134">[アドイン **] メニューで** 、作成するアイテムの適切なコマンドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9d73-134">On the **Addins** menu, click the appropriate command for the item to create.</span></span> 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a><span data-ttu-id="c9d73-135">MFCMAPI アプリケーションからコードをダウンロードして表示する</span><span class="sxs-lookup"><span data-stu-id="c9d73-135">Download and view code from the MFCMAPI application</span></span>

<span data-ttu-id="c9d73-136">一部のトピックでは、MFCMAPI アプリケーション自体のソース コードを参照します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-136">Some topics refer to source code from the MFCMAPI application itself.</span></span> <span data-ttu-id="c9d73-137">次の手順では、MFCMAPI ソース コードをダウンロードし、そのソース コードを表示する方法Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="c9d73-137">The following steps describe how to download the MFCMAPI source code and view it in Visual Studio.</span></span> 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a><span data-ttu-id="c9d73-138">MFCMAPI アプリケーションのソース コードをダウンロードして表示するには</span><span class="sxs-lookup"><span data-stu-id="c9d73-138">To download and view the MFCMAPI application source code</span></span>

1. <span data-ttu-id="c9d73-139">[MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154)アプリケーションの現在のバージョンのソース コードをシステム上のフォルダーにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c9d73-139">Download the source code for the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) application to a folder on your system.</span></span> 
    
2. <span data-ttu-id="c9d73-140">MFCMAPI- 変更セット内の.zip、ハード ドライブ上の空のフォルダーに展開します。</span><span class="sxs-lookup"><span data-stu-id="c9d73-140">Extract the files in MFCMAPI- _changeset_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="c9d73-141">ソース コードを調べるには、MFCMapi プロジェクト (\ _foldername_\ MFCMapi.vcproj) をVisual Studioで開きます。</span><span class="sxs-lookup"><span data-stu-id="c9d73-141">Open the MFCMapi project (\ _foldername_\ MFCMapi.vcproj) in Visual Studio to examine the source code.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9d73-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9d73-142">See also</span></span>

- [<span data-ttu-id="c9d73-143">簡易メール アイテムの作成</span><span class="sxs-lookup"><span data-stu-id="c9d73-143">Create a Simple Mail Item</span></span>](how-to-create-a-simple-mail-item.md)
- [<span data-ttu-id="c9d73-144">単純な繰り返しタスク アイテムの作成</span><span class="sxs-lookup"><span data-stu-id="c9d73-144">Create a Simple Recurrent Task Item</span></span>](how-to-create-a-simple-recurrent-task-item.md)
- [<span data-ttu-id="c9d73-145">複雑な繰り返し予定アイテムの作成</span><span class="sxs-lookup"><span data-stu-id="c9d73-145">Create a Complex Recurrent Appointment Item</span></span>](how-to-create-a-complex-recurrent-appointment-item.md)
- [<span data-ttu-id="c9d73-146">定期的なパターンの読み取りと解析</span><span class="sxs-lookup"><span data-stu-id="c9d73-146">Read and Parse a Recurrence Pattern</span></span>](how-to-read-and-parse-a-recurrence-pattern.md)

