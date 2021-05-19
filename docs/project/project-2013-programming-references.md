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
- プロジェクト サーバー インターフェイス、Project Server、エラー コード、VBA、Project オブジェクト モデル、Project 2013、プラットフォーム、Visual Basic for Applications、Project オブジェクト モデル、オブジェクト モデル、Project VBA、Project Server、PSI リファレンス、PSI
localization_priority: Normal
ms.assetid: 79c78c44-1e08-4c9b-a7fe-a5089e666055
description: Project Server Interface (PSI) リファレンスの概要、ASMX インターフェイスと PSI の WCF インターフェイスの使い方、Project Server エラー コードに関する情報、および ProjectData OData サービスの参照について説明します。
ms.openlocfilehash: 27b2eb27d62ec1abdb1a835b5d874e211e7e793e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357037"
---
# <a name="project-2013-programming-references"></a><span data-ttu-id="5bbc8-104">Project 2013 プログラミング リファレンス</span><span class="sxs-lookup"><span data-stu-id="5bbc8-104">Project 2013 programming references</span></span>

<span data-ttu-id="5bbc8-105">Project Server インターフェイス (PSI) リファレンスの概要、ASMX インターフェイスと PSI の WCF インターフェイスの使い方、Project Server エラー コードに関する情報、および **ProjectData** OData サービスの参照について説明します。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-105">Find an overview of the Project Server Interface (PSI) reference, how to use the ASMX interface and the WCF interface of the PSI, information about Project Server error codes, and a reference for the **ProjectData** OData service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5bbc8-106">Project Server 2013 の PSI およびクライアント側オブジェクト モデル (CSOM) の主な参照については、Project [Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md)のクラス ライブラリと[Web](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx)サービスリファレンスと JavaScript API リファレンスのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-106">For the primary references for the PSI and the client-side object model (CSOM) in Project Server 2013, see the following sections: [Class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) and [JavaScript API reference for Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md).</span></span> <span data-ttu-id="5bbc8-107">> Office 2013 作業ウィンドウ アプリの Java Project Script リファレンスを含む Office アドインリファレンスについては[、「JavaScript API for Office」を参照してください](https://msdn.microsoft.com/library/fp142185.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-107">> For the Office Add-ins references, which include the JavaScript reference for Project 2013 task pane apps, see [JavaScript API for Office](https://msdn.microsoft.com/library/fp142185.aspx).</span></span> <span data-ttu-id="5bbc8-108">> 2013 および Project Standard Project Professional 2013 の VBA リファレンスについては、「Project VBA 開発者向けリファレンス」を[参照してください](https://msdn.microsoft.com/library/jj235035.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-108">> For the VBA reference for Project Standard 2013 and Project Professional 2013, see [Project 2013 VBA developer reference](https://msdn.microsoft.com/library/jj235035.aspx).</span></span> <span data-ttu-id="5bbc8-109">> サーバー 2013 データベース内のレポート テーブルとビュー Project参照はまだ使用できません。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-109">> The reference for the reporting tables and views in the on-premises Project Server 2013 database is not yet available.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="5bbc8-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="5bbc8-110">In this section</span></span>

<span data-ttu-id="5bbc8-111">[Project PSI リファレンスの概要](project-psi-reference-overview.md)サーバー 2013 の PSI リファレンスのアセンブリと名前空間Project説明します。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-111">[Project PSI reference overview](project-psi-reference-overview.md) Describes the assemblies and namespaces in the PSI reference for Project Server 2013.</span></span> 
  
<span data-ttu-id="5bbc8-112">[ASMX ベースのコード サンプルの前提条件をProject](prerequisites-for-asmx-based-code-samples-in-project.md)テスト アプリケーションで ASMX Web サービスを使用して構築された PSI リファレンスでコード サンプルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-112">[Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using ASMX web services in your test applications.</span></span> 
  
<span data-ttu-id="5bbc8-113">[WCF ベースのコード サンプルの前提条件 (Project](prerequisites-for-wcf-based-code-samples-in-project.md)テスト アプリケーションで通信ファンデーション (WCF) サービスを使用Windows PSI リファレンスでコード サンプルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-113">[Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using Windows Communication Foundation (WCF) services in your test applications.</span></span> 
  
<span data-ttu-id="5bbc8-114">[Projectサーバーのエラー コード](project-server-error-codes.md)サーバー エラーのコードと説明をProject機能領域別に一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-114">[Project Server error codes](project-server-error-codes.md) Lists the codes and descriptions of Project Server errors by functional area.</span></span> 
  
<span data-ttu-id="5bbc8-115">[ProjectData - OData Project OData サービス参照](https://msdn.microsoft.com/library/office/jj163015.aspx)Project Server レポート データの OData サービスの概要、LINQ クエリでの OData フィードの使用の概要、**および ProjectData** サービスの XML メタデータの参照が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5bbc8-115">[ProjectData - Project OData service reference](https://msdn.microsoft.com/library/office/jj163015.aspx) Includes an overview of the OData service for Project Server reporting data, an introduction to using the OData feeds with LINQ queries, and references for the XML metadata in the **ProjectData** service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5bbc8-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="5bbc8-116">See also</span></span>



[<span data-ttu-id="5bbc8-117">JavaScript API for Office</span><span class="sxs-lookup"><span data-stu-id="5bbc8-117">JavaScript API for Office</span></span>](https://msdn.microsoft.com/library/fp142185.aspx)
  
[<span data-ttu-id="5bbc8-118">Project 2013 VBA 開発者向けリファレンス</span><span class="sxs-lookup"><span data-stu-id="5bbc8-118">Project 2013 VBA developer reference</span></span>](https://msdn.microsoft.com/library/jj235035.aspx)

