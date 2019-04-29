---
title: サンプルプロバイダテンプレートを適用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'サンプルの Outlook Social Connector (.osc) プロバイダテンプレートには、.osc プロバイダーを実装するためのフレームワークが用意されています。 '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425912"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="7168d-103">サンプルプロバイダテンプレートを適用する</span><span class="sxs-lookup"><span data-stu-id="7168d-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="7168d-104">サンプルの Outlook Social Connector (.osc) プロバイダテンプレートには、.osc プロバイダーを実装するためのフレームワークが用意されています。</span><span class="sxs-lookup"><span data-stu-id="7168d-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="7168d-105">プロバイダーテンプレートは、C++、C#、および Visual Basic で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7168d-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="7168d-106">これらのテンプレートは、プロバイダー開発の出発点にすぎません。テンプレートは、プロバイダーの実装コードの記述と、プロバイダーのセットアップパッケージの作成には対応していません。</span><span class="sxs-lookup"><span data-stu-id="7168d-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="7168d-107">次の手順は、プロバイダーの開発を開始するときに、.osc プロバイダテンプレートを適用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7168d-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="7168d-108">.osc プロバイダテンプレートを適用するには</span><span class="sxs-lookup"><span data-stu-id="7168d-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="7168d-109">[**スタート**] メニューで、[ **Microsoft Visual Studio 2010** ] を右クリックし、[**管理者として実行**] コマンドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7168d-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="7168d-110">メッセージが表示されたら、[**はい**] をクリックして、Visual Studio を管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="7168d-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="7168d-111">テンプレート内のプロジェクト名と名前空間をプロジェクト名と名前空間識別子に変更します。</span><span class="sxs-lookup"><span data-stu-id="7168d-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="7168d-112">適切なアセンブリ情報を指定するように、 **AssemblyInfo**クラスを変更します。</span><span class="sxs-lookup"><span data-stu-id="7168d-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="7168d-113">do としてマークされたインターフェイスメンバーを実装し、必要**に**応じてさらに依存関係と参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="7168d-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="7168d-114">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="7168d-114">Build the project.</span></span>
    
6. <span data-ttu-id="7168d-115">プロバイダアセンブリ ProgID がのキーとしてリストされ`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`ていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7168d-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="7168d-116">セットアッププロジェクトを配布するには、Visual Studio または任意のセットアップツールでセットアッププロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="7168d-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="7168d-117">セットアッププロジェクトは、アセンブリの COM 登録を完了し、手順5に示されているように ProgID キーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7168d-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7168d-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="7168d-118">See also</span></span>

- [<span data-ttu-id="7168d-119">サンプルのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7168d-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="7168d-120">.osc サンプルテンプレート</span><span class="sxs-lookup"><span data-stu-id="7168d-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

