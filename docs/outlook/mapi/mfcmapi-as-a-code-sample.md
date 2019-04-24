---
title: コード サンプルとしての MFCMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356862"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="d7136-103">コード サンプルとしての MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d7136-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="d7136-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7136-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7136-105">mfcmapi サンプルでは、メッセージング API を使用して、グラフィカルユーザーインターフェイスを介して MAPI ストアへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d7136-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="d7136-106">このサンプルをダウンロードすると、ソースファイルを使用して、多くの MAPI インターフェイスおよび参照の使用状況の例を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="d7136-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="d7136-107">詳細については、「 [MAPI のインターフェイス](mapi-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7136-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7136-108">対象</span><span class="sxs-lookup"><span data-stu-id="d7136-108">Platforms:</span></span>  <br/> |<span data-ttu-id="d7136-109">windows 7、windows Vista、windows server 2008、windows XP SP2、および windows server 2003 SP1 をコンパイルするための Microsoft Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="d7136-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="d7136-110">mfcmapi をダウンロードするには</span><span class="sxs-lookup"><span data-stu-id="d7136-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="d7136-111">[ [mfcmapi](https://codeplex.com/MFCMAPI) ] ページで、[**ソースコード**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="d7136-112">[**最近のチェックイン**] で、最新のビルドに対して [**ダウンロード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="d7136-113">使用許諾契約書の内容を確認し、[**同意**する] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="d7136-114">**[ファイルのダウンロード]** ダイアログ ボックスで **[保存]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="d7136-115">[名前を付け**て保存**] ダイアログボックスで、ソースファイルを保存するフォルダーを見つけ、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="d7136-116">[**ダウンロードの完了**] ダイアログボックスで、[**フォルダーを開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="d7136-117">また、[**閉じる**] をクリックしてダイアログボックスを閉じ、保存したフォルダーで zip 形式のソースファイルを特定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d7136-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="d7136-118">**mfcmapi\<-バージョン番号\>.zip**ファイルを右クリックし、[**すべて展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="d7136-119">表示されるダイアログボックスで、[**抽出**] をクリックして、表示されているフォルダーにファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="d7136-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="d7136-120">[**参照**] をクリックして、別のフォルダーを選択または作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d7136-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="d7136-121">管理者として Visual Studio 2008 を実行します。</span><span class="sxs-lookup"><span data-stu-id="d7136-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="d7136-122">Windows XP を実行しているコンピューターでは、管理者としてログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7136-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="d7136-123">Windows Vista を実行しているコンピューターでは、管理者としてログインしていて、Visual Studio 2008 アイコンを右クリックし、[**管理者として実行**] をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7136-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="d7136-124">Visual Studio 2008 で、[**ファイル**] をクリックし、[**開く**] をポイントして、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="d7136-125">サンプルを保存した場所に移動し、[ **mfcmapi .vcproj**] を選択して、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="d7136-126">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="d7136-127">[名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7136-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="d7136-128">コードサンプルとして mfcmapi を使用するには</span><span class="sxs-lookup"><span data-stu-id="d7136-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="d7136-129">**ソリューションエクスプローラー**で、[ **mfcmapi** ] プロジェクトを展開し、[**ヘッダーファイル**]、[**リソースファイル**]、[**ソースファイル**] の各ノード内のファイルを調べてプログラミングシナリオを確認します。</span><span class="sxs-lookup"><span data-stu-id="d7136-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="d7136-130">「 [MAPI のインターフェイス](mapi-interfaces.md)」セクションにある多くのメソッドのトピックでは、プログラミング例のために mfcmapi ソースファイルをポイントしています。</span><span class="sxs-lookup"><span data-stu-id="d7136-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="d7136-131">たとえば、 [IMsgStore:: getreceivefoldertable](imsgstore-getreceivefoldertable.md)では、MsgStoreDlg ファイル内の関数`CMsgStoreDlg::OnDisplayReceiveFolderTable`を参照するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="d7136-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7136-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7136-132">See also</span></span>

- [<span data-ttu-id="d7136-133">MAPI Samples</span><span class="sxs-lookup"><span data-stu-id="d7136-133">MAPI Samples</span></span>](mapi-samples.md)

