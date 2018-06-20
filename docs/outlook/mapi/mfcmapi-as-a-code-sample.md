---
title: MFCMAPI をコード サンプルとして
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fc92cc8deb3d12c4bc8fca4c680fd4a675b4a578
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801638"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="f1f84-103">MFCMAPI をコード サンプルとして</span><span class="sxs-lookup"><span data-stu-id="f1f84-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="f1f84-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1f84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1f84-105">MFCMAPI サンプルでは、メッセージング API を使用して、グラフィカル ユーザー インターフェイスによって、MAPI ストアへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f1f84-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="f1f84-106">このサンプルをダウンロードした後は、MAPI インターフェイス、および参照の多くの例の使用状況を確認するのにはソース ファイルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1f84-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="f1f84-107">詳細については、 [MAPI インターフェイス](mapi-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1f84-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1f84-108">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="f1f84-108">Platforms:</span></span>  <br/> |<span data-ttu-id="f1f84-109">Windows 7、Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 のプログラムをコンパイルするのには、Microsoft Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="f1f84-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="f1f84-110">MFCMAPI をダウンロードするには</span><span class="sxs-lookup"><span data-stu-id="f1f84-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="f1f84-111">[MFCMAPI](http://codeplex.com/MFCMAPI) ] ページで、[**ソース コード**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-111">On the [MFCMAPI](http://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="f1f84-112">[**最近のチェックイン**では、最新のビルドでは、[**ダウンロード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="f1f84-113">ライセンス契約を読み、[ **I Agree**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="f1f84-114">**ファイルのダウンロード**] ダイアログ ボックスで [**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="f1f84-115">**名前を付けて保存**] ダイアログ ボックスで、ソース ファイルを保存するフォルダーを見つけてし、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="f1f84-116">**[ダウンロードの完了**] ダイアログ ボックスで**フォルダーを開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="f1f84-117">**を閉じる**] ダイアログ ボックスを閉じるしでそれらを保存したフォルダー内の圧縮されたソース ファイルを検索をクリックすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f1f84-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="f1f84-118">右クリックし、 **MFCMAPI -\<バージョン番号\>.zip**ファイル、および、[**すべて展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="f1f84-119">ダイアログ ボックスが表示されたら、表示されているフォルダーにファイルを抽出する**抽出**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="f1f84-120">**参照**を選択するか、別のフォルダーを作成するをクリックすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f1f84-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="f1f84-121">Visual Studio 2008 を管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="f1f84-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="f1f84-122">場合は、コンピューターが Windows XP を実行して、必要がありますログインするは、管理者として。</span><span class="sxs-lookup"><span data-stu-id="f1f84-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="f1f84-123">お使いのコンピューターには、Windows Vista を実行して、管理者としてに記録される必要があり、Visual Studio 2008 のアイコンを右クリックし、[**管理者として実行**] をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1f84-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="f1f84-124">Visual Studio 2008 で、[**ファイル**] をクリックを選択し、[**開く**] をポイントし、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="f1f84-125">サンプルを保存する場所を参照する**MFCMapi.vcproj**を選択し、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="f1f84-126">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="f1f84-127">**ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="f1f84-128">MFCMAPI をコード サンプルとして使用するには</span><span class="sxs-lookup"><span data-stu-id="f1f84-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="f1f84-129">**ソリューション エクスプ ローラー**では、 **MFCMapi**プロジェクトを展開し、プログラミング シナリオについては、**ヘッダー ファイル**、**リソース ファイル**、および**ソース ファイル**のノードでのファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="f1f84-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="f1f84-130">[MAPI インターフェイス](mapi-interfaces.md)で多くのメソッドのトピックでは、プログラミングの例については、MFCMAPI ソース ファイルをポイントします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="f1f84-131">たとえば、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)での指示がある関数を検索する`CMsgStoreDlg::OnDisplayReceiveFolderTable`MsgStoreDlg.cpp ファイルにします。</span><span class="sxs-lookup"><span data-stu-id="f1f84-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1f84-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1f84-132">See also</span></span>

- [<span data-ttu-id="f1f84-133">MAPI Samples</span><span class="sxs-lookup"><span data-stu-id="f1f84-133">MAPI Samples</span></span>](mapi-samples.md)

