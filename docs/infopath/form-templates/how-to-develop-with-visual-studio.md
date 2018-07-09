---
title: Visual Studio を開発します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Visual Studio 2012 で開発したマネージ コードを使用して InfoPath フォームを拡張することによって、フォームの機能を大幅に強化できます。フォームを拡張したら、コードを含むフォームを SharePoint Server 2013 のフォーム ライブラリに発行できます。
ms.openlocfilehash: d6a2cfa1847b4b59b6978b8f4a0775aedf07a72d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799133"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="29525-104">Visual Studio を開発します。</span><span class="sxs-lookup"><span data-stu-id="29525-104">Develop with Visual Studio</span></span>

<span data-ttu-id="29525-p102">Visual Studio 2012 で開発したマネージ コードを使用して InfoPath フォームを拡張することによって、フォームの機能を大幅に強化できます。フォームを拡張したら、コードを含むフォームを SharePoint Server 2013 のフォーム ライブラリに発行できます。</span><span class="sxs-lookup"><span data-stu-id="29525-p102">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012. You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="29525-107">マネージ コードを含む InfoPath フォームのプログラミングと展開は、次の 3 つの大まかな手順で始めることができます。</span><span class="sxs-lookup"><span data-stu-id="29525-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="29525-108">Visual Studio 2012 を [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) アドオンと共にインストールします。</span><span class="sxs-lookup"><span data-stu-id="29525-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="29525-109">プログラミング言語を設定し、Visual Studio 2012 コード エディターでコードを記述してデバッグします。</span><span class="sxs-lookup"><span data-stu-id="29525-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="29525-110">フォームのデザインとコードの開発が完了したら、フォーム テンプレートを SharePoint Server 2013 に発行できます。</span><span class="sxs-lookup"><span data-stu-id="29525-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="29525-111">次の理由から、SharePoint Server 2013 と互換性のあるフォームを作成することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="29525-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="29525-p103">InfoPath Forms Services を実行している SharePoint Server 2013 にフォームを展開すると、ブラウザーでフォームに入力できます。これにより、InfoPath をインストールしていないユーザーもフォームを開いて使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="29525-p103">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser. This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="29525-p104">デザインするフォームのバージョンを 1 つに限定できます。Microsoft SharePoint Server と互換性のあるフォームは InfoPath Filler とも互換性がありますが、InfoPath Filler としか互換性のないフォームをブラウザーで開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="29525-p104">You design only one version of the form. Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="29525-p105">フォームを SharePoint に発行する方法としては、SharePoint のセキュリティで保護されたソリューションと管理者が展開するソリューションの 2 つがあります。それぞれの発行方法と、現在のシナリオに最適な方法を判断する際の推奨事項の詳細については、「[コードを含むフォームを発行する](publishing-forms-with-code.md)」を参照してください。セキュリティで保護されたソリューションの例については、「[サンドボックス ソリューションのサンプル](sample-sandboxed-solutions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29525-p105">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions. For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md). For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="29525-119">Visual Studio での開発</span><span class="sxs-lookup"><span data-stu-id="29525-119">Developing with Visual Studio</span></span>

<span data-ttu-id="29525-120">Visual Studio 2012 と Microsoft Visual Studio Tools for Applications 2012 アドオンをインストールしたら、InfoPath マネージ コード ソリューションの開発をいつでも開始できます。</span><span class="sxs-lookup"><span data-stu-id="29525-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="29525-121">プログラミング言語の選択</span><span class="sxs-lookup"><span data-stu-id="29525-121">Choosing a Programming Language</span></span>

