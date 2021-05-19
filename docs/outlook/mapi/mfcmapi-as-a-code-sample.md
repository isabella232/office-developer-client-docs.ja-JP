---
title: コード サンプルとしての MFCMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356862"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="feb51-103">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="feb51-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="feb51-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feb51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feb51-105">MFCMAPI サンプルでは、メッセージング API を使用して、グラフィカル ユーザー インターフェイスを介して MAPI ストアへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="feb51-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="feb51-106">このサンプルをダウンロードした後、ソース ファイルを使用して、多くの MAPI インターフェイスと参照の使用例を確認できます。</span><span class="sxs-lookup"><span data-stu-id="feb51-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="feb51-107">詳細については [、「MAPI インターフェイス」を参照してください](mapi-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="feb51-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="feb51-108">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="feb51-108">Platforms:</span></span>  <br/> |<span data-ttu-id="feb51-109">Microsoft Visual Studio 2008 Windows 7、Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 用にコンパイルする</span><span class="sxs-lookup"><span data-stu-id="feb51-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="feb51-110">MFCMAPI をダウンロードするには</span><span class="sxs-lookup"><span data-stu-id="feb51-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="feb51-111">[[MFCMAPI] ページで](https://codeplex.com/MFCMAPI)、[ソース コード]**タブをクリック** します。</span><span class="sxs-lookup"><span data-stu-id="feb51-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="feb51-112">[ **最近のチェックイン] で、[** 最新の **ビルドのダウンロード** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="feb51-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="feb51-113">使用許諾契約書を読み、[同意する] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="feb51-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="feb51-114">**[ファイルのダウンロード]** ダイアログ ボックスで **[保存]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="feb51-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="feb51-115">[名前 **を付けて保存** ] ダイアログ ボックスで、ソース ファイルを保存するフォルダーを探し、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="feb51-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="feb51-116">[ダウンロードの **完了] ダイアログ ボックス** で、[フォルダーを開く] **をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="feb51-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="feb51-117">[閉じる] **をクリック** してダイアログ ボックスを閉じ、保存したフォルダー内の圧縮されたソース ファイルを検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="feb51-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="feb51-118">MFCMAPI- バージョン番号ファイルを右クリック.zip、[すべて展開]**をクリックします**。 **\< \>**</span><span class="sxs-lookup"><span data-stu-id="feb51-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="feb51-119">表示されるダイアログ ボックスで、[抽出] **を** クリックして、表示されるフォルダーにファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="feb51-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="feb51-120">[参照] をクリック **して** 別のフォルダーを選択または作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="feb51-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="feb51-121">管理者Visual Studio 2008 を実行します。</span><span class="sxs-lookup"><span data-stu-id="feb51-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="feb51-122">XP でコンピューターがWindowsしている場合は、管理者としてログインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="feb51-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="feb51-123">コンピューターが Windows Vista を実行している場合は、管理者としてログインし、Visual Studio 2008 アイコンを右クリックし、[管理者として実行] をクリックする必要 **があります**。</span><span class="sxs-lookup"><span data-stu-id="feb51-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="feb51-124">[Visual Studio 2008 で、[ファイル] をクリックし、[開く] をポイントして **、[Project/ソリューション] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="feb51-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="feb51-125">サンプルを保存した場所を参照し **、[MFCMapi.vcproj]** を選択し、[開く] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="feb51-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="feb51-126">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="feb51-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="feb51-127">[ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="feb51-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="feb51-128">MFCMAPI をコード サンプルとして使用するには</span><span class="sxs-lookup"><span data-stu-id="feb51-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="feb51-129">ソリューション **エクスプローラーで\*\*\*\*、MFCMapi** プロジェクトを展開し、プログラミング シナリオ用のヘッダー ファイル、リソース ファイル、およびソース ファイル ノードのファイルを調べてください。</span><span class="sxs-lookup"><span data-stu-id="feb51-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="feb51-130">[MAPI インターフェイス] セクションの [多くのメソッド トピック](mapi-interfaces.md) は、プログラミングの例を示す MFCMAPI ソース ファイルを指しています。</span><span class="sxs-lookup"><span data-stu-id="feb51-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="feb51-131">たとえば [、IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) では  `CMsgStoreDlg::OnDisplayReceiveFolderTable` 、MsgStoreDlg.cpp ファイル内の関数を確認するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="feb51-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="feb51-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="feb51-132">See also</span></span>

- [<span data-ttu-id="feb51-133">MAPI Samples</span><span class="sxs-lookup"><span data-stu-id="feb51-133">MAPI Samples</span></span>](mapi-samples.md)

