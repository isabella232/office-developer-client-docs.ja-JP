---
title: InfoPath Toolkit で作成したフォーム テンプレートを開くか変換する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- converting form templates [infopath 2007],InfoPath Toolkit, opening form templates from,form templates [InfoPath 2007], opening,InfoPath 2007, converting InfoPath Toolkit form templates,opening form templates [InfoPath 2007],form templates [InfoPath 2007], converting,script [InfoPath 2007], converting to managed code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: InfoPath 2003 Toolkit for Visual Studio に含まれるツールキットを使用して InfoPath 2003 マネージ コード フォーム テンプレートを作成した場合に、InfoPath 2003 との互換性を維持するには、Microsoft InfoPath および Visual Studio 2012 でフォーム テンプレート プロジェクト開きます。これにより、引き続きそのフォーム テンプレート プロジェクトを使用して開発を進めることができます。
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428586"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a><span data-ttu-id="0e187-104">InfoPath Toolkit で作成したフォーム テンプレートを開くか変換する</span><span class="sxs-lookup"><span data-stu-id="0e187-104">Open or Convert a Form Template Created with the InfoPath Toolkit</span></span>

<span data-ttu-id="0e187-105">InfoPath 2003 Toolkit for Visual Studio に含まれるツールキットを使用して InfoPath 2003 マネージ コード フォーム テンプレートを作成した場合に、InfoPath 2003 との互換性を維持するには、Microsoft InfoPath および Visual Studio 2012 でフォーム テンプレート プロジェクト開きます。これにより、引き続きそのフォーム テンプレート プロジェクトを使用して開発を進めることができます。</span><span class="sxs-lookup"><span data-stu-id="0e187-105">If you created an InfoPath 2003 managed code form template using one of the InfoPath 2003 Toolkits for Visual Studio and want to maintain compatibility with InfoPath 2003, you can continue to work on and further develop your form template project by opening it in Microsoft InfoPath and Visual Studio 2012.</span></span>
  
<span data-ttu-id="0e187-p101">または、InfoPath 2003 プロジェクトのコードを移行およびアップグレードして、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される新しい .NET オブジェクト モデルを使用することもできます。その場合は、 **Microsoft.Office.InfoPath** 名前空間のメンバーを使用するようにすべてのコードを書き直す必要があります。ただし、以前のプロジェクトのコードはすべて、 **#if InfoPathManagedObjectModel** ステートメントと **#endif** ステートメント (C# の場合) または **#If InfoPathManagedObject Model** ステートメントと **#End If** ステートメント (Visual Basic の場合) で囲まれて、参照用に維持されます。</span><span class="sxs-lookup"><span data-stu-id="0e187-p101">Alternatively, you can migrate and upgrade the code in your InfoPath 2003 project to use the new .NET object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace. When doing so, all of your code will need to be re-written to use members of the **Microsoft.Office.InfoPath** namespace, but all of the code from your previous project is retained and surrounded by **#if InfoPathManagedObjectModel** and **#endif** (C#) or **#If InfoPathManagedObject Model** and **#End If** (Visual Basic) statements for your reference.</span></span> 
  
