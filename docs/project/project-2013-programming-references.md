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
- プロジェクト サーバー インターフェイスでは、Project Server では、エラー コード、VBA プロジェクト オブジェクト モデルでは、Project 2013 では、プラットフォーム、プロジェクト オブジェクト モデルでは、Visual Basic for Applications オブジェクト モデルでは、VBA のプロジェクト、プロジェクトのサーバー、PSI リファレンス、PSI
localization_priority: Normal
ms.assetid: 79c78c44-1e08-4c9b-a7fe-a5089e666055
description: プロジェクト Server インターフェイス (PSI) の参照の概要を説明 ProjectData OData サービスの ASMX インターフェイスおよび WCF インターフェイスの PSI、Project Server のエラー コードに関する情報、および参照を使用する方法です。
ms.openlocfilehash: 8e2ee8730e737408899b6fe26ce55210e0c68e81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19804675"
---
# <a name="project-2013-programming-references"></a><span data-ttu-id="e8545-104">Project 2013 プログラミング リファレンス</span><span class="sxs-lookup"><span data-stu-id="e8545-104">Project 2013 programming references</span></span>

<span data-ttu-id="e8545-105">プロジェクト Server インターフェイス (PSI) の参照の概要を説明**ProjectData** OData サービスの ASMX インターフェイスおよび WCF インターフェイスの PSI、Project Server のエラー コードに関する情報、および参照を使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="e8545-105">Find an overview of the Project Server Interface (PSI) reference, how to use the ASMX interface and the WCF interface of the PSI, information about Project Server error codes, and a reference for the **ProjectData** OData service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e8545-106">PSI および Project Server 2013 のクライアント側オブジェクト モデル (CSOM) のプライマリ参照、次のセクションを参照してください:[クラス ライブラリと web サービスを参照](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)し、 [Project Server 2013 の JavaScript API リファレンス](javascript-library-and-rest-reference-for-project-server-2013.md)です。</span><span class="sxs-lookup"><span data-stu-id="e8545-106">For the primary references for the PSI and the client-side object model (CSOM) in Project Server 2013, see the following sections: [Class library and web service reference](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) and [JavaScript API reference for Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md).</span></span> <span data-ttu-id="e8545-107">> Project 2013 の作業ウィンドウ アプリの JavaScript の参照を含めるには、Office アドインの参照には、 [Office 用の JavaScript API](http://msdn.microsoft.com/ja-jp/library/fp142185.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8545-107">> For the Office Add-ins references, which include the JavaScript reference for Project 2013 task pane apps, see [JavaScript API for Office](http://msdn.microsoft.com/ja-jp/library/fp142185.aspx).</span></span> <span data-ttu-id="e8545-108">> リファレンスについては、VBA プロジェクトの標準的な 2013 および評価のためのプロジェクトの[VBA の Project 2013 開発者用リファレンス](http://msdn.microsoft.com/ja-jp/library/jj235035.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8545-108">> For the VBA reference for Project Standard 2013 and Project Professional 2013, see [Project 2013 VBA developer reference](http://msdn.microsoft.com/ja-jp/library/jj235035.aspx).</span></span> <span data-ttu-id="e8545-109">> レポートのテーブルと、オンプレミスの Project Server 2013 のデータベース内のビューへの参照はまだ利用可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="e8545-109">> The reference for the reporting tables and views in the on-premises Project Server 2013 database is not yet available.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="e8545-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="e8545-110">In this section</span></span>

<span data-ttu-id="e8545-111">[プロジェクトの PSI リファレンスの概要](project-psi-reference-overview.md)Project Server 2013 の PSI 参照内の名前空間とアセンブリを説明します。</span><span class="sxs-lookup"><span data-stu-id="e8545-111">[Project PSI reference overview](project-psi-reference-overview.md) Describes the assemblies and namespaces in the PSI reference for Project Server 2013.</span></span> 
  
<span data-ttu-id="e8545-112">[プロジェクト内の ASMX ベースのコード サンプルの前提条件](prerequisites-for-asmx-based-code-samples-in-project.md)テスト アプリケーションの ASMX web サービスを使用して組み込まれている PSI リファレンスのコード サンプルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8545-112">[Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using ASMX web services in your test applications.</span></span> 
  
<span data-ttu-id="e8545-113">[プロジェクト内の WCF ベースのコード サンプルの前提条件](prerequisites-for-wcf-based-code-samples-in-project.md)テスト アプリケーションで Windows Communication Foundation (WCF) サービスを使用して組み込まれている PSI リファレンスのコード サンプルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8545-113">[Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using Windows Communication Foundation (WCF) services in your test applications.</span></span> 
  
<span data-ttu-id="e8545-114">[Project Server のエラー コード](project-server-error-codes.md)コードと機能領域で Project Server のエラーの説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8545-114">[Project Server error codes](project-server-error-codes.md) Lists the codes and descriptions of Project Server errors by functional area.</span></span> 
  
<span data-ttu-id="e8545-115">[ProjectData - プロジェクトの OData サービスの参照](https://msdn.microsoft.com/ja-jp/library/office/jj163015.aspx)**ProjectData**サービス内の XML メタデータの OData フィードを使用して LINQ クエリでは、参照の概要レポートのデータを Project Server の OData サービスの概要が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e8545-115">[ProjectData - Project OData service reference](https://msdn.microsoft.com/ja-jp/library/office/jj163015.aspx) Includes an overview of the OData service for Project Server reporting data, an introduction to using the OData feeds with LINQ queries, and references for the XML metadata in the **ProjectData** service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8545-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8545-116">See also</span></span>



[<span data-ttu-id="e8545-117">JavaScript API for Office</span><span class="sxs-lookup"><span data-stu-id="e8545-117">JavaScript API for Office</span></span>](http://msdn.microsoft.com/ja-jp/library/fp142185.aspx)
  
[<span data-ttu-id="e8545-118">Project 2013 VBA 開発者用リファレンス</span><span class="sxs-lookup"><span data-stu-id="e8545-118">Project 2013 VBA developer reference</span></span>](http://msdn.microsoft.com/ja-jp/library/jj235035.aspx)

