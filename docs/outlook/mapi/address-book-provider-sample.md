---
title: アドレス帳プロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331109"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="5ab1a-103">アドレス帳プロバイダーのサンプル</span><span class="sxs-lookup"><span data-stu-id="5ab1a-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="5ab1a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ab1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ab1a-105">このサンプルでは、表示名と電子メールアドレス用の単一の読み取り専用コンテナーをサポートしています。これは、フラットなバイナリファイルから読み取られます。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="5ab1a-106">サンプルでは、プロファイルウィザードを除く、1回限りのテンプレートとすべての構成オプションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="5ab1a-107">このサンプルは、 [Outlook Messaging API (MAPI) コードサンプル](https://go.microsoft.com/fwlink/?LinkId=129740
)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ab1a-108">実行可能</span><span class="sxs-lookup"><span data-stu-id="5ab1a-108">Executable:</span></span>  <br/> |<span data-ttu-id="5ab1a-109">SABP32</span><span class="sxs-lookup"><span data-stu-id="5ab1a-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="5ab1a-110">ソースコードディレクトリ:</span><span class="sxs-lookup"><span data-stu-id="5ab1a-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="5ab1a-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="5ab1a-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="5ab1a-112">言語</span><span class="sxs-lookup"><span data-stu-id="5ab1a-112">Language:</span></span>  <br/> |<span data-ttu-id="5ab1a-113">+</span><span class="sxs-lookup"><span data-stu-id="5ab1a-113">C++</span></span>  <br/> |
|<span data-ttu-id="5ab1a-114">対象</span><span class="sxs-lookup"><span data-stu-id="5ab1a-114">Platforms:</span></span>  <br/> |<span data-ttu-id="5ab1a-115">windows Vista、windows server 2008、windows XP SP2、および windows server 2003 SP1 用にコンパイルする Microsoft Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="5ab1a-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="5ab1a-116">サポートされる機能</span><span class="sxs-lookup"><span data-stu-id="5ab1a-116">Supported Features</span></span>

<span data-ttu-id="5ab1a-117">この例では、次の機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="5ab1a-118">表の制限</span><span class="sxs-lookup"><span data-stu-id="5ab1a-118">Table restrictions.</span></span> <span data-ttu-id="5ab1a-119">この例では、プレフィックスとあいまいな名前の解決を実装しています。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="5ab1a-120">完全な MAPI 制限言語を実装するわけではなく、表示名でのみ制限がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="5ab1a-121">メッセージングユーザーの詳細表示テーブル。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="5ab1a-122">1回限りの住所。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-122">One-off addresses.</span></span>
    
- <span data-ttu-id="5ab1a-123">[高度な検索] ダイアログボックス</span><span class="sxs-lookup"><span data-stu-id="5ab1a-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="5ab1a-124">[imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="5ab1a-125">このインターフェイスは部分的にサポートされています。**imapiprop**メソッドは、 **ipropdata**インターフェイスに委任されます。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="5ab1a-126">詳細については、 [ipropdata: imapiprop](ipropdataimapiprop.md)インターフェイスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="5ab1a-127">対話型およびプログラムによる構成。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="5ab1a-128">サポートされない機能</span><span class="sxs-lookup"><span data-stu-id="5ab1a-128">Unsupported Features</span></span>

<span data-ttu-id="5ab1a-129">このサンプルでは、次の機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="5ab1a-130">替え.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-130">Sorting.</span></span>
    
- <span data-ttu-id="5ab1a-131">配布リスト。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-131">Distribution lists.</span></span>
    
- <span data-ttu-id="5ab1a-132">エントリの作成、削除、変更。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="5ab1a-133">複数の値を持つプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="5ab1a-134">名前付きプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-134">Named properties.</span></span>
    
- <span data-ttu-id="5ab1a-135">表示名の最初と最後の名前を区別します。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="5ab1a-136">**サンプルアドレス帳プロバイダーをインストールするには**</span><span class="sxs-lookup"><span data-stu-id="5ab1a-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="5ab1a-137">サンプルのアドレス帳プロバイダーをダウンロードするには、「 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="5ab1a-138">Outlook MAPI サンプルを保存したフォルダーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="5ab1a-139">**OutlookMAPISamples-\<version\>番号**の zip フォルダーを右クリックし、[**すべて抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="5ab1a-140">[**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="5ab1a-141">Visual Studio 2008 を実行します。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="5ab1a-142">Visual Studio 2008 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="5ab1a-143">サンプルを保存した場所を参照し、[ **SABP**] をクリックして、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="5ab1a-144">[ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="5ab1a-145">[名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="5ab1a-146">サンプルを保存したフォルダーで、**インストールする .bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="5ab1a-147">[**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5ab1a-148">**.bat をインストール**すると、.dll は既定の Microsoft Office インストールフォルダーである C:\Program C:\Program Office\Office12 にコピーされます。\.</span><span class="sxs-lookup"><span data-stu-id="5ab1a-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="5ab1a-149">別の場所に Office 製品をインストールした場合は、[**インストール**] を右クリックし、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="5ab1a-150">ファイルがメモ帳で開きます。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-150">The file opens in Notepad.</span></span> <span data-ttu-id="5ab1a-151">既定のインストールパスを、コンピューターで使用されているインストールパスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5ab1a-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

