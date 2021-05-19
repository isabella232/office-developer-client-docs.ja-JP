---
title: アドレス帳プロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331109"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="f35b4-103">アドレス帳プロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="f35b4-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="f35b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f35b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f35b4-105">このサンプルでは、フラット バイナリ ファイルから読み取る表示名と電子メール アドレスの読み取り専用コンテナーが 1 つサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f35b4-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="f35b4-106">このサンプルでは、プロファイル ウィザード以外の 1 回きりテンプレートとすべての構成オプションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f35b4-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="f35b4-107">このサンプルは、メッセージング[API (MAPI) Outlookサンプルからダウンロードできます](https://go.microsoft.com/fwlink/?LinkId=129740
)。</span><span class="sxs-lookup"><span data-stu-id="f35b4-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f35b4-108">実行可能ファイル:</span><span class="sxs-lookup"><span data-stu-id="f35b4-108">Executable:</span></span>  <br/> |<span data-ttu-id="f35b4-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="f35b4-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="f35b4-110">ソース コード ディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="f35b4-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="f35b4-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="f35b4-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="f35b4-112">言語:</span><span class="sxs-lookup"><span data-stu-id="f35b4-112">Language:</span></span>  <br/> |<span data-ttu-id="f35b4-113">C++</span><span class="sxs-lookup"><span data-stu-id="f35b4-113">C++</span></span>  <br/> |
|<span data-ttu-id="f35b4-114">プラットフォーム:</span><span class="sxs-lookup"><span data-stu-id="f35b4-114">Platforms:</span></span>  <br/> |<span data-ttu-id="f35b4-115">Microsoft Visual Studio Vista、Windows Windows Server 2008、Windows XP SP2、Windows Server 2003 SP1 用にコンパイルする 2008</span><span class="sxs-lookup"><span data-stu-id="f35b4-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="f35b4-116">サポートされている機能</span><span class="sxs-lookup"><span data-stu-id="f35b4-116">Supported Features</span></span>

<span data-ttu-id="f35b4-117">このサンプルでは、次の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f35b4-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="f35b4-118">テーブルの制限。</span><span class="sxs-lookup"><span data-stu-id="f35b4-118">Table restrictions.</span></span> <span data-ttu-id="f35b4-119">このサンプルでは、プレフィックス一致とあいまいな名前解決を実装します。</span><span class="sxs-lookup"><span data-stu-id="f35b4-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="f35b4-120">MAPI の完全な制限言語は実装されません。制限は表示名でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f35b4-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="f35b4-121">メッセージング ユーザーの詳細表示テーブル。</span><span class="sxs-lookup"><span data-stu-id="f35b4-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="f35b4-122">1 回のアドレス。</span><span class="sxs-lookup"><span data-stu-id="f35b4-122">One-off addresses.</span></span>
    
- <span data-ttu-id="f35b4-123">高度な検索ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="f35b4-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="f35b4-124">[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="f35b4-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="f35b4-125">このインターフェイスは部分的にサポートされています。 **IMAPIProp** メソッドは **IPropData インターフェイスに委任** されます。</span><span class="sxs-lookup"><span data-stu-id="f35b4-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="f35b4-126">詳細については [、「IPropData : IMAPIProp インターフェイス」を参照](ipropdataimapiprop.md) してください。</span><span class="sxs-lookup"><span data-stu-id="f35b4-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="f35b4-127">対話型およびプログラムによる構成。</span><span class="sxs-lookup"><span data-stu-id="f35b4-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="f35b4-128">サポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="f35b4-128">Unsupported Features</span></span>

<span data-ttu-id="f35b4-129">このサンプルでは、次の機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f35b4-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="f35b4-130">並べ替え。</span><span class="sxs-lookup"><span data-stu-id="f35b4-130">Sorting.</span></span>
    
- <span data-ttu-id="f35b4-131">配布リスト。</span><span class="sxs-lookup"><span data-stu-id="f35b4-131">Distribution lists.</span></span>
    
- <span data-ttu-id="f35b4-132">エントリの作成、削除、および変更。</span><span class="sxs-lookup"><span data-stu-id="f35b4-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="f35b4-133">複数の値を持つプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f35b4-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="f35b4-134">名前付きプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f35b4-134">Named properties.</span></span>
    
- <span data-ttu-id="f35b4-135">表示名の名と名を区別します。</span><span class="sxs-lookup"><span data-stu-id="f35b4-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="f35b4-136">**サンプル アドレス帳プロバイダーをインストールするには**</span><span class="sxs-lookup"><span data-stu-id="f35b4-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="f35b4-137">サンプル アドレス帳プロバイダーをダウンロードするには、「MAPI サンプルのダウンロード[Outlookを参照してください](downloading-the-outlook-mapi-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="f35b4-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="f35b4-138">MAPI サンプルに保存したフォルダー Outlook探します。</span><span class="sxs-lookup"><span data-stu-id="f35b4-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="f35b4-139">**OutlookMAPISamples- バージョン \< \>** 番号 zip フォルダーを右クリックし、[すべて抽出]**をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="f35b4-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="f35b4-140">[ **参照] を** クリックし、サンプルを保存する場所を選択し、[抽出] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="f35b4-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="f35b4-141">2008 Visual Studioを実行します。</span><span class="sxs-lookup"><span data-stu-id="f35b4-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="f35b4-142">[Visual Studio 2008 で、[ファイル] を **クリック** し、[開く]**を選択し**、[Project/**ソリューション] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="f35b4-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="f35b4-143">サンプルを保存した場所を参照し **、[SABP.vcproj]** をクリックし、[開く] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="f35b4-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="f35b4-144">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f35b4-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="f35b4-145">[ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。</span><span class="sxs-lookup"><span data-stu-id="f35b4-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="f35b4-146">サンプルを保存したフォルダーで、ファイルを右クリックし、[管理者として **install.batを\*\*\*\*クリックします**。</span><span class="sxs-lookup"><span data-stu-id="f35b4-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="f35b4-147">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f35b4-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f35b4-148">**Install.bat** を既定.dll Microsoft Officeインストール フォルダー C:\Program Files\Microsoft Office\Office12 にコピーします。\.</span><span class="sxs-lookup"><span data-stu-id="f35b4-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="f35b4-149">別の場所にOffice製品をインストールしている場合は、[編集] をInstall.bat **クリック\*\*\*\*します**。</span><span class="sxs-lookup"><span data-stu-id="f35b4-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="f35b4-150">ファイルが [ファイル] ウィンドウメモ帳。</span><span class="sxs-lookup"><span data-stu-id="f35b4-150">The file opens in Notepad.</span></span> <span data-ttu-id="f35b4-151">既定のインストール パスを、コンピューターで使用されるインストール パスに置き換える。</span><span class="sxs-lookup"><span data-stu-id="f35b4-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

