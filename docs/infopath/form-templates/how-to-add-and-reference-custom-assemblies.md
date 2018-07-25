---
title: カスタム アセンブリを追加および参照する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003 互換のフォーム テンプレート,カスタム アセンブリを使用する,アセンブリ [InfoPath 2007],InfoPath 2003 オブジェクト モデルを使用してカスタムを追加する
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: マネージ コードのフォーム テンプレート プロジェクトでカスタム アセンブリへの参照を追加すると、プロジェクトをコンパイルおよび発行したときに、そのアセンブリがフォーム テンプレート ファイル (.xsn) に含められます。
ms.openlocfilehash: e182930ebe14b6f64d1b90509fe400cc1fb1b26e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799107"
---
# <a name="add-and-reference-custom-assemblies"></a><span data-ttu-id="0511a-104">カスタム アセンブリを追加および参照する</span><span class="sxs-lookup"><span data-stu-id="0511a-104">How to: Add and Reference Custom Assemblies</span></span>

<span data-ttu-id="0511a-105">マネージ コードのフォーム テンプレート プロジェクトでカスタム アセンブリへの参照を追加すると、プロジェクトをコンパイルおよび発行したときに、そのアセンブリがフォーム テンプレート ファイル (.xsn) に含められます。</span><span class="sxs-lookup"><span data-stu-id="0511a-105">When you add a reference to a custom assembly in a managed-code form template project, that assembly is included within the form template file (.xsn) when your project is compiled and published.</span></span>
  
## <a name="add-and-reference-a-custom-assembly"></a><span data-ttu-id="0511a-106">カスタム アセンブリを追加および参照する</span><span class="sxs-lookup"><span data-stu-id="0511a-106">Add and Reference a Custom Assembly</span></span>

<span data-ttu-id="0511a-p101">InfoPath プロジェクト システムがフォーム テンプレート ファイルに追加されるファイルを管理する方法と競合しないように、フォーム テンプレート プロジェクトの最上位フォルダーには、参照するカスタム アセンブリをコピーしないでください。既定では、このフォルダーのパス形式は < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*  となります。</span><span class="sxs-lookup"><span data-stu-id="0511a-p101">To avoid a conflict with how the InfoPath project system manages files that are added to the form template file, do not copy any custom assemblies that you want to reference into the top-level folder of a form template project. By default, this will be a path in the following format: < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*</span></span> 
  
<span data-ttu-id="0511a-p102">参照するカスタム アセンブリをプロジェクト フォルダー内で移動するには、メイン プロジェクト フォルダーの下にサブフォルダーを作成し、そのサブフォルダーにコピーしたカスタム アセンブリを参照する必要があります。ただし、参照するアセンブリのためのサブフォルダーを作成する必要はありません。参照するアセンブリがプロジェクトの最上位フォルダーになければ、プロジェクトをコンパイルおよび発行したときに、InfoPath プロジェクト システムによってアセンブリがフォーム テンプレート ファイル (.xsn) にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="0511a-p102">If you do want to move custom assemblies that you reference to a location within the project folder, you must create a subfolder under the main project folder, and then copy and reference custom assemblies from that subfolder. However, be aware that creating a subfolder for referenced assemblies is not necessary. As long as a referenced assembly is not located within the project's top-level folder, the InfoPath project system will copy the assembly into the form template file (.xsn) when the project is compiled and published.</span></span>
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a><span data-ttu-id="0511a-112">既定の場所からカスタム アセンブリを参照する</span><span class="sxs-lookup"><span data-stu-id="0511a-112">Reference a custom assembly from its default location</span></span>

1. <span data-ttu-id="0511a-113">Visual Studio 2012 でフォーム テンプレート プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="0511a-113">Open the form template project in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="0511a-114">[ **プロジェクト**] メニューで、[ **参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0511a-114">On the **Project** menu, click **Add Reference**.</span></span>
    
3. <span data-ttu-id="0511a-115">[ **参照**] タブで、アセンブリを探して選択し、[ **OK**] をクリックして参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="0511a-115">Click the **Browse** tab, locate and specify the assembly, and then click **OK** to add the reference.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0511a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="0511a-116">See also</span></span>

#### <a name="tasks"></a><span data-ttu-id="0511a-117">タスク</span><span class="sxs-lookup"><span data-stu-id="0511a-117">Tasks</span></span>

[<span data-ttu-id="0511a-118">InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="0511a-118">How to: Create a Form Template Using the InfoPath 2003 Object Model</span></span>](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

