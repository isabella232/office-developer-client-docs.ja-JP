---
title: Excel ソフトウェア開発キットへようこそ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- 'excel 2007 xll software development kit,add-ins [Excel 2007] ms.prod: office-online-server localization_priority: Normal ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0'
localization_priority: Normal
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4de88a12b5fb945c6243e52b77babe88b2d02417
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798954"
---
# <a name="welcome-to-the-excel-software-development-kit"></a><span data-ttu-id="61678-104">Excel ソフトウェア開発キットへようこそ</span><span class="sxs-lookup"><span data-stu-id="61678-104">Welcome to the Excel Software Development Kit</span></span>

 <span data-ttu-id="61678-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="61678-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="61678-p101">Excel 2013 XLL ソフトウェア開発キット (SDK) ドキュメントへようこそ。このリファレンスには、Microsoft Excel 2013 XLL の開発に役立つ概要情報、プログラミング タスク、サンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="61678-p101">Welcome to the Excel 2013 XLL Software Development Kit (SDK) documentation. This reference contains conceptual overviews, programming tasks, and samples to help you develop Microsoft Excel 2013 XLLs.</span></span>
  
<span data-ttu-id="61678-108">更新: 2012 年 11 月</span><span class="sxs-lookup"><span data-stu-id="61678-108">Revised: November 2012</span></span>
  
<span data-ttu-id="61678-109">[Excel 2013 XLL SDK](http://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="61678-109">Download the [Excel 2013 XLL SDK](http://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span></span>
  
<span data-ttu-id="61678-110">Excel 2013 XLL SDK には、次が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61678-110">The Excel 2013 XLL SDK includes the following:</span></span>
  
- <span data-ttu-id="61678-111">**C アプリケーション プログラミング インターフェイス (API)**— DLL が Excel 2013 の機能にアクセスできるようにするヘッダー ファイルとソース ファイル、および Excel アドイン マネージャーと協働するために DLL が公開すべきインターフェイスの説明が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61678-111">**C application programming interface (API)**—Includes header and source files that enable DLLs to access Excel 2013 functionality, and a description of the interface that a DLL should expose to work with the Excel Add-in Manager.</span></span>
    
- <span data-ttu-id="61678-p102">**Microsoft Visual Studio プロジェクト**— C/C++ ソース コードが含まれ、C API の使用方法を示します。これらのサンプル プロジェクトには例が含まれ、独自のアドイン開発の開始点になります。</span><span class="sxs-lookup"><span data-stu-id="61678-p102">**Microsoft Visual Studio projects**—Includes C/C++ source code and shows how to use the C API. These sample projects provide examples and they serve as a starting point for your own add-in development.</span></span>
    
<span data-ttu-id="61678-114">SDK のドキュメントには、以下のセクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="61678-114">The SDK documentation contains the following sections:</span></span>
  
- [<span data-ttu-id="61678-115">Excel XLL SDK の概要</span><span class="sxs-lookup"><span data-stu-id="61678-115">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
    
- [<span data-ttu-id="61678-116">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="61678-116">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
    
- [<span data-ttu-id="61678-117">Excel クラスター コネクタの開発</span><span class="sxs-lookup"><span data-stu-id="61678-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
    
- [<span data-ttu-id="61678-118">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="61678-118">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a><span data-ttu-id="61678-119">対象外の機能</span><span class="sxs-lookup"><span data-stu-id="61678-119">Functionality Not Covered</span></span>

<span data-ttu-id="61678-120">次の内容は取り上げません。</span><span class="sxs-lookup"><span data-stu-id="61678-120">The following subjects are not covered:</span></span>
  
- <span data-ttu-id="61678-121">Excel マクロ (XML) シートのユーザー定義関数とコマンドの開発。</span><span class="sxs-lookup"><span data-stu-id="61678-121">Developing user-defined functions and commands in Excel macro (XLM) sheets.</span></span>
    
- <span data-ttu-id="61678-122">XML マクロの実行の流れを制御する DLL のユーザー定義関数の作成。</span><span class="sxs-lookup"><span data-stu-id="61678-122">Creating user-defined functions in DLLs that control the flow of execution of an XLM macro.</span></span>
    
    <span data-ttu-id="61678-123">そのような関数は特別なフロー制御のデータ型を返すことで機能しますが、これについてもこのドキュメントでは説明しません。</span><span class="sxs-lookup"><span data-stu-id="61678-123">Such functions work by returning a special flow control data type, which is also not described in this documentation.</span></span>
    
## <a name="related-links"></a><span data-ttu-id="61678-124">関連リンク</span><span class="sxs-lookup"><span data-stu-id="61678-124">Related Links</span></span>

[<span data-ttu-id="61678-125">Excel デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="61678-125">Excel Developer Center</span></span>](http://msdn.microsoft.com/ja-JP/office/aa905411.aspx)
  
[<span data-ttu-id="61678-126">Microsoft Office デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="61678-126">Microsoft Office Developer Center</span></span>](http://msdn.microsoft.com/ja-JP/office/default.aspx)
  
[<span data-ttu-id="61678-127">Excel 2010 SDK: Excel 2010 XLL ソフトウェア開発キット</span><span class="sxs-lookup"><span data-stu-id="61678-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span></span>](http://go.microsoft.com/fwlink/?LinkID=186435&amp;clcid=0x409)
  

