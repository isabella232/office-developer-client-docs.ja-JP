---
title: JavaScript ライブラリとプロジェクトのサーバーの残りの部分参照
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: JavaScript ライブラリと残りの部分参照は、Project Server 2013 には、JavaScript オブジェクト モデルおよび Project Server の機能にアクセスするために使用する REST インターフェイスに関する情報が含まれています。 これらの Api を使用すると、ブラウザー間の web アプリケーション、プロジェクトの評価のためのアドインの場合、および Project Server 2013 とオンラインのプロジェクトにアクセスする Windows 以外のデバイス用のアプリケーションを開発します。
ms.openlocfilehash: f834ffdc80de28eceb2d7ab9b30c1444b0478bd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804567"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a><span data-ttu-id="eaeb0-104">JavaScript ライブラリとプロジェクトのサーバーの残りの部分参照</span><span class="sxs-lookup"><span data-stu-id="eaeb0-104">JavaScript library and REST reference for Project Server</span></span>

<span data-ttu-id="eaeb0-105">JavaScript ライブラリと残りの部分参照は、Project Server 2013 には、JavaScript オブジェクト モデルおよび Project Server の機能にアクセスするために使用する REST インターフェイスに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-105">The JavaScript library and REST reference for Project Server 2013 contains information about the JavaScript object model and the REST interface that you use to access Project Server functionality.</span></span> <span data-ttu-id="eaeb0-106">これらの Api を使用すると、ブラウザー間の web アプリケーション、プロジェクトの評価のためのアドインの場合、および Project Server 2013 とオンラインのプロジェクトにアクセスする Windows 以外のデバイス用のアプリケーションを開発します。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-106">You can use these APIs to develop cross-browser web apps, Project Professional 2013 add-ins, and apps for non-Windows devices that access Project Server 2013 and Project Online.</span></span>
  
> [!NOTE]
> <span data-ttu-id="eaeb0-107">JavaScript オブジェクト モデルと REST インターフェイスは、Project Server のクライアント側オブジェクト モデル (CSOM) に沿って配置します。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-107">The JavaScript object model and REST interface align with the Project Server client-side object model (CSOM).</span></span> <span data-ttu-id="eaeb0-108">CSOM で**Microsoft.ProjectServer.Client**の名前空間と同等の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-108">They provide equivalent functionality to the **Microsoft.ProjectServer.Client** namespace in the CSOM.</span></span> 
  
<span data-ttu-id="eaeb0-109">Project Server の機能をアクセスするには、JavaScript オブジェクト モデルを通じて、 [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)の名前空間で定義されている、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js`ファイルです。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-109">You can access Project Server functionality through the JavaScript object model, which is defined in the [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) namespace in the  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` file.</span></span> <span data-ttu-id="eaeb0-110">[PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)名前空間内の[ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx)オブジェクトは、JavaScript オブジェクト モデルへのエントリ ポイントです。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-110">The [ProjectContext](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) object in the [PS](http://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) namespace is the entry point to the JavaScript object model.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eaeb0-111">JavaScript オブジェクト モデルを参照して、デバッグに役立つように、同じディレクトリに PS.debug.js ファイルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-111">To browse the JavaScript object model and to help with debugging, you can use the PS.debug.js file in the same directory.</span></span> <span data-ttu-id="eaeb0-112">[Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435)ではリモート コンピューター上の開発を支援するため、CSOM および PS.js と PS.debug.js ファイルの.NET Framework アセンブリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-112">To help with development on a remote computer, the [Project 2013 SDK download](https://www.microsoft.com/en-us/download/details.aspx?id=30435) includes the .NET Framework assemblies for the CSOM, and the PS.js and PS.debug.js files.</span></span> 
  
<span data-ttu-id="eaeb0-113">REST インターフェイスで Project Server の機能をアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-113">You can also access Project Server functionality through the REST interface.</span></span> <span data-ttu-id="eaeb0-114">REST インターフェイスへのエントリ ポイントでは、 **ProjectServer**リソースを使用してアクセスすることが、`http://ServerName/pwaName/_api/ProjectServer`エンドポイントの URI です。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-114">The entry point to the REST interface is the **ProjectServer** resource, which you access by using the  `http://ServerName/pwaName/_api/ProjectServer` endpoint URI.</span></span> <span data-ttu-id="eaeb0-115">次のクエリが指定されたプロジェクト内の割り当てを取得するなど、(_サーバー名_と_pwaName_を交換し、プロジェクトに一致する GUID を変更) します。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-115">For example, the following query gets the assignments in the specified project (replace  _ServerName_ and  _pwaName_, and change the GUID to match a project).</span></span>
  
`http://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

<span data-ttu-id="eaeb0-116">**ProjectServer**リソースには、 [REST インターフェイスでは、ProjectServer リソース](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources)が記載されています。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-116">The **ProjectServer** resource is described in [ProjectServer resources in the REST interface](http://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources).</span></span> <span data-ttu-id="eaeb0-117">他の REST リソースは、対応する JavaScript オブジェクトとメンバーでは、この参照のマニュアルで説明します。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-117">Other REST resources are described in the documentation for the corresponding JavaScript objects and members in this reference.</span></span> <span data-ttu-id="eaeb0-118">残りの部分の使用に関する詳細については、 [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)と[SharePoint 2013 の REST サービスを使用してプログラミング](http://msdn.microsoft.com/ja-jp/library/fp142385%28office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-118">For more information about using REST, see [Client-side object model (CSOM) for Project Server](client-side-object-model-csom-for-project-2013.md) and [Programming using the SharePoint 2013 REST service](http://msdn.microsoft.com/ja-jp/library/fp142385%28office.15%29.aspx).</span></span>
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a><span data-ttu-id="eaeb0-119">JavaScript ライブラリとプロジェクトのサーバーの残りの部分参照</span><span class="sxs-lookup"><span data-stu-id="eaeb0-119">JavaScript library and REST reference for Project Server</span></span>
<span data-ttu-id="eaeb0-120"><a name="pj15_JavaScriptAPIReference_PS"> </a></span><span class="sxs-lookup"><span data-stu-id="eaeb0-120"></span></span>

- <span data-ttu-id="eaeb0-121">[PS.js JavaScript ライブラリおよび他の参照](http://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx)Project Server 2013 の JavaScript オブジェクト モデルと REST インターフェイスに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-121">[PS.js JavaScript library and REST reference](http://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Contains information about the JavaScript object model and the REST interface for Project Server 2013.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="eaeb0-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="eaeb0-122">See also</span></span>
<span data-ttu-id="eaeb0-123"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="eaeb0-123"></span></span>

- [<span data-ttu-id="eaeb0-124">Project 2013 開発者向けドキュメント</span><span class="sxs-lookup"><span data-stu-id="eaeb0-124">Project 2013 developer documentation</span></span>](project-2013-developer-documentation.md)   
- [<span data-ttu-id="eaeb0-125">Project Server のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="eaeb0-125">Client-side object model (CSOM) for Project Server</span></span>](client-side-object-model-csom-for-project-2013.md)   
- [<span data-ttu-id="eaeb0-126">JavaScript オブジェクト モデルの概要</span><span class="sxs-lookup"><span data-stu-id="eaeb0-126">Getting started with the JavaScript object model</span></span>](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [<span data-ttu-id="eaeb0-127">JavaScript オブジェクト モデルを使用してプロジェクトの作業します。</span><span class="sxs-lookup"><span data-stu-id="eaeb0-127">Work with projects by using the JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

