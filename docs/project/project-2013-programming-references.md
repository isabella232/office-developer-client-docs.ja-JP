---
title: Project 2013 プログラミング リファレンス
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- object model
- Project Server errors
- Project VBA
- PSI
- PSI reference
- VBA
- VBA object model
keywords:
- project server interface、project server、error コード、VBA、project オブジェクトモデル、プロジェクト2013、プラットフォーム、Visual Basic for Applications、project オブジェクトモデル、オブジェクトモデル、プロジェクト VBA、project server、psi 参照、psi
localization_priority: Normal
ms.assetid: 79c78c44-1e08-4c9b-a7fe-a5089e666055
description: project server Interface (psi) リファレンスの概要、ASMX インターフェイスおよび psi の WCF インターフェイスの使用方法、Project Server のエラーコードに関する情報、projectdata OData サービスのリファレンスを紹介します。
ms.openlocfilehash: 27b2eb27d62ec1abdb1a835b5d874e211e7e793e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357037"
---
# <a name="project-2013-programming-references"></a><span data-ttu-id="0bb59-104">Project 2013 プログラミング リファレンス</span><span class="sxs-lookup"><span data-stu-id="0bb59-104">Project 2013 programming references</span></span>

<span data-ttu-id="0bb59-105">project server Interface (psi) リファレンスの概要、ASMX インターフェイスおよび psi の WCF インターフェイスの使用方法、Project Server のエラーコードに関する情報、 **projectdata** OData サービスのリファレンスを紹介します。</span><span class="sxs-lookup"><span data-stu-id="0bb59-105">Find an overview of the Project Server Interface (PSI) reference, how to use the ASMX interface and the WCF interface of the PSI, information about Project Server error codes, and a reference for the **ProjectData** OData service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0bb59-106">project server 2013 の PSI およびクライアント側オブジェクトモデル (csom) のプライマリ参照については、以下のセクションを参照してください。「 [Class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) 」および「 [JavaScript API reference for project server 2013](javascript-library-and-rest-reference-for-project-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bb59-106">For the primary references for the PSI and the client-side object model (CSOM) in Project Server 2013, see the following sections: [Class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) and [JavaScript API reference for Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md).</span></span> <span data-ttu-id="0bb59-107">> office アドインの参照 (プロジェクト2013の作業ウィンドウアプリの javascript リファレンスを含む) については、「 [javascript API for Office](https://msdn.microsoft.com/library/fp142185.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bb59-107">> For the Office Add-ins references, which include the JavaScript reference for Project 2013 task pane apps, see [JavaScript API for Office](https://msdn.microsoft.com/library/fp142185.aspx).</span></span> <span data-ttu-id="0bb59-108">> project Standard 2013 および project Professional 2013 の vba リファレンスについては、「 [project 2013 VBA 開発者用リファレンス](https://msdn.microsoft.com/library/jj235035.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bb59-108">> For the VBA reference for Project Standard 2013 and Project Professional 2013, see [Project 2013 VBA developer reference](https://msdn.microsoft.com/library/jj235035.aspx).</span></span> <span data-ttu-id="0bb59-109">> オンプレミスの Project Server 2013 データベースのレポートテーブルとビューの参照はまだ使用できません。</span><span class="sxs-lookup"><span data-stu-id="0bb59-109">> The reference for the reporting tables and views in the on-premises Project Server 2013 database is not yet available.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0bb59-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="0bb59-110">In this section</span></span>

<span data-ttu-id="0bb59-111">[プロジェクト PSI リファレンスの概要](project-psi-reference-overview.md)Project Server 2013 の PSI リファレンスのアセンブリと名前空間について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bb59-111">[Project PSI reference overview](project-psi-reference-overview.md) Describes the assemblies and namespaces in the PSI reference for Project Server 2013.</span></span> 
  
<span data-ttu-id="0bb59-112">[プロジェクトの ASMX ベースのコードサンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)テストアプリケーションで ASMX web サービスを使用して構築された PSI 参照でコードサンプルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bb59-112">[Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using ASMX web services in your test applications.</span></span> 
  
<span data-ttu-id="0bb59-113">[Project の WCF ベースのコードサンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)テストアプリケーションで Windows Communication Foundation (WCF) サービスを使用して構築された PSI リファレンスでコードサンプルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bb59-113">[Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using Windows Communication Foundation (WCF) services in your test applications.</span></span> 
  
<span data-ttu-id="0bb59-114">[Project Server のエラーコード](project-server-error-codes.md)機能領域別の Project Server エラーのコードと説明を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0bb59-114">[Project Server error codes](project-server-error-codes.md) Lists the codes and descriptions of Project Server errors by functional area.</span></span> 
  
<span data-ttu-id="0bb59-115">[projectdata-Project OData サービスリファレンス](https://msdn.microsoft.com/library/office/jj163015.aspx)Project Server レポートデータの odata サービスの概要、LINQ クエリでの odata フィードの使用方法、および**projectdata**サービスの XML メタデータの参照について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bb59-115">[ProjectData - Project OData service reference](https://msdn.microsoft.com/library/office/jj163015.aspx) Includes an overview of the OData service for Project Server reporting data, an introduction to using the OData feeds with LINQ queries, and references for the XML metadata in the **ProjectData** service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0bb59-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bb59-116">See also</span></span>



[<span data-ttu-id="0bb59-117">JavaScript API for Office</span><span class="sxs-lookup"><span data-stu-id="0bb59-117">JavaScript API for Office</span></span>](https://msdn.microsoft.com/library/fp142185.aspx)
  
[<span data-ttu-id="0bb59-118">Project 2013 VBA 開発者用リファレンス</span><span class="sxs-lookup"><span data-stu-id="0bb59-118">Project 2013 VBA developer reference</span></span>](https://msdn.microsoft.com/library/jj235035.aspx)

