---
title: アドレス帳プロバイダー サンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c32017598407760d5dbbb01ee6c28267bbffd152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799639"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="7bc92-103">アドレス帳プロバイダー サンプル</span><span class="sxs-lookup"><span data-stu-id="7bc92-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="7bc92-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bc92-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bc92-105">このサンプルには、表示名と電子メール アドレスは、バイナリのフラット ファイルからの読み取りは、1 つの読み取り専用コンテナーがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7bc92-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="7bc92-106">サンプルには、1 回限りのテンプレートおよびプロファイル ウィザードを除くすべての構成オプションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7bc92-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="7bc92-107">[Outlook メッセージング API (MAPI) のサンプル コード](http://go.microsoft.com/fwlink/?LinkId=129740
)からは、このサンプルをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="7bc92-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7bc92-108">実行可能ファイル:</span><span class="sxs-lookup"><span data-stu-id="7bc92-108">Executable:</span></span>  <br/> |<span data-ttu-id="7bc92-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="7bc92-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="7bc92-110">ソース コードのディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="7bc92-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="7bc92-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="7bc92-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="7bc92-112">言語:</span><span class="sxs-lookup"><span data-stu-id="7bc92-112">Language:</span></span>  <br/> |<span data-ttu-id="7bc92-113">C++</span><span class="sxs-lookup"><span data-stu-id="7bc92-113">C++</span></span>  <br/> |
|<span data-ttu-id="7bc92-114">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="7bc92-114">Platforms:</span></span>  <br/> |<span data-ttu-id="7bc92-115">Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 のプログラムをコンパイルするのには、Microsoft Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="7bc92-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="7bc92-116">サポートされている機能</span><span class="sxs-lookup"><span data-stu-id="7bc92-116">Supported Features</span></span>

<span data-ttu-id="7bc92-117">このサンプルには、次の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7bc92-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="7bc92-118">テーブルの制限です。</span><span class="sxs-lookup"><span data-stu-id="7bc92-118">Table restrictions.</span></span> <span data-ttu-id="7bc92-119">サンプルでは、プレフィックスに一致およびあいまいな名前解決を実装します。</span><span class="sxs-lookup"><span data-stu-id="7bc92-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="7bc92-120">完全な MAPI 制限言語を実装していないと表示名にのみ制限をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="7bc92-121">メッセージング ユーザーの詳細表示のテーブル。</span><span class="sxs-lookup"><span data-stu-id="7bc92-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="7bc92-122">1 回限りのアドレスです。</span><span class="sxs-lookup"><span data-stu-id="7bc92-122">One-off addresses.</span></span>
    
- <span data-ttu-id="7bc92-123">高度な検索] ダイアログ ボックスの場合。</span><span class="sxs-lookup"><span data-stu-id="7bc92-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="7bc92-124">[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="7bc92-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="7bc92-125">このインターフェイスは部分的にサポートされています。**IMAPIProp**メソッドは、 **IPropData**インターフェイスに委任されます。</span><span class="sxs-lookup"><span data-stu-id="7bc92-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="7bc92-126">詳細についてを参照してください、 [IPropData: IMAPIProp](ipropdataimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="7bc92-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="7bc92-127">インタラクティブおよびプログラマティックな構成です。</span><span class="sxs-lookup"><span data-stu-id="7bc92-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="7bc92-128">サポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="7bc92-128">Unsupported Features</span></span>

<span data-ttu-id="7bc92-129">このサンプルでは、次の機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7bc92-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="7bc92-130">並べ替えします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-130">Sorting.</span></span>
    
- <span data-ttu-id="7bc92-131">配布リストです。</span><span class="sxs-lookup"><span data-stu-id="7bc92-131">Distribution lists.</span></span>
    
- <span data-ttu-id="7bc92-132">作成、削除、およびエントリを変更します。</span><span class="sxs-lookup"><span data-stu-id="7bc92-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="7bc92-133">複数値を持つプロパティです。</span><span class="sxs-lookup"><span data-stu-id="7bc92-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="7bc92-134">名前付きプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7bc92-134">Named properties.</span></span>
    
- <span data-ttu-id="7bc92-135">表示名の最初と最後の名前を区別します。</span><span class="sxs-lookup"><span data-stu-id="7bc92-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="7bc92-136">**サンプルのアドレス帳プロバイダーをインストールするのには**</span><span class="sxs-lookup"><span data-stu-id="7bc92-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="7bc92-137">サンプルのアドレス帳プロバイダーをダウンロードするには、 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bc92-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="7bc92-138">Outlook MAPI サンプルを保存したフォルダーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="7bc92-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="7bc92-139">右クリックし、 **OutlookMAPISamples ・\<バージョン番号\>** フォルダーを zip し、[**すべて展開**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="7bc92-140">**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="7bc92-141">Visual Studio 2008年を実行します。</span><span class="sxs-lookup"><span data-stu-id="7bc92-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="7bc92-142">Visual Studio 2008 では、[**ファイル**] をクリックして、[**開いている**、および**プロジェクト/ソリューション**] をクリックし。</span><span class="sxs-lookup"><span data-stu-id="7bc92-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="7bc92-143">サンプルを保存する場所を参照する**SABP.vcproj**をクリックし、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="7bc92-144">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="7bc92-145">**ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="7bc92-146">サンプルを保存したフォルダーに**install.bat**ファイルを右クリックし、**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="7bc92-147">**ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="7bc92-148">**Install.bat**コピー .dll ファイルを既定の Microsoft Office のインストール フォルダー、C:\Program ファイル Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="7bc92-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="7bc92-149">別の場所に Office 製品をインストールした場合は、 **Install.bat**を右クリックし、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bc92-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="7bc92-150">ファイルがメモ帳で開きます。</span><span class="sxs-lookup"><span data-stu-id="7bc92-150">The file opens in Notepad.</span></span> <span data-ttu-id="7bc92-151">既定のインストール パスをお使いのコンピューターで使用されているインストール パスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="7bc92-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

