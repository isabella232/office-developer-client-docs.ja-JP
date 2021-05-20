---
title: SharePoint オブジェクト モデルのメンバーを使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: InfoPath フォーム テンプレート内で実行されるコードから、SharePoint オブジェクト モデルのメンバーに対してプログラミングを行う場合は、事前に、フォームの Visual Studio 2012 プロジェクトで Microsoft.SharePoint.dll アセンブリを参照する必要があります。そのためには、Microsoft SharePoint Server 2010 のライセンス コピーのファイル システム、または Microsoft SharePoint Foundation 2010 を実行するサーバーのファイル システムにアクセスして、Microsoft.SharePoint.dll アセンブリのコピーを取得する必要があります。
ms.openlocfilehash: e29725450a6a1bdcba99215e337493f8686491e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431660"
---
# <a name="use-sharepoint-object-model-members"></a><span data-ttu-id="8a034-104">SharePoint オブジェクト モデルのメンバーを使用する</span><span class="sxs-lookup"><span data-stu-id="8a034-104">Use SharePoint Object Model Members</span></span>

<span data-ttu-id="8a034-p102">InfoPath フォーム テンプレート内で実行されるコードから、SharePoint オブジェクト モデルのメンバーに対してプログラミングを行う場合は、事前に、フォームの Visual Studio 2012 プロジェクトで Microsoft.SharePoint.dll アセンブリを参照する必要があります。そのためには、Microsoft SharePoint Server 2010 のライセンス コピーのファイル システム、または Microsoft SharePoint Foundation 2010 を実行するサーバーのファイル システムにアクセスして、Microsoft.SharePoint.dll アセンブリのコピーを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a034-p102">Before you can program against members of the SharePoint object model from code running in an InfoPath form template, you must reference the Microsoft.SharePoint.dll assembly in the Visual Studio 2012 project for your form. To do that, you must have access to the file system of a licensed copy of Microsoft SharePoint Server 2010 or a server that is running Microsoft SharePoint Foundation 2010 so that you can obtain a copy of the Microsoft.SharePoint.dll assembly.</span></span> 
  
<span data-ttu-id="8a034-p103">また、フォーム テンプレートを、サンドボックス ソリューションまたは管理者承認ソリューションのどちらかとして、サーバーに展開する必要もあります。これらの展開オプションの詳細については、「[コードを含むフォームを発行する](publishing-forms-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a034-p103">Additionally, your form template must be deployed to the server as either a sandboxed or administrator-approved solution. For more information about these deployment options, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a><span data-ttu-id="8a034-109">Microsoft.SharePoint アセンブリを追加して、InfoPath フォーム テンプレートから参照する</span><span class="sxs-lookup"><span data-stu-id="8a034-109">Add and Reference the Microsoft.SharePoint Assembly from an InfoPath Form Template</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a034-p104">InfoPath プロジェクト システムがフォーム テンプレート ファイルに追加されるファイルを管理する方法と競合しないように、フォーム テンプレート プロジェクトの最上位フォルダーには、参照するアセンブリをコピーしないでください。既定では、このフォルダーのパス形式は、< *ドライブ*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *製品名*  となります。 > 参照するアセンブリをプロジェクト フォルダー内で移動するには、メインの *製品名*  プロジェクト フォルダーの下にサブフォルダーを作成し、そのサブフォルダーにコピーしたアセンブリを参照する必要があります。ただし、参照するアセンブリのためのサブフォルダーを作成する必要はありません。参照するアセンブリがプロジェクトの最上位フォルダーになければ、プロジェクトをコンパイルおよび発行したときに、InfoPath プロジェクト システムによってアセンブリがフォーム テンプレート ファイル (.xsn) にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8a034-p104">To avoid a conflict with how the InfoPath project system manages files that are added to the form template file, do not copy any assemblies that you want to reference into the top-level folder of a form template project. By default, this will be a path in the following format: < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName* > If you do want to move assemblies that you reference to a location within the project folder, you must create a subfolder under the main  *ProjectName*  project folder, and then copy and reference assemblies from that subfolder. However, be aware that creating a subfolder for referenced assemblies is not necessary. As long as a referenced assembly is not located within the project's top-level folder, the InfoPath project system will copy the assembly into the form template file (.xsn) when the project is compiled and published.</span></span> 
  
<span data-ttu-id="8a034-114">既定では、Microsoft.SharePoint.Server.dll は、SharePoint Server 2010 のファイル システム、または SharePoint Foundation 2010 を実行するサーバーのファイル システムの C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="8a034-114">By default, Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI in the file system of SharePoint Server 2010 or a server that is running SharePoint Foundation 2010.</span></span>
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a><span data-ttu-id="8a034-115">Microsoft.SharePoint アセンブリを、InfoPath フォームのコード プロジェクトから参照するには</span><span class="sxs-lookup"><span data-stu-id="8a034-115">To reference the Microsoft.SharePoint assembly from an InfoPath form's code project</span></span>

1. <span data-ttu-id="8a034-116">Microsoft.SharePoint.Server.dll アセンブリをサーバーからローカル フォルダーにコピーするか、共有フォルダーからアセンブリへのアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="8a034-116">Copy the Microsoft.SharePoint.Server.dll assembly from the server to a local folder, or get access to the assembly from a shared folder.</span></span>
    
2. <span data-ttu-id="8a034-117">Visual Studio 2012 で、フォーム テンプレート プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a034-117">Open the form template project in Visual Studio 2012.</span></span>
    
3. <span data-ttu-id="8a034-118">[ **プロジェクト**] メニューの [ **参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a034-118">On the **Project** menu, click **Add Reference**.</span></span>
    
4. <span data-ttu-id="8a034-119">[ **参照**] タブをクリックし、アセンブリを探して選択し、[ **OK**] をクリックして参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="8a034-119">Click the **Browse** tab, locate and specify the assembly, and then click **OK** to add the reference.</span></span> 
    
<span data-ttu-id="8a034-p105">これで、SharePoint オブジェクト モデルのメンバーに対して、フォーム コードからコードを記述できるようになりました。Microsoft.SharePoint 名前空間のメンバーをより簡単に参照するには、コード ファイルの一番上のディレクティブに、 `using Microsoft.SharePoint;` または  `Imports Microsoft.SharePoint` を追加します。InfoPath フォーム内での SharePoint オブジェクト モデルのメンバーの使用例については、「 [サンドボックス ソリューションのサンプル](sample-sandboxed-solutions.md)」の「例 2: SharePoint リストでのベンダーの管理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a034-p105">Now you can write code against members of the SharePoint object model from your form code. To make it easier to reference members of the Microsoft.SharePoint namespace, add  `using Microsoft.SharePoint;` or  `Imports Microsoft.SharePoint` to the directives at the beginning of your code file. For an example that shows how to use members of the SharePoint object model in an InfoPath form, see "Example 2: Managing Vendors in a SharePoint List" in [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>