<span data-ttu-id="0e187-108">以下の手順では、InfoPath Toolkit を使用して作成したマネージ コード フォーム テンプレートを開いて InfoPath 2003 との互換性を維持する方法と、新しい InfoPath オブジェクト モデルに移行およびアップグレードする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="0e187-108">The following procedures describe how to open a managed code form template created by using the InfoPath Toolkit and maintain compatibility with InfoPath 2003 or migrate and upgrade to the new InfoPath object model.</span></span> 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a><span data-ttu-id="0e187-109">InfoPath Toolkit で作成したマネージ コード フォーム テンプレートを Visual Studio Tools for Applications を使用して開き、InfoPath 2003 との互換性を維持する</span><span class="sxs-lookup"><span data-stu-id="0e187-109">Open a managed code form template created with the InfoPath Toolkit and maintain compatibility with InfoPath 2003 using Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="0e187-110">InfoPath デザイン モードを開き、[ **ファイル**] タブの [ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-110">Open the InfoPath Designer, and then click **Open** on the **File** tab.</span></span> 
    
2. <span data-ttu-id="0e187-111">[ **デザイン モードで開く**] ダイアログ ボックスで、InfoPath Toolkit フォーム テンプレート プロジェクトが保存されているプロジェクト フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="0e187-111">In the **Open in Design Mode** dialog box, navigate to the project folder where the InfoPath Toolkit form template project is saved.</span></span> 
    
    <span data-ttu-id="0e187-p102">By default, this will be a folder in  `C:\Users\` *username*  `\Documents\Visual Studio Projects` on the computer where the project was created. Or, you can move the folder to the location where InfoPath stores Visual Studio 2012 projects, which by default is  `C:\Users\` *username*  `\Documents\InfoPath Projects`</span><span class="sxs-lookup"><span data-stu-id="0e187-p102">By default, this will be a folder in  `C:\Users\` *username*  `\Documents\Visual Studio Projects` on the computer where the project was created. Or, you can move the folder to the location where InfoPath stores Visual Studio 2012 projects, which by default is  `C:\Users\` *username*  `\Documents\InfoPath Projects`</span></span>
    
3. <span data-ttu-id="0e187-114">manifest.xsf という名前のファイルをクリックし、[ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-114">Click the file that is named manifest.xsf, and then click **Open**.</span></span>
    
4. <span data-ttu-id="0e187-115">[ **開発**] タブの [ **コード エディター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-115">On the **Developer** tab, click **Code Editor**.</span></span>
    
5. <span data-ttu-id="0e187-p103">"Visual Basic または Visual C# コードを追加する前に、このフォーム テンプレートを保存する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="0e187-p103">The message "This form template must be saved before you can add Visual Basic or C# code to it" is displayed. Click **OK** to continue.</span></span> 
    
6. <span data-ttu-id="0e187-118">ファイルを保存する場所に移動し、ファイルの名前を入力して、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-118">Navigate to the location where you want to save the file, name the file, and then click **Save**.</span></span>
    
7. <span data-ttu-id="0e187-p104">"このコードは InfoPath 2003 Toolkit for Microsoft Visual Studio に含まれるツールキットで作成されたものです。InfoPath では、このツールキット プロジェクトを新しい形式に移行する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="0e187-p104">The message "This code was created with one of the InfoPath 2003 Toolkits for Microsoft Visual Studio. InfoPath needs to migrate the toolkit project to a new format" is displayed. Click **OK** to continue.</span></span> 
    
8. <span data-ttu-id="0e187-122">プロジェクトの Visual Studio ソリューション (.sln) ファイルを選択し、[ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-122">Select the Visual Studio Solution (.sln) file for the project, and then click **Open**.</span></span>
    
9. <span data-ttu-id="0e187-p105">移行プロセスが完了すると、"プロジェクトが移行されました" というメッセージが表示されます。[ **OK**] をクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="0e187-p105">The message "Your project has been migrated" is displayed when the migration process is complete. Click **OK** to continue.</span></span> 
    
10. <span data-ttu-id="0e187-p106">"このフォームのコードは、InfoPath 2003 オブジェクト モデルを使用しています" というメッセージが表示され、"Microsoft Office InfoPath オブジェクト モデルを使用するようにコードをアップグレードしますか?" とたずねられます。InfoPath 2003 との互換性を維持し、**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを引き続き使用するには、[ [いいえ](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-p106">The message "The code in this form uses the InfoPath 2003 object model" is displayed with the prompt "Do you want to upgrade your code to use the Microsoft Office InfoPath object model?" Click **No** to retain compatibility with InfoPath 2003 and to continue working with the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
    
    <span data-ttu-id="0e187-127">InfoPath 2003 と互換性のあるマネージ コード フォーム テンプレートの作業方法の詳細については、「[InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを開発する](developing-form-templates-using-the-infopath-2003-object-model.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e187-127">For information about how to work with managed code form templates that are compatible with InfoPath 2003, see [Developing Form Templates Using the InfoPath 2003 Object Model](developing-form-templates-using-the-infopath-2003-object-model.md).</span></span>
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a><span data-ttu-id="0e187-128">InfoPath Toolkit で作成したマネージ コード フォーム テンプレートを Visual Studio Tools for Applications を使用して開き、新しい InfoPath オブジェクト モデルを使用するようにアップグレードする</span><span class="sxs-lookup"><span data-stu-id="0e187-128">Open a managed code form template created with the InfoPath Toolkit and upgrade it to use the new InfoPath object model using Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="0e187-129">InfoPath デザイン モードを開き、[ **ファイル**] タブの [ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-129">Open the InfoPath Designer, and then click **Open** on the **File** tab.</span></span> 
    
2. <span data-ttu-id="0e187-130">[ **フォーム テンプレートを開く**] で、[ **自分のコンピューター上**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-130">Under **Open a form template**, click **On My Computer**.</span></span>
    
3. <span data-ttu-id="0e187-131">[ **デザイン モードで開く**] ダイアログ ボックスで、InfoPath Toolkit フォーム テンプレート プロジェクトが保存されているプロジェクト フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="0e187-131">In the **Open in Design Mode** dialog box, navigate to the project folder where the InfoPath Toolkit form template project is saved.</span></span> 
    
    <span data-ttu-id="0e187-p107">By default this will be a folder in  `C:\Users\` *username*  `\Documents\Visual Studio Projects` on the computer where the project was created. Or, you can move the folder to the location where InfoPath stores Visual Studio 2012 projects, which by default is  `C:\Users\` *username*  `\Documents\InfoPath Projects`</span><span class="sxs-lookup"><span data-stu-id="0e187-p107">By default this will be a folder in  `C:\Users\` *username*  `\Documents\Visual Studio Projects` on the computer where the project was created. Or, you can move the folder to the location where InfoPath stores Visual Studio 2012 projects, which by default is  `C:\Users\` *username*  `\Documents\InfoPath Projects`</span></span>
    
4. <span data-ttu-id="0e187-134">manifest.xsf という名前のファイルをクリックし、[ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-134">Click the file that is named manifest.xsf, and then click **Open**.</span></span>
    
5. <span data-ttu-id="0e187-135">[ **開発**] タブの [ **コード エディター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-135">On the **Developer** tab, click **Code Editor**.</span></span>
    
6. <span data-ttu-id="0e187-p108">"Visual Basic または Visual C# コードを追加する前に、このフォーム テンプレートを保存する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="0e187-p108">The message "This form template must be saved before you can add Visual Basic or C# code to it" is displayed. Click **OK** to continue.</span></span> 
    
7. <span data-ttu-id="0e187-138">ファイルを保存する場所に移動し、ファイルの名前を入力して、[ **保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-138">Navigate to the location where you want to save the file, name the file, and then click **Save**.</span></span>
    
8. <span data-ttu-id="0e187-p109">"このコードは InfoPath 2003 Toolkit for Microsoft Visual Studio に含まれるツールキットで作成されたものです。InfoPath では、このツールキット プロジェクトを新しい形式に移行する必要があります" というメッセージが表示されます。[ **OK**] をクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="0e187-p109">The message "This code was created with one of the InfoPath 2003 Toolkits for Microsoft Visual Studio. InfoPath needs to migrate the toolkit project to a new format" is displayed. Click **OK** to continue.</span></span> 
    
9. <span data-ttu-id="0e187-142">プロジェクトの Visual Studio ソリューション (.sln) ファイルを選択し、[ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0e187-142">Select the Visual Studio Solution (.sln) file for the project, and then click **Open**.</span></span>
    
10. <span data-ttu-id="0e187-p110">移行プロセスが完了すると、"プロジェクトが移行されました" というメッセージが表示されます。[ **OK**] をクリックして続行します。</span><span class="sxs-lookup"><span data-stu-id="0e187-p110">The message "Your project has been migrated" is displayed when the migration process is complete. Click **OK** to continue.</span></span> 
    
11. <span data-ttu-id="0e187-p111">"このフォームのコードは、InfoPath 2003 オブジェクト モデルを使用しています" というメッセージが表示され、"Microsoft Office InfoPath オブジェクト モデルを使用するようにコードをアップグレードしますか?" とたずねられます。[ **はい**] をクリックして、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される新しいマネージ コード オブジェクト モデルを使用するようにフォーム テンプレートをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="0e187-p111">The message "The code in this form uses the InfoPath 2003 object model" is displayed with the prompt "Do you want to upgrade your code to use the Microsoft Office InfoPath object model?" Click **Yes** to upgrade the form template to use the new managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
    
    <span data-ttu-id="0e187-p112">フォーム コードが Visual Studio 2012 コード エディターで開きます。以前のプロジェクトのすべてのコードが、 **#if** **InfoPathManagedObjectModel** ステートメントと **#endif** ステートメント (C# の場合) または **#If InfoPathManagedObjectModel** ステートメントと **#End If** ステートメント (Visual Basic の場合) で囲まれて、参照用に維持されています。これらすべてのコードを、 **Microsoft.Office.InfoPath** 名前空間によって提供されるオブジェクト モデルのメンバーを使用するように書き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e187-p112">Your form code is opened in the Visual Studio 2012 code editor with all of the code from your previous project surrounded by **#if** **InfoPathManagedObjectModel** and **#endif** (C#) or **#If InfoPathManagedObjectModel** and **#End If** (Visual Basic) statements for your reference. All of this code will have to be re-written to use members of the object model provided by the **Microsoft.Office.InfoPath** namespace.</span></span> 
    
    <span data-ttu-id="0e187-149">新しい InfoPath マネージ コード オブジェクト モデルを使用するマネージ コード フォーム テンプレートの作業方法の詳細については、「[コードを含む InfoPath フォーム テンプレートを開発する](developing-infopath-form-templates-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e187-149">For information about how to work with managed code form templates that use the new InfoPath managed code object model, see [Developing InfoPath Form Templates with Code](developing-infopath-form-templates-with-code.md).</span></span>
    

