---
title: サンプル プロバイダーのテンプレートを適用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Outlook ソーシャル コネクタ (OSC) のサンプル プロバイダー テンプレート フレームワークを提供、OSC プロバイダーを実装するためです。 '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804323"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="8dcb3-103">サンプル プロバイダーのテンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="8dcb3-104">Outlook ソーシャル コネクタ (OSC) のサンプル プロバイダー テンプレート フレームワークを提供、OSC プロバイダーを実装するためです。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="8dcb3-105">プロバイダー テンプレートは、C++、C# および Visual Basic で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="8dcb3-106">これらのテンプレートは、プロバイダーの開発の開始点に過ぎませんプロバイダーの実装コードを作成し、プロバイダーのセットアップ パッケージを作成する、テンプレートは対応していません。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="8dcb3-107">次の手順では、プロバイダーの開発を開始するときに、OSC プロバイダーのテンプレートを適用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="8dcb3-108">OSC プロバイダー テンプレートを適用するには</span><span class="sxs-lookup"><span data-stu-id="8dcb3-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="8dcb3-109">[**スタート**] メニューで、 **Microsoft Visual Studio 2010**を右クリックし、**管理者として実行**] コマンドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="8dcb3-110">ダイアログ ボックスが表示されたら、 **[はい]** は、管理者として Visual Studio を実行するをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="8dcb3-111">プロジェクトの名前と、テンプレート内の名前空間をプロジェクトの名前と名前空間の識別子に変更します。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="8dcb3-112">適切なアセンブリ情報を指定するのには、 **AssemblyInfo**クラスを変更します。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="8dcb3-113">**タスク**としてマークされているインターフェイス メンバーを実装し、必要に応じて複数の依存関係および参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="8dcb3-114">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-114">Build the project.</span></span>
    
6. <span data-ttu-id="8dcb3-115">プロバイダー アセンブリの ProgID が下のキーとして表示されていることを確認`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="8dcb3-116">セットアップ プロジェクトを配布するには、Visual Studio または任意のセットアップ ツールでセットアップ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="8dcb3-117">セットアップ プロジェクトは、アセンブリの COM の登録を完了し、も手順 5 に記載されている ProgID キーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8dcb3-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8dcb3-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="8dcb3-118">See also</span></span>

- [<span data-ttu-id="8dcb3-119">サンプルのダウンロード</span><span class="sxs-lookup"><span data-stu-id="8dcb3-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="8dcb3-120">OSC サンプル テンプレート</span><span class="sxs-lookup"><span data-stu-id="8dcb3-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