<span data-ttu-id="29525-p106">InfoPath では、Visual Basic と C# の 2 種類の言語で 4 つのバージョンの InfoPath オブジェクト モデルを使用することによって、プログラミングのためのオプションを提供しています。4 つのバージョンのオブジェクト モデルは、InfoPath 2013、InfoPath、Office InfoPath 2007、および Microsoft InfoPath 2003 と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="29525-p106">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#. The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="29525-124">プログラミング言語とオブジェクト モデルを指定するには</span><span class="sxs-lookup"><span data-stu-id="29525-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="29525-125">InfoPath デザイン モードでフォーム テンプレート プロジェクトを開いた状態で、[ **開発**] タブの [ **言語**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29525-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="29525-p107">[ **フォームのオプション**] ダイアログ ボックスの [ **プログラミング**] カテゴリで、[ **フォーム テンプレートのコード言語**] ボックスの一覧から使用する言語を選択します。[ **ターゲット バージョン**] ボックスの一覧からオブジェクト モデルのバージョンを選択します。InfoPath 2013 としか互換性のない **ターゲット バージョン** オプションには、" **InfoPath**" という名前の後にバージョンを表す年が付いていません。</span><span class="sxs-lookup"><span data-stu-id="29525-p107">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list. Then, select the version of the object model from the **Target version** drop-down list. The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="29525-p108">すべての種類のフォーム テンプレートがコードをサポートしているわけではありません。たとえば、 **SharePoint リスト** フォーム テンプレートと **テンプレート パーツ**は、フォーム コードをサポートしていません。コードをサポートしていないフォーム テンプレートをデザインする場合、[ **開発**] タブは使用できません。また、4 つのバージョンのオブジェクト モデルをすべてサポートしているのは一部のフォーム テンプレートに限られます。たとえば、 **空白のフォーム (InfoPath Filler)** テンプレートは、4 つのバージョンのオブジェクト モデルをすべてサポートしており、各バージョンでは InfoPath Filler とのみ互換性があるフォーム テンプレートが作成されます。しかし、 **空白のフォーム** テンプレートは InfoPath 2013 と InfoPath だけをサポートしており、InfoPath Filler とブラウザーの両方と互換性があるフォーム テンプレートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="29525-p108">Not all form template types support code. For example, the **SharePoint List** form template type and **Template Parts** do not support form code. When designing a form template type that does not support code, the **Developer** tab will not be available. Also, only some form template types support all four versions of the object model. For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="29525-134">既定のプログラミング言語を設定できます。その場合、InfoPath フォーム デザイナーは選択した言語とオブジェクト モデル バージョンで常に起動するようになります。</span><span class="sxs-lookup"><span data-stu-id="29525-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="29525-135">既定のプログラミング言語を設定するには</span><span class="sxs-lookup"><span data-stu-id="29525-135">To set the default programming language</span></span>

1. <span data-ttu-id="29525-136">[ **ファイル**] タブをクリックし、[ **オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29525-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="29525-137">[ **InfoPath オプション**] ダイアログ ボックスの [ **基本設定**] セクションで、[ **その他のオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29525-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="29525-138">[ **オプション**] ダイアログ ボックスの [ **デザイン**] タブの [ **プログラミング用の既定値**] セクションで、既定のプログラミング言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="29525-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="29525-139">コードの作成</span><span class="sxs-lookup"><span data-stu-id="29525-139">Writing Code</span></span>

<span data-ttu-id="29525-140">これで、InfoPath 2013 と Visual Studio 2012 を使用して開発作業を開始できます。</span><span class="sxs-lookup"><span data-stu-id="29525-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="29525-141">Visual Studio コード エディターを起動するには</span><span class="sxs-lookup"><span data-stu-id="29525-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="29525-142">InfoPath デザイン モードでフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="29525-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="29525-143">[ **開発**] タブの [ **コード エディター**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29525-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="29525-144">[ **開発**] タブのコマンド、ショートカット メニュー、およびその他のユーザー インターフェイスを使用して、コード エディターを起動し、フォームのイベント ハンドラーやコントロール イベントを自動的に追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="29525-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="29525-145">詳細については、[イベント ハンドラーの追加](how-to-add-an-event-handler.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29525-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

