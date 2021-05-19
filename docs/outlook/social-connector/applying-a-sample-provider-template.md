---
title: サンプル プロバイダー テンプレートの適用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'ソーシャル コネクタ (OSC) プロバイダー Outlookサンプルは、OSC プロバイダーを実装するためのフレームワークを提供します。 '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425912"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="71f42-103">サンプル プロバイダー テンプレートの適用</span><span class="sxs-lookup"><span data-stu-id="71f42-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="71f42-104">ソーシャル コネクタ (OSC) プロバイダー Outlookサンプルは、OSC プロバイダーを実装するためのフレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="71f42-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="71f42-105">プロバイダー テンプレートは、C++、C#、およびVisual Basic。</span><span class="sxs-lookup"><span data-stu-id="71f42-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="71f42-106">これらのテンプレートは、プロバイダー開発の開始点にすすらなります。テンプレートは、プロバイダーの実装コードを記述し、プロバイダーのセットアップ パッケージを作成する方法には取り組む必要はありません。</span><span class="sxs-lookup"><span data-stu-id="71f42-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="71f42-107">次の手順は、プロバイダーの開発を開始するときに OSC プロバイダー テンプレートを適用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="71f42-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="71f42-108">OSC プロバイダー テンプレートを適用するには</span><span class="sxs-lookup"><span data-stu-id="71f42-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="71f42-109">[スタート]**メニュー** の **[2010** 年Microsoft Visual Studio右クリックし、[管理者として実行]**コマンドをクリック** します。</span><span class="sxs-lookup"><span data-stu-id="71f42-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="71f42-110">プロンプトが表示されたら、[**は** い] をクリックして管理者Visual Studio実行します。</span><span class="sxs-lookup"><span data-stu-id="71f42-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="71f42-111">テンプレート内のプロジェクト名と名前空間をプロジェクト名と名前空間識別子に変更します。</span><span class="sxs-lookup"><span data-stu-id="71f42-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="71f42-112">**AssemblyInfo クラスを変更** して、適切なアセンブリ情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="71f42-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="71f42-113">必要に応じて、To-Doとして **マークされた** インターフェイス メンバーを実装し、さらに依存関係と参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="71f42-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="71f42-114">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="71f42-114">Build the project.</span></span>
    
6. <span data-ttu-id="71f42-115">プロバイダー アセンブリ ProgID が [キー] の下に一覧表示されている必要があります  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` 。</span><span class="sxs-lookup"><span data-stu-id="71f42-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="71f42-116">セットアップ プロジェクトを配布するには、セットアップ プロジェクトを Visual Studioまたは選択したセットアップ ツールで作成します。</span><span class="sxs-lookup"><span data-stu-id="71f42-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="71f42-117">セットアップ プロジェクトは、アセンブリの COM 登録を完了し、手順 5 に示す ProgID キーも作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71f42-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71f42-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="71f42-118">See also</span></span>

- [<span data-ttu-id="71f42-119">サンプルのダウンロード</span><span class="sxs-lookup"><span data-stu-id="71f42-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="71f42-120">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="71f42-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

