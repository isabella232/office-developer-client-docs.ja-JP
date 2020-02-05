---
title: プログラムを使用して Visio ファイル形式を操作する
manager: lindalu
ms.date: 04/17/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Visio 2013 での新しいファイル形式パッケージを読み取り、パッケージ内のパーツを選択しその中のデータを変更して、パッケージに新しいパーツを追加するソリューションをVisual Studio 2012で作成します。
localization_priority: Priority
ms.openlocfilehash: 36a621856e5d53e7b3355a39edd7b7a03636b15d
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773744"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a><span data-ttu-id="3c348-103">プログラムを使用して Visio ファイル形式を操作する</span><span class="sxs-lookup"><span data-stu-id="3c348-103">Manipulate the Visio file format programmatically</span></span>

![操作手順のトピック](media/mod_icon_howto.png)
  
<span data-ttu-id="3c348-105">Visio 2013 での新しいファイル形式パッケージを読み取り、パッケージ内のパーツを選択しその中のデータを変更して、パッケージに新しいパーツを追加するソリューションをVisual Studio 2012で作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3c348-105">Learn how to create a solution in Visual Studio 2012 to read the new file format package in Visio 2013, select parts in the package, change the data in a part, and add new parts to the package.</span></span>
   
## <a name="visio-file-format-manipulation-essentials"></a><span data-ttu-id="3c348-106">Visio ファイル形式の操作の基本</span><span class="sxs-lookup"><span data-stu-id="3c348-106">Visio file format manipulation essentials</span></span>
<span data-ttu-id="3c348-107"><a name="vis15_ManipulateFF_Essentials"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-107"><a name="vis15_ManipulateFF_Essentials"> </a></span></span>

<span data-ttu-id="3c348-108">Visio の以前のバージョンでは、独自のバイナリ ファイル形式 (.vsd) またはシングル ドキュメント Visio XML 図面ファイル形式 (.vdx) でファイルを保存していました。</span><span class="sxs-lookup"><span data-stu-id="3c348-108">Previous versions of Visio saved files in a proprietary binary file format (.vsd) or a single-document Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="3c348-109">Visio 2013 では、XML と ZIP のアーカイブ テクノロジに基づく新しいファイル形式 (.vsdx) が導入されています。</span><span class="sxs-lookup"><span data-stu-id="3c348-109">Visio 2013 introduces a new file format (.vsdx), which is based on XML and ZIP archive technologies.</span></span> <span data-ttu-id="3c348-110">以前のバージョンの Visio と同じように、ファイルは 1 つのコンテナーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="3c348-110">Just as in previous versions of Visio, files are saved in a single container.</span></span> <span data-ttu-id="3c348-111">しかし、従来のファイルとは違って、新しいファイル形式は Visio 2013 アプリケーションを自動化することなく、開いたり、読み取ったり、更新したり、変更したり、構築したりできます。</span><span class="sxs-lookup"><span data-stu-id="3c348-111">Unlike legacy files, however, the new file format can be opened, read, updated, changed, and constructed without automating the Visio 2013 application.</span></span> <span data-ttu-id="3c348-112">XML の操作や [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) 名前空間の処理に精通している開発者は、プログラムによる新しいファイル形式ですぐに仕事を始められます。</span><span class="sxs-lookup"><span data-stu-id="3c348-112">Developers who are familiar with manipulating XML or working with the [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) namespace can quickly get started working with the new file format programmatically.</span></span> <span data-ttu-id="3c348-113">以前のバージョンから Visio XML 図面形式を処理していた開発者は、以前の形式の構造の多くが新しいファイル形式でも保持されていることに気づかれるでしょう。</span><span class="sxs-lookup"><span data-stu-id="3c348-113">Developers who have worked with the Visio XML Drawing format from previous versions can find that many of the structures from that format have been retained in the new file format.</span></span> 
  
<span data-ttu-id="3c348-114">この記事では、Microsoft .NET Framework 4.5 や C#、Visual Basic、 Visual Studio 2012 を使用して、Visio 2013 でファイル形式をプログラムによって操作する方法を検証します。</span><span class="sxs-lookup"><span data-stu-id="3c348-114">In this article, we examine how to work with the Visio 2013 file format programmatically, using the Microsoft .NET Framework 4.5, C# or Visual Basic, and Visual Studio 2012.</span></span> <span data-ttu-id="3c348-115">Visio 2013 ファイルを開き、ファイル内のドキュメント パーツを選択し、パーツ内のデータを変更し、新しいドキュメント パーツを作成する方法が記載されています。</span><span class="sxs-lookup"><span data-stu-id="3c348-115">You can see how to open a Visio 2013 file, select document parts within the file, change data in parts, and create a new document part.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3c348-116">この記事のコード サンプルは、読者が [System.Xml.Linq](https://docs.microsoft.com/dotnet/api/system.xml.linq?view=netframework-4.8) と [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) の名前空間内のクラスに関する基本的な知識があることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-116">The code samples in this article assume that you have a rudimentary understanding of the classes in the [System.Xml.Linq](https://docs.microsoft.com/dotnet/api/system.xml.linq?view=netframework-4.8) and [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) namespaces.</span></span> <span data-ttu-id="3c348-117">> この記事では、読者が Open Packaging Conventions の概念と用語を理解していることも想定しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-117">> This article also assumes that you understand the concepts and terminology of the Open Packaging Conventions.</span></span> <span data-ttu-id="3c348-118">パッケージ、文書パーツまたはパッケージ パーツ、およびリレーションシップの概念を理解している必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-118">You should have some familiarity with the concepts of packages, document parts or package parts, and relationships.</span></span> <span data-ttu-id="3c348-119">詳しくは、[OPC: データのパッケージ化のための新しい標準](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3c348-119">For more information, see [OPC: A New Standard for Packaging Your Data](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data).</span></span> <span data-ttu-id="3c348-120">> コードは、統合言語クエリ (LINQ: Language-Integrated Query) を作成して XML を選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-120">> The code demonstrates how to create LINQ (Language-Integrated Query) queries to select XML.</span></span> <span data-ttu-id="3c348-121">コード サンプルのほとんどでは、クエリ構文を使用して LINQ クエリを構築しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-121">Most of the code samples use the query syntax for building LINQ queries.</span></span> <span data-ttu-id="3c348-122">必要に応じて、LINQ メソッド構文を使用して、コード内にある LINQ クエリを書き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="3c348-122">You can rewrite any of the LINQ queries provided in the code by using the LINQ method syntax, if necessary.</span></span> <span data-ttu-id="3c348-123">LINQ クエリの構文とメソッドの構文の詳細については、次を参照してください。[LINQ クエリ構文とメソッドの構文 (C#)](https://docs.microsoft.com/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq)> 表 1 は、この記事を読み進める前に精通しておく必要のある重要なトピックを示しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-123">For more information about LINQ query syntax and method syntax, see [LINQ Query Syntax versus Method Syntax (C#)](https://docs.microsoft.com/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq)> Table 1 shows the essential topics that you should be familiar with before you work through this article.</span></span> 
  
<span data-ttu-id="3c348-124">**表 1. Visio 2013 ファイル形式の操作に関する中心的概念**</span><span class="sxs-lookup"><span data-stu-id="3c348-124">**Table 1. Core concepts for manipulating the Visio 2013 file format**</span></span>

|<span data-ttu-id="3c348-125">**記事のタイトル**</span><span class="sxs-lookup"><span data-stu-id="3c348-125">**Article title**</span></span>|<span data-ttu-id="3c348-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c348-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c348-127">Visio ファイル形式 (.vsdx) の概要</span><span class="sxs-lookup"><span data-stu-id="3c348-127">Introduction to the Visio file format (.vsdx)</span></span>](introduction-to-the-visio-file-formatvsdx.md) <br/> |<span data-ttu-id="3c348-128">この概説では、Visio 2013 ファイル形式の主な機能の一部を説明しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-128">This high-level overview describes some of the major features of the Visio 2013 file format.</span></span> <span data-ttu-id="3c348-129">Visio 2013 ファイル形式に適用されている Open Packaging Conventions (OPC) について解説しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-129">It discusses the Open Packaging Conventions (OPC) as they have been applied to the Visio 2013 file format.</span></span> <span data-ttu-id="3c348-130">また、Visio 2013 ファイル形式と以前の Visio XML 図面ファイル形式 (.vdx) との違いを抜粋して一覧表示しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-130">It also lists some differences between the Visio 2013 file format and the previous Visio XML Drawing file format (.vdx).</span></span>  <br/> |
|[<span data-ttu-id="3c348-131">OPC: データのパッケージ化のための新しい標準</span><span class="sxs-lookup"><span data-stu-id="3c348-131">OPC: A New Standard for Packaging Your Data</span></span>](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data) <br/> |<span data-ttu-id="3c348-132">この MSDN マガジンの記事では、Open Packaging Conventions の概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="3c348-132">This MSDN Magazine article describes the Open Packaging Conventions as a concept.</span></span>  <br/> |
|<span data-ttu-id="3c348-133">[Open Packaging Conventions の基本](https://docs.microsoft.com/en-us/previous-versions/office/office-12/ee361919(v=office.12))</span><span class="sxs-lookup"><span data-stu-id="3c348-133">[Essentials of the Open Packaging Conventions](https://docs.microsoft.com/en-us/previous-versions/office/office-12/ee361919(v=office.12))</span></span> <br/> <span data-ttu-id="3c348-134">[Office (2007) Open XML ファイル形式の概要](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12))</span><span class="sxs-lookup"><span data-stu-id="3c348-134">[Introducing the Office (2007) Open XML File Formats](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12))</span></span> <br/> |<span data-ttu-id="3c348-135">これら 2 つの記事では、Open Packaging Conventions を Microsoft Office ファイルに適用する方法について解説します。</span><span class="sxs-lookup"><span data-stu-id="3c348-135">These two articles discuss how the Open Packaging Conventions have been applied to Microsoft Office files.</span></span> <span data-ttu-id="3c348-136">パッケージ内でのリレーションシップの働きについて説明し、コード例もいくつか記述されています。</span><span class="sxs-lookup"><span data-stu-id="3c348-136">They contain descriptions of how relationships work in a package and also include some code examples.</span></span>  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a><span data-ttu-id="3c348-137">.vsdx ファイルと新しい Visual Studio ソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="3c348-137">Create a .vsdx file and a new Visual Studio solution</span></span>
<span data-ttu-id="3c348-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span></span>

<span data-ttu-id="3c348-139">この記事の手順で作業を開始する前に、操作の対象となる Visio 2013 ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-139">Before you can begin working through the procedures in this article, you need to create a Visio 2013 file to open and manipulate.</span></span> <span data-ttu-id="3c348-140">この記事のコード例で使用されている図面には 1 つのページがあり、そこに 2 つの接続された図形が含まれます。そのうちの 1 つは「基本フローチャート」テンプレートからの「開始/終了」図形になります。</span><span class="sxs-lookup"><span data-stu-id="3c348-140">The drawing used in the code examples in this article contains a single page with two connected shapes on it, one of the shapes being a "Start/End" shape from the "Basic Flowchart" template.</span></span>
  
<span data-ttu-id="3c348-141">次の手順を使用して、この記事の残りの手順で使用する Visio 2013 のファイルを新しく作成してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-141">Use the following procedure to create a new Visio 2013 file to use in the remaining procedures in this article.</span></span>
  
### <a name="to-create-new-file-in-visio-2013"></a><span data-ttu-id="3c348-142">Visio 2013 の新しいファイルを作成するには</span><span class="sxs-lookup"><span data-stu-id="3c348-142">To create new file in Visio 2013</span></span>

1. <span data-ttu-id="3c348-143">Visio 2013 を開きます。</span><span class="sxs-lookup"><span data-stu-id="3c348-143">Open Visio 2013.</span></span>
    
2. <span data-ttu-id="3c348-144">**[カテゴリ]**、**[フローチャート]**、**[基本フローチャート]**、**[作成]** を選択して、基本フローチャート テンプレートに基づいて新しいドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c348-144">Create a new document based on the Basic Flowchart template by choosing **CATEGORIES**, **Flowchart**, **Basic Flowchart**, **Create**.</span></span>
    
3. <span data-ttu-id="3c348-145">**[図形]**  ウィンドウから、**[開始/終了]** 図形をキャンバス上にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="3c348-145">From the **Shapes** window, drag a **Start/End** shape onto the canvas.</span></span> 
    
4. <span data-ttu-id="3c348-146">図面キャンバス上で新しい開始/終了図形を選択し、「処理の開始」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3c348-146">Select the new Start/End shape on the drawing canvas and type 'Begin Process'.</span></span>
    
5. <span data-ttu-id="3c348-147">**[図形]** ウィンドウから、**[処理]** 図形をキャンバス上にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="3c348-147">From the **Shapes** window, drag a **Process** shape onto the canvas.</span></span> 
    
6. <span data-ttu-id="3c348-148">図面キャンバス上で新しい処理図形を選択 し、「タスクの実行」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3c348-148">Select the new Process shape on the drawing canvas and type 'Perform some task'.</span></span>
    
7. <span data-ttu-id="3c348-149">開始/終了図形のショートカット メニューで、**[ページに 1 つのコネクタを追加]** を選択してから、図 1 のように、キャンバス上の開始/終了図形と処理図形の間にコネクタを描画します。</span><span class="sxs-lookup"><span data-stu-id="3c348-149">On the shortcut menu for the Start/End shape, select **Add One Connector to the Page**, and then draw a connector between the Start/End and Process shapes on the canvas, as shown in Figure 1.</span></span>
    
    <span data-ttu-id="3c348-150">**図 1。Visio 2013 の簡単な描画**</span><span class="sxs-lookup"><span data-stu-id="3c348-150">**Figure 1. Simple Visio 2013 drawing**</span></span>
    
     ![処理図形に接続されている開始/終了図形](media/vis15_SimpleFlowchart.png)
  
8. <span data-ttu-id="3c348-152">**[ファイル]**、**[名前を付けて保存]**、**[コンピューター]**、**[デスクトップ]** を選択して、ファイルをデスクトップに .vsdx ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="3c348-152">Save the file to your Desktop as a .vsdx file by choosing **File**, **Save As**, **Computer**, **Desktop**.</span></span>
    
    <span data-ttu-id="3c348-153">**[名前を付けて保存]** ダイアログ ボックスで、**[ファイル名]** ボックスに「Visio パッケージ」と入力し、**[ファイルの種類]\*リストで **[Visio 図面 (**.vsdx)]** を選択してから、**[保存]** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-153">In the **Save As** dialog box, enter Visio Package in the **File name** box"", select **Visio Drawing (\*.vsdx)** in the **Save as type** list, and then choose the **Save** button.</span></span> 
    
9. <span data-ttu-id="3c348-154">ファイルを閉じてから、Visio 2013 を閉じます。</span><span class="sxs-lookup"><span data-stu-id="3c348-154">Close the file and then close Visio 2013.</span></span>
    
> [!TIP]
> <span data-ttu-id="3c348-155">Visio では問題のあるファイルが正常に開かれることがあります。</span><span class="sxs-lookup"><span data-stu-id="3c348-155">Sometimes Visio opens a file successfully even if there are issues with the file.</span></span> <span data-ttu-id="3c348-156">Visio からファイルの問題が確実に通知されるようにするには、ファイル パッケージ レベルで Visio ファイルを操作するソリューションをテストする際に、ファイルを開くときの警告を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-156">To ensure that Visio notifies you of any file issues, you should enable file open warnings when testing solutions that manipulate Visio files at the file package level.</span></span> <span data-ttu-id="3c348-157">> ファイルを開くときの警告を有効にするには、Visio 2013 で、**[ファイル]**、**[オプション]**、**[詳細設定]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-157">> To enable file open warnings, in Visio 2013, choose **File**, **Options**, **Advanced**.</span></span> <span data-ttu-id="3c348-158">**[保存/開く]** から、**[ファイルを開くときの警告を表示する]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-158">Under **Save/Open**, select **Show file open warnings**.</span></span> 
  
<span data-ttu-id="3c348-159">これらの手順では、"Visio Package.vsdx"ファイルを操作するのに Windows コンソール アプリケーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c348-159">These procedures use a Windows console application to manipulate the "Visio Package.vsdx" file.</span></span> <span data-ttu-id="3c348-160">Visual Studio 2012 で新しい Windows コンソール アプリケーションを作成してセットアップするには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="3c348-160">Use the following procedure to create and set up a new Windows console application in Visual Studio 2012.</span></span>
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a><span data-ttu-id="3c348-161">Visual Studio 2012 で新しいソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c348-161">To create a new solution in Visual Studio 2012</span></span>

1. <span data-ttu-id="3c348-162">**[ファイル]** メニューで、**[新規作成]**、**[プロジェクト]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-162">On the **File** menu, choose **New**, **Project**.</span></span>
    
2. <span data-ttu-id="3c348-163">**[新しいプロジェクト]** ダイアログ ボックスで、**[Visual C#]** または **[Visual Basic]** を展開してから、**[Windows]**、**[コンソール アプリケーション]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-163">In the **New Project** dialog box, expand either **Visual C#** or **Visual Basic**, and then choose **Windows**, **Console Application**.</span></span>
    
    <span data-ttu-id="3c348-164">**[名前]** ボックスで、「VisioFileAccessor」と入力し、プロジェクトの場所を選択してから、**[OK]** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-164">In the **Name** box, enter ' VisioFileAccessor', select a location for the project, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="3c348-165">[ **プロジェクト**] メニューの [ **参照の追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-165">On the **Project** menu, choose **Add Reference**.</span></span> 
    
    <span data-ttu-id="3c348-166">**[参照マネージャー]** ダイアログ ボックスで、**[アセンブリ]** の下の **[フレームワーク]** を選択してから、参照を **[System.Xml]** コンポーネントと **[WindowsBase]** コンポーネントに追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-166">In the **Reference Manager** dialog box, under **Assemblies**, choose **Framework**, and then add a reference to the **System.Xml** and **WindowsBase** components.</span></span> 
    
4. <span data-ttu-id="3c348-167">プロジェクトの Program.cs または Module1.vb ファイル内に、次の**使用している** ディレクティブ (Visual Basic の **Imports** ステートメント) を追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-167">In the Program.cs or Module1.vb file for the project, add the following **using** directives (**Imports** statements in Visual Basic):</span></span> 
    
    ```cs
    using System.Xml;
    using System.Xml.Linq;
    using System.IO;
    using System.IO.Packaging;
    using System.Text;
    
    ```

    ```vb
    Imports System.Xml
    Imports System.Xml.Linq
    Imports System.IO
    Imports System.IO.Packaging
    Imports System.Text
    
    ```

5. <span data-ttu-id="3c348-168">同様に、Program.cs または Module1.vb ファイル内の、**Program** クラス (Visual Basic では **Module1**) の **Main** メソッドの末尾の前に、ユーザーがキーを押すまでコンソール アプリケーションの実行を停止する次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-168">Also in the Program.cs or Module1.vb file, before the end of the **Main** method of the **Program** class (**Module1** in Visual Basic), add the following code that stops execution of the console application until the user presses a key.</span></span> 
    
    ```cs
    // This code stops the execution of the console application
    // so you can read the output.
    Console.WriteLine("Press any key to continue ...");
    Console.ReadKey();
    
    ```

    ```vb
    ' This code stops the execution of the console application
    ' so you can read the output.
    Console.WriteLine("Press any key to continue ...")
    Console.ReadKey()
    ```

## <a name="open-a-visio-2013-file-as-a-package"></a><span data-ttu-id="3c348-169">Visio 2013 ファイルをパッケージとして開く</span><span class="sxs-lookup"><span data-stu-id="3c348-169">Open a Visio 2013 file as a package</span></span>
<span data-ttu-id="3c348-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span></span>

<span data-ttu-id="3c348-171">ファイル内のデータを操作するには、その前に [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging.package?view=netframework-4.8) 名前空間に含まれる [Package](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) オブジェクト内のファイルを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-171">Before you can manipulate any of the data within the file, you need to first open the file within a [Package](https://docs.microsoft.com/dotnet/api/system.io.packaging.package?view=netframework-4.8) object, which is contained within the [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8) namespace.</span></span> <span data-ttu-id="3c348-172">**Package** オブジェクトは Visio ファイルを全体として表します。</span><span class="sxs-lookup"><span data-stu-id="3c348-172">The **Package** object represents the Visio file as a whole.</span></span> <span data-ttu-id="3c348-173">ファイル パッケージ内の個々の文書パーツの選択を許可しているメンバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c348-173">It exposes members that allow you to select individual document parts within the file package.</span></span> <span data-ttu-id="3c348-174">特に、**Package** クラスは、ファイルをパッケージとして開くのに使用する静的[Open(String, FileMode, FileAccess)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.open?view=netframework-4.8) メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="3c348-174">In particular, the **Package** class exposes the static [Open(String, FileMode, FileAccess)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.open?view=netframework-4.8) method that you use to open a file as a package.</span></span> <span data-ttu-id="3c348-175">また、作業が終了したらパッケージを閉じるための [Close()](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.close?view=netframework-4.8) メソッドも公開します。</span><span class="sxs-lookup"><span data-stu-id="3c348-175">It also exposes a [Close()](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.close?view=netframework-4.8) method for closing the package once you've finished with it.</span></span> 
  
> [!TIP]
> <span data-ttu-id="3c348-176">最善の方法としては、**using** ブロックを使用して **Package** オブジェクト内の Visio ファイルを開くと、作業終了時にファイル パッケージを明示的に閉じる必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="3c348-176">As a best practice, use a **using** block to open the Visio file in the **Package** object so that you don't have to explicitly close the file package when you're done with it.</span></span> <span data-ttu-id="3c348-177">また、**try/catch/finally** 構造の **Finally** ブロックで **Package.Close** メソッドを明示的に呼び出すこともできます。</span><span class="sxs-lookup"><span data-stu-id="3c348-177">You can also explicitly call the **Package.Close** method in the **finally** block of a **try/catch/finally** construction.</span></span> 
  
<span data-ttu-id="3c348-178">[FileInfo](https://docs.microsoft.com/dotnet/api/system.io.fileinfo?view=netframework-4.8) オブジェクトを使用して「Visio Package.vsdx」ファイルの完全パスを取得し、そのパスを引数として **Package.Open** メソッドに渡してから、呼び出し側のコードに **Package** オブジェクトを返すには、次のコードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-178">Use the following code to get the full path for the "Visio Package.vsdx" file by using a [FileInfo](https://docs.microsoft.com/dotnet/api/system.io.fileinfo?view=netframework-4.8) object, pass the path as an argument to the **Package.Open** method, and then return a **Package** object to the calling code.</span></span> 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a><span data-ttu-id="3c348-179">.vsdx ファイルをパッケージとして開くには</span><span class="sxs-lookup"><span data-stu-id="3c348-179">To open a .vsdx file as a package</span></span>

1. <span data-ttu-id="3c348-180">**Program** クラス (または Visual Basic の **Module1**) 内の **メイン** メソッドの後に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-180">After the **Main** method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static Package OpenPackage(string fileName, 
        Environment.SpecialFolder folder)
    {
        Package visioPackage = null;
        // Get a reference to the location 
        // where the Visio file is stored.
        string directoryPath = System.Environment.GetFolderPath(
            folder);
        DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
        // Get the Visio file from the location.
        FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
        if (fileInfos.Count() > 0)
        {
            FileInfo fileInfo = fileInfos[0];
            string filePathName = fileInfo.FullName;
            // Open the Visio file as a package with
            // read/write file access.
            visioPackage = Package.Open(
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite);
            }
            // Return the Visio file as a package.
            return visioPackage;
    }
    ```

    ```vb
    Private Function OpenPackage(fileName As String, _
        folder As Environment.SpecialFolder) As Package
        Dim visioPackage As Package = Nothing
        ' Get a reference to the location
        ' where the Visio file is stored.
        Dim directoryPath As String = System.Environment.GetFolderPath( _
            folder)
        Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
        ' Get the Visio file from the location.
        Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
        If (fileInfos.Count() > 0) Then
            Dim fileInfo As FileInfo = fileInfos(0)
            Dim filePathName As String = fileInfo.FullName
            ' Open the Visio file as a package 
            ' with read/write access.
            visioPackage = Package.Open( _
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite)
            End If
        ' Return the Visio file as a package.
        Return visioPackage
    End Function
    
    ```

2. <span data-ttu-id="3c348-181">**Program** クラス (または Visual Basic の **Module1**) 内の **メイン** メソッドで、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-181">In the **Main** method of the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    // Open the Visio file in a Package object.
    using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
        Environment.SpecialFolder.Desktop))
    {
    }
    
    ```

    ```vb
    ' Open the Visio file in a Package object.
    Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
        Environment.SpecialFolder.Desktop)
    End Using
    
    ```

## <a name="select-and-read-package-parts-from-a-package"></a><span data-ttu-id="3c348-182">パッケージからパッケージ パーツを選択して読み取る</span><span class="sxs-lookup"><span data-stu-id="3c348-182">Select and read package parts from a package</span></span>
<span data-ttu-id="3c348-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span></span>

<span data-ttu-id="3c348-184">パッケージとして Visio 2013 のファイルを開いたら、**System.IO.Packaging**名前空間に含まれている[PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx)クラスを使用して、ファイルの中のドキュメント パーツにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3c348-184">Once you have the Visio 2013 file open as a package, you can access the document parts within it using the [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) class included in the **System.IO.Packaging** namespace.</span></span> <span data-ttu-id="3c348-185">**PackagePart**オブジェクトは、個別またはコレクションとしてインスタンス化することができます。</span><span class="sxs-lookup"><span data-stu-id="3c348-185">**PackagePart** objects can be instantiated individually or as a collection.</span></span> <span data-ttu-id="3c348-186">**Package** クラスは、 [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) から [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) オブジェクトを取得するための **GetParts()** メソッドと **GetPart(Uri)** メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="3c348-186">The **Package** class exposes a [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) method and a [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) method for getting **PackagePart** objects out of the **Package**.</span></span> <span data-ttu-id="3c348-187">**Package.GetParts** メソッドは[PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) クラスのインスタンスを返します。それにより [IEnumerator\< T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2)インターフェースを実行するほかのコレクションを操作することができます。</span><span class="sxs-lookup"><span data-stu-id="3c348-187">The **Package.GetParts** method returns an instance of the [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) class, which you can then interact with like any other collection that implements the [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2) interface.</span></span> 
  
<span data-ttu-id="3c348-188">**PackagePartCollection** オブジェクトを **Package** からコレクションとして取得し、コレクション内で **PackagePart** オブジェクトを反復処理し、各 **PackagePart** の URI とコンテンツ タイプをコンソールに書き込むには、次の手順のコードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-188">Use the code in the following procedure to get a **PackagePartCollection** object from the **Package** as a collection, iterate through the **PackagePart** objects in the collection, and write the URI and content type of each **PackagePart** to the console.</span></span> 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a><span data-ttu-id="3c348-189">パッケージ内のパッケージ パーツを反復処理するには</span><span class="sxs-lookup"><span data-stu-id="3c348-189">To iterate through the package parts in a package</span></span>

1. <span data-ttu-id="3c348-190">**Program** クラス (または Visual Basic の **Module1**) 内の `OpenPackage` メソッドの後に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-190">After the  `OpenPackage` method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static void IteratePackageParts(Package filePackage)
    {
        
        // Get all of the package parts contained in the package
        // and then write the URI and content type of each one to the console.
        PackagePartCollection packageParts = filePackage.GetParts();
        foreach (PackagePart part in packageParts)
        {
            Console.WriteLine("Package part URI: {0}", part.Uri);
            Console.WriteLine("Content type: {0}", part.ContentType.ToString());
        }
    }
    
    ```

    ```vb
    Private Sub IteratePackageParts(filePackage As Package)
        ' Get all of the package parts contained in the package
        ' and then write the URI and content type of each one to the console.
        Dim packageParts As PackagePartCollection = filePackage.GetParts()
        For Each part In packageParts
            Console.WriteLine("Package part: {0}", part.Uri)
            Console.WriteLine("Content type: {0}", part.ContentType.ToString())
        Next
    End Sub 
    
    ```

2. <span data-ttu-id="3c348-191">**Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-191">Add the following code inside the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic):</span></span> 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. <span data-ttu-id="3c348-192">F5 キーを選択してソリューションをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="3c348-192">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="3c348-193">プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="3c348-193">When the program has completed running, choose any key to exit.</span></span>
    
<span data-ttu-id="3c348-194">コンソール アプリケーションは、次のような出力を生成します (簡潔にするため、出力の一部が省略されています)。</span><span class="sxs-lookup"><span data-stu-id="3c348-194">The console application produces output similar to the following (some of the output has been omitted for brevity):</span></span>
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
<span data-ttu-id="3c348-195">ほとんどの場合、**PackagePart**のいずれかを選択するだけでよく、それらすべてを反復処理する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3c348-195">More often than not, you need to select one **PackagePart** without having to iterate over all of them.</span></span> <span data-ttu-id="3c348-196">**Package** または他の **PackagePart** とのリレーションシップを使用して、**Package**から**PackagePart** オブジェクトを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="3c348-196">You can get a **PackagePart** object from a **Package** by using its relationship to the **Package** or another **PackagePart**.</span></span> <span data-ttu-id="3c348-197">Visio 2013 ファイル形式のリレーションシップは、ドキュメント パーツとファイル パッケージの関係や 2 つのドキュメント パーツの相互の関係を記述した個別のエンティティです。</span><span class="sxs-lookup"><span data-stu-id="3c348-197">A relationship in the Visio 2013 file format is a discrete entity that describes how a document part relates to the file package or how two document parts relate to each other.</span></span> <span data-ttu-id="3c348-198">たとえば、Visio 2013 ファイル パッケージ自体には Visio ドキュメント パーツとのリレーションシップがあり、Visio ドキュメント パーツには Windows のパーツとのリレーションシップがあります。</span><span class="sxs-lookup"><span data-stu-id="3c348-198">For example, the Visio 2013 file package itself has a relationship to its Visio Document part, and the Visio Document part has a relationship to the Windows part.</span></span> <span data-ttu-id="3c348-199">これらのリレーションシップは、[PackageRelationship](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationship?view=netframework-4.8) または [PackageRelationshipCollection](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationshipcollection?view=netframework-4.8) クラスのインスタンスとして表されます。</span><span class="sxs-lookup"><span data-stu-id="3c348-199">These relationships are represented as instances of the [PackageRelationship](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationship?view=netframework-4.8) or [PackageRelationshipCollection](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationshipcollection?view=netframework-4.8) classes.</span></span> 

<span data-ttu-id="3c348-200">**Package**クラスは、**PackageRelationship**または**PackageRelationshipCollection**オブジェクトとして含まれているリレーションシップを取得するいくつかの方法を公開します。</span><span class="sxs-lookup"><span data-stu-id="3c348-200">The **Package** class exposes several methods for getting the relationships that it contains as **PackageRelationship** or **PackageRelationshipCollection** objects.</span></span> <span data-ttu-id="3c348-201">[GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) メソッドを使用して、1 つの特定の種類の **PackageRelationship** オブジェクトを含む **PackageRelationshipCollection** オブジェクトをインスタンス化できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-201">You can use the [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) method to instantiate a **PackageRelationshipCollection** object that contains **PackageRelationship** objects of a single specific type.</span></span> <span data-ttu-id="3c348-202">もちろん、 **Package.GetRelationshipsByType**メソッドを使用するには、必要なリレーションシップの種類が既にわかっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-202">Of course, using the **Package.GetRelationshipsByType** method requires that you already know the relationship type that you need.</span></span> <span data-ttu-id="3c348-203">リレーションシップの種類は、XML 名前空間の形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="3c348-203">Relationship types are strings in XML namespace format.</span></span> <span data-ttu-id="3c348-204">たとえば、Visio の文書パーツのリレーションシップの種類はhttps://schemas.microsoft.com/visio/2010/relationships/documentです。</span><span class="sxs-lookup"><span data-stu-id="3c348-204">For example, the relationship type of the Visio Document part is https://schemas.microsoft.com/visio/2010/relationships/document.</span></span> 
  
<span data-ttu-id="3c348-205">**PackagePart** と **Package** または別の **PackagePart** とのリレーションシップが分かったら (つまり、目的の **PackagePart** を参照する **PackageRelationship** オブジェクトがある場合)、このリレーションシップを使用して、その **PackagePart** の URI を取得できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-205">Once you know the relationship of a **PackagePart** to the **Package** or to another **PackagePart** (that is, you have a **PackageRelationship** object that references the **PackagePart** that you want), you can use that relationship to get the URI of that **PackagePart**.</span></span> <span data-ttu-id="3c348-206">**PackagePart**を返すための**Package.GetPart** メソッドにURIを渡します。</span><span class="sxs-lookup"><span data-stu-id="3c348-206">You then pass the URI to the **Package.GetPart** method to return the **PackagePart**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3c348-207">パッケージ パーツのリレーションシップを取得するステップを迂回し、**Package.GetPart** メソッドと **PackagePart** の URI のみを使用して特定の **PackagePart** への参照を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="3c348-207">You can also get a reference to a specific **PackagePart** by using just the **Package.GetPart** method and the URI of the **PackagePart**, bypassing the step where you get the package part's relationships.</span></span> <span data-ttu-id="3c348-208">しかし、Visio ファイル パッケージ内のパッケージ パーツの一部が、パッケージ内の既定以外の場所に保存されることがあります。</span><span class="sxs-lookup"><span data-stu-id="3c348-208">However, some package parts in the Visio file package can be saved to locations other than their default locations in a package.</span></span> <span data-ttu-id="3c348-209">パッケージ パーツが常にすべてのファイルに対して同じ URI にあるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="3c348-209">You cannot assume that a package part is always located at the same URI for every file.</span></span> <span data-ttu-id="3c348-210">> その代わりに、リレーションシップを使用して個々 の **PackagePart** オブジェクトにアクセスする方法が最善です。</span><span class="sxs-lookup"><span data-stu-id="3c348-210">> Instead, it is a best practice to use relationships to access individual **PackagePart** objects.</span></span> 
  
<span data-ttu-id="3c348-211">パーツを参照する**Package**から **PackageRelationship** を使用して**PackagePart** (Visio ドキュメント パーツ) を取得するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c348-211">Use the following procedure to get a **PackagePart** (the Visio Document part) by using the **PackageRelationship** from the **Package** that references the part.</span></span> 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a><span data-ttu-id="3c348-212">リレーションシップによりパッケージ内の特定のパッケージ パーツを選択するには</span><span class="sxs-lookup"><span data-stu-id="3c348-212">To select a specific package part in the package by relationship</span></span>

1. <span data-ttu-id="3c348-213">`IteratePackageParts`Program\*\* クラス (または Visual Basic の \*\*Module1 \*\*) 内の \*\*メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-213">After the  `IteratePackageParts` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        string relationship)
    {
        
        // Use the namespace that describes the relationship 
        // to get the relationship.
        PackageRelationship packageRel = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart part = null;
        // If the Visio file package contains this type of relationship with 
        // one of its parts, return that part.
        if (packageRel != null)
        {
            // Clean up the URI using a helper class and then get the part.
            Uri docUri = PackUriHelper.ResolvePartUri(
                new Uri("/", UriKind.Relative), packageRel.TargetUri);
            part = filePackage.GetPart(docUri);
        }
        return part;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, relationship As String) _
        As PackagePart
        ' Use the namespace that describes the relationship 
        ' to get the relationship.
        Dim packageRel As PackageRelationship = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
        Dim part As PackagePart = Nothing
        ' If the Visio file package contains this type of relationship with 
        ' one of its parts, return that part.
        If Not IsNothing(packageRel) Then
            ' Clean up the URI using a helper class and then get the part.
            Dim docUri = PackUriHelper.ResolvePartUri( _
                New Uri("/", UriKind.Relative), packageRel.TargetUri)
            part = filePackage.GetPart(docUri)
        End If
        Return part
    End Function
    
    ```

2. <span data-ttu-id="3c348-214">**Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のコードを、次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3c348-214">Replace the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Get a reference to the Visio Document part contained in the file package.
    PackagePart documentPart = GetPackagePart(visioPackage, 
        "https://schemas.microsoft.com/visio/2010/relationships/document");
    
    ```

    ```vb
    ' Get a reference to the Visio Document part contained in the file package.
    Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
        "https://schemas.microsoft.com/visio/2010/relationships/document")
    
    ```

<span data-ttu-id="3c348-215">前述のように、他の**PackagePart**オブジェクトとのリレーションシップを使って**PackagePart**オブジェクトを取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="3c348-215">As mentioned previously, you can also get **PackagePart** objects by using their relationship to other **PackagePart** objects.</span></span> <span data-ttu-id="3c348-216">Visio ドキュメントの場合、複雑さにかかわらずほとんどの **PackagePart** オブジェクトは **Package** とのリレーションシップがないので、この点は重要です。</span><span class="sxs-lookup"><span data-stu-id="3c348-216">This is important because, for a Visio document of any complexity, most of the **PackagePart** objects don't have a relationship to the **Package**.</span></span> <span data-ttu-id="3c348-217">たとえば、ファイル パッケージ内の個々 のページ コンテンツ パーツ (つまり/visio/pages/page1.xml) には、ページ インデックス パーツ (つまり /visio/pages/pages.xml) とのリレーションシップはありますが、ファイル パッケージ自体とのリレーションシップはありません。</span><span class="sxs-lookup"><span data-stu-id="3c348-217">For example, an individual Page Content part in the file package (that is, /visio/pages/page1.xml) has a relationship to the Page Index part (that is, /visio/pages/pages.xml) but not to the file package itself.</span></span> <span data-ttu-id="3c348-218">パッケージ内の個々 のページの正確な URI がわからない場合は、ページ インデックス パーツとのリレーションシップを使用してそのページへの参照を取得できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-218">If you don't have the exact URI of the individual page in the package, you can use its relationship to the Page Index part to get a reference to it.</span></span>
  
<span data-ttu-id="3c348-219">**PackagePart** クラスは、1つの種類の[ PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx)オブジェクトだけを含む **PackageRelationshipCollection** オブジェクトを返すために使用できる **GetRelationshipsByType(String)** メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="3c348-219">The **PackagePart** class exposes a [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) method that you can use to return a **PackageRelationshipCollection** object that contains only one type of **PackageRelationship** object.</span></span> <span data-ttu-id="3c348-220">**PackageRelationshipCollection** を取得したら、コレクションから必要な **PackageRelationship** を選び、**PackagePart** オブジェクトを参照できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-220">Once you have the **PackageRelationshipCollection**, you can select the **PackageRelationship** that you need from the collection and then reference the **PackagePart** object.</span></span> 
  
<span data-ttu-id="3c348-221">別の **PackagePart** との（**PackageRelationship** オブジェクトから取得する）リレーションシップによって **Package** から \*\* PackagePart\*\* を取得するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c348-221">Use the following code to get a **PackagePart** from the **Package** by using its relationship to (getting a **PackageRelationship** object from) another **PackagePart**.</span></span>
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a><span data-ttu-id="3c348-222">別のパッケージ パーツとのリレーションシップを利用して特定のパッケージ パーツを選択するには</span><span class="sxs-lookup"><span data-stu-id="3c348-222">To select a specific package part through its relationship to another package part</span></span>

1. <span data-ttu-id="3c348-223">`GetPackagePart`Program\*\* クラス (または Visual Basic の \*\*Module1 \*\*) 内の \*\*メソッドの後に、次のオーバーロード メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-223">After the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following overload method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        PackagePart sourcePart, string relationship)
    {
        // This gets only the first PackagePart that shares the relationship
        // with the PackagePart passed in as an argument. You can modify the code
        // here to return a different PackageRelationship from the collection.
        PackageRelationship packageRel = 
            sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart relatedPart = null;
        if (packageRel != null)
        {
            // Use the PackUriHelper class to determine the URI of PackagePart
            // that has the specified relationship to the PackagePart passed in
            // as an argument.
            Uri partUri = PackUriHelper.ResolvePartUri(
                sourcePart.Uri, packageRel.TargetUri);
            relatedPart = filePackage.GetPart(partUri);
        }
        return relatedPart;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, 
        sourcePart As PackagePart, relationship As String) As PackagePart
        ' This gets only the first PackagePart that shares the relationship
        ' with the PackagePart passed in as an argument. You can modify the
        ' code to return a different PackageRelationship from the collection.
        Dim packageRel As PackageRelationship = sourcePart. _
            GetRelationshipsByType(relationship).FirstOrDefault()
        Dim relatedPart As PackagePart = Nothing
        If Not IsNothing(packageRel) Then
            ' Use the PackUriHelper class to determine the URI of the 
            ' PackagePart that has the specified relationship to the 
            ' PackagePart passed in as an argument.
            Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
                sourcePart.Uri, packageRel.TargetUri)
            relatedPart = filePackage.GetPart(partUri)
        End If
        Return relatedPart
    End Function
    ```

2. <span data-ttu-id="3c348-224">**Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-224">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> <span data-ttu-id="3c348-225">(前の手順で追加したコードを削除しないでください。)</span><span class="sxs-lookup"><span data-stu-id="3c348-225">(Do not delete the code that you added in the previous procedure.)</span></span> 
    
    ```cs
    // Get a reference to the collection of pages in the document, 
    // and then to the first page in the document.
    PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/pages");
    PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/page");
    
    ```

    ```vb
    ' Get a reference to the collection of pages in the document,
    ' and then to the first page in the document.
    Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/pages") 
    Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/page") 
    ```

<span data-ttu-id="3c348-226">ドキュメント パーツに含まれている XML に変更を加えるには、その前にまず [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) クラスか [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) クラスを使用して、その XML を閲覧できるようにするオブジェクト内に XML ドキュメントを読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-226">Before you can make changes to the XML included in a document part, you need to first load the XML document into an object that allows you to read the XML, using the [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) class or [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) class.</span></span> <span data-ttu-id="3c348-227">両方のクラスとも、XML ドキュメント内に含まれる XML 要素の選択、属性の作成と読み書き、新しい XML 要素のドキュメント内への挿入などのタスクに関するメソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="3c348-227">Both classes expose methods for tasks such as selecting XML elements contained within the XML documents; creating, reading, and writing attributes; and inserting new XML elements into a document.</span></span> 
  
<span data-ttu-id="3c348-228">2 つの**XDocument**クラスでは、LINQ を使用して XML をクエリすることができます。</span><span class="sxs-lookup"><span data-stu-id="3c348-228">Of the two, the **XDocument** class allows you to query the XML using LINQ.</span></span> <span data-ttu-id="3c348-229">LINQ を使用すると、コレクション内のすべての要素を反復処理して必要な要素をテストしたりしなくても、クエリを作成することにより個々の要素を XML ドキュメントから簡単に選択できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-229">With LINQ, you can easily select individual elements from an XML document by creating queries, rather than iterating over all of the elements in a collection and testing for the elements that you need.</span></span> <span data-ttu-id="3c348-230">この理由で、この記事の次の手順では **XDocument** クラスと **System.Xml.Linq** 名前空間の他のクラスを使用して XML を処理します。</span><span class="sxs-lookup"><span data-stu-id="3c348-230">For these reasons, the following procedures in this article use the **XDocument** class and other classes of the **System.Xml.Linq** namespace for working with XML.</span></span> 
  
<span data-ttu-id="3c348-231">**XDocument** オブジェクト内の XML ドキュメントとして **PackagePart** を開くには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c348-231">Use the following procedure to open a **PackagePart** as an XML document in an **XDocument** object.</span></span> 
  
### <a name="to-read-the-xml-in-a-package-part"></a><span data-ttu-id="3c348-232">パッケージ パーツ内の XML を読み取るには</span><span class="sxs-lookup"><span data-stu-id="3c348-232">To read the XML in a package part</span></span>

1. <span data-ttu-id="3c348-233">**Program** クラス (Visual Basic では **Module1**) 内の`GetPackagePart`メソッドの最後のオーバー ロードの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-233">After the last overload for the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static XDocument GetXMLFromPart(PackagePart packagePart)
    {
        XDocument partXml = null;
        // Open the packagePart as a stream and then 
        // open the stream in an XDocument object.
        Stream partStream = packagePart.GetStream();
        partXml = XDocument.Load(partStream);
        return partXml;
    }
    ```

    ```vb
    Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
        Dim partXml As XDocument = Nothing
        ' Open the packagePart as a stream and then
        ' open the stream in an an XDocument object.
        Dim partStream As Stream = packagePart.GetStream()
        partXml = XDocument.Load(partStream)
        Return partXml
    End Function
    ```

2. <span data-ttu-id="3c348-234">**Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-234">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a><span data-ttu-id="3c348-235">パッケージ パーツ内の XML データを選択して変更する</span><span class="sxs-lookup"><span data-stu-id="3c348-235">Select and change XML data in a package part</span></span>
<span data-ttu-id="3c348-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span></span>

<span data-ttu-id="3c348-237">**XDocument** オブジェクト内にドキュメント パーツを読み込み終えたら、LINQ を使用して、XML 要素を選択し、XML ドキュメントに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="3c348-237">Once you have loaded a document part into an **XDocument** object, you can use LINQ to select XML elements and make changes to the XML document.</span></span> <span data-ttu-id="3c348-238">XML データを変更、追加またはデータを削除することができます。その後、文書パーツに XML ドキュメントを保存できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-238">You can change XML data, add or remove data, and then save the XML document back to the document part.</span></span> 
  
<span data-ttu-id="3c348-239">Visio ファイル形式の操作に関する最も一般的なタスクは、ドキュメント内の特定の XML 要素か要素のコレクションを選択することです。</span><span class="sxs-lookup"><span data-stu-id="3c348-239">The most common task for manipulating the Visio file format is selecting specific XML elements or collections of elements in the document.</span></span> <span data-ttu-id="3c348-240">**System.Xml.Linq** 名前空間には、XML 要素を表す [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) クラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c348-240">The **System.Xml.Linq** namespace includes the [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) class, which represents an XML element.</span></span> <span data-ttu-id="3c348-241">**XElement** クラスは、 Visio ファイルに含まれるデータにきめ細かいレベルで (たとえば、個々の **Shape** 要素から **ValidationRule** 要素に至るまで) アクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3c348-241">The **XElement** class gives you access to the data contained in the Visio file at a granular level, from individual **Shape** elements to **ValidationRule** elements (as examples).</span></span> 
  
<span data-ttu-id="3c348-242">**Shape** 要素を **XDocument** (ページ コンテンツ パーツを含む) から選択してから、特定の **Shape** 要素を選択するには、次のコードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-242">Use the following code to select the **Shape** elements from an **XDocument** (containing a Page Contents part) and to then select a specific **Shape** element.</span></span> 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a><span data-ttu-id="3c348-243">パッケージ パーツ内の特定の要素を選択するには</span><span class="sxs-lookup"><span data-stu-id="3c348-243">To select a specific element in a package part</span></span>

1. <span data-ttu-id="3c348-244">`GetXMLFromPart`Program\*\* クラス (または Visual Basic の \*\*Module1 \*\*) 内の \*\*メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-244">After the  `GetXMLFromPart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
        
    ```cs
    private static IEnumerable<XElement> GetXElementsByName(
        XDocument packagePart, string elementType)
    {
        // Construct a LINQ query that selects elements by their element type.
        IEnumerable<XElement> elements = 
            from element in packagePart.Descendants() 
            where element.Name.LocalName == elementType 
            select element;
        // Return the selected elements to the calling code.
        return elements.DefaultIfEmpty(null);
    }
    
    ```

    ```vb
    Private Function GetXElementsByName(partXML As XDocument, _
        elementType As String) As IEnumerable(Of XElement)
        ' Construct a LINQ query that selects elements by their element type.
        Dim elements As IEnumerable(Of XElement) =
            From element In partXML.Descendants()
            Where element.Name.LocalName = elementType
            Select element
        ' If there aren't any elements of the specified type
        ' in the document, return Nothing to the calling code.
        Return elements.DefaultIfEmpty(Nothing)
    End Function
    ```

2. <span data-ttu-id="3c348-245">前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `GetXElementsByName` メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-245">After the  `GetXElementsByName` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
        string attributeName, string attributeValue) 
    {
        // Construct a LINQ query that selects elements from a group
        // of elements by the value of a specific attribute.
        IEnumerable<XElement> selectedElements = 
            from el in elements
            where el.Attribute(attributeName).Value == attributeValue
            select el;
        // If there aren't any elements of the specified type
        // with the specified attribute value in the document,
        // return null to the calling code.
        return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
    }
    ```

    ```vb
    Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
        attributeName As String, attributeValue As String) As XElement
        ' Construct a LINQ query that selects elements from a group
        ' of elements by the value of a specific attribute.
        Dim selectedElements As IEnumerable(Of XElement) =
            From el In elements
            Where el.Attribute(attributeName).Value = attributeValue
            Select el
        ' If there aren't any elements of the specified type 
        ' with the specified attribute value in the document,
        ' return Nothing to the calling code.
        Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
    End Function
    
    ```

3. <span data-ttu-id="3c348-246">**Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-246">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Get all of the shapes from the page by getting
    // all of the Shape elements from the pageXML document.
    IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
    // Select a Shape element from the shapes on the page by 
    // its name. You can modify this code to select elements
    // by other attributes and their values.
    XElement startEndShapeXML = 
        GetXElementByAttribute(shapesXML, "NameU", "Start/End");
    
    ```

    ```vb
    ' Get all of the shapes from the page by getting
    ' all of the Shape elements from the pageXML document.
    Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
        pageXML, "Shape")
    ' Select a Shape element from the shapes on the page by
    ' its name. You can modify this code to select elements
    ' by other attributes and their values.
    Dim startEndShapeXML As XElement = GetXElementByAttribute( _
        shapesXML, "NameU", "Start/End")
    ```

<span data-ttu-id="3c348-247">**XDocument** オブジェクト内に含まれる **XElement** オブジェクトへの参照を取得し終えたら、他の XML データと同様に操作できるので、Visio ファイル内に含まれるデータを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-247">Once you have gotten a reference to a **XElement** object contained within an **XDocument** object, you can manipulate it like any other XML data and, thereby, change the data contained in the Visio file.</span></span> <span data-ttu-id="3c348-248">たとえば、Visio で開いている図形にテキストがある場合、対応する **Shape** 要素には 1 つ以上の **Text** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c348-248">For example, if a shape has text when it is opened in Visio, the corresponding **Shape** element will contain at least one **Text** element.</span></span> <span data-ttu-id="3c348-249">この **Text** 要素の値を変更すると、Visio でファイルを表示する際に、この図形のテキストは変更されます。</span><span class="sxs-lookup"><span data-stu-id="3c348-249">If you change the value of that **Text** element, the shape's text is changed when the file is viewed in Visio.</span></span> 
  
<span data-ttu-id="3c348-250">開始/終了図形内のテキストを「Begin process」から「Start process」に変更するには、**Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-250">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) to change the text in the Start/End shape from "Begin process" to "Start process".</span></span> 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> <span data-ttu-id="3c348-251">上記のコード例で、既存の図形のテキストと置き換える文字列の文字数は同じです。</span><span class="sxs-lookup"><span data-stu-id="3c348-251">In the previous code example, the existing shape text and the string used to replace it have the same number of characters.</span></span> <span data-ttu-id="3c348-252">また、LINQ クエリは、返される要素の最後の子ノード (この例ではテキスト ノード) の値を変更することにもご注意ください。</span><span class="sxs-lookup"><span data-stu-id="3c348-252">Also note that the LINQ query changes the value of the last child node of the returned element (which, in this case, is a text node).</span></span> <span data-ttu-id="3c348-253">これは、**テキスト**要素の子である **cp** 要素の設定を変更しないようにするため行われます。</span><span class="sxs-lookup"><span data-stu-id="3c348-253">This is done to avoid changing the settings of the **cp** element that is a child of the **Text** element.</span></span> <span data-ttu-id="3c348-254">>**Text** 要素のすべての子を上書きする方法でプログラムによって図形のテキストを変更すると、ファイルが不安定になることがあります。</span><span class="sxs-lookup"><span data-stu-id="3c348-254">> It is possible to cause file instability if you alter shape text programmatically by overwriting all children of the **Text** element.</span></span> <span data-ttu-id="3c348-255">上記の例のように、テキストの書式はファイル内の **Text** 要素の下の **cp** 要素で表されます。</span><span class="sxs-lookup"><span data-stu-id="3c348-255">As in the example above, the text formatting is represented by **cp** elements under the **Text** element in the file.</span></span> <span data-ttu-id="3c348-256">書式設定の定義は、親 **Section** 要素に格納されています。</span><span class="sxs-lookup"><span data-stu-id="3c348-256">The definition of the formatting is stored in the parent **Section** element.</span></span> <span data-ttu-id="3c348-257">これら 2 つの情報が整合していないと、ファイルは正常に動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-257">If these two pieces of information become inconsistent, then the file may not behave as expected.</span></span> <span data-ttu-id="3c348-258">Visio は不整合の多くを修復しますが、プログラムによる変更が一貫しており、ファイルの最終的な動作が制御されているか確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3c348-258">Visio heals many inconsistencies, but it is better to ensure that any programmatic changes are consistent so that you are controlling the ultimate behavior of the file.</span></span> 
  
<span data-ttu-id="3c348-p126">ドキュメント パーツの XML に変更を加える場合、その変更内容はメモリ内のみに存在します。ファイル内に変更を保持するには、ドキュメント パーツに XML を戻して保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-p126">When you make changes to the XML of a document part, those changes exist in memory only. To persist the changes in the file, you must save the XML back to the document part.</span></span>
  
<span data-ttu-id="3c348-261">次のコードは、[XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) クラスと [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) クラスを使用して XML をパッケージ パーツに書き戻します。</span><span class="sxs-lookup"><span data-stu-id="3c348-261">The following code uses the [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) class and [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) class to write the XML back to the package part.</span></span> <span data-ttu-id="3c348-262">[Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) メソッドを使用して XML をパーツに戻して保存できますが、**XmlWriter** クラスと **XmlWriterSettings** クラスを使用するとエンコードの種類を指定するなど、出力をより細かく制御できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-262">Although you can use the [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) method to save the XML back to the part, the **XmlWriter** and **XmlWriterSettings** classes allow you finer control over the output, including specifying the type of encoding.</span></span> <span data-ttu-id="3c348-263">**XDocument** クラスは、**XmlWriter** オブジェクトを利用して XML をストリームに書き戻す [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="3c348-263">The **XDocument** class exposes a [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) method that takes an **XmlWriter** object and writes XML back to a stream.</span></span> 
  
<span data-ttu-id="3c348-264">XML を Visio ページからページ コンテンツ パーツに戻して保存するには、次の手順を使用してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-264">Use the following procedure to save the XML from the Visio page back to the Page Contents part.</span></span>
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a><span data-ttu-id="3c348-265">変更した XML をパッケージに戻して保存するには</span><span class="sxs-lookup"><span data-stu-id="3c348-265">To save the changed XML back to the package</span></span>

1. <span data-ttu-id="3c348-266">前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `GetXElementByAttribute` メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-266">After the  `GetXElementByAttribute` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void SaveXDocumentToPart(PackagePart packagePart, 
        XDocument partXML)
    {
        
        // Create a new XmlWriterSettings object to 
        // define the characteristics for the XmlWriter
        XmlWriterSettings partWriterSettings = new XmlWriterSettings();
        partWriterSettings.Encoding = Encoding.UTF8;
        // Create a new XmlWriter and then write the XML
        // back to the document part.
        XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
            partWriterSettings);
        partXML.WriteTo(partWriter);
        // Flush and close the XmlWriter.
        partWriter.Flush();
        partWriter.Close();
    }
    ```

    ```vb
    Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
        partXML As XDocument)
        ' Create a new XmlWriterSettings object to 
        ' define the characteristics for the XmlWriter.
        Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
        partWriterSettings.Encoding = Encoding.UTF8
        ' Create a new XmlWriter and then write the XML
        ' back to the document part.
        Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
        partXML.WriteTo(partWriter)
        ' Flush and close the XmlWriter.
        partWriter.Flush()
        partWriter.Close()
    End Sub
    ```

2. <span data-ttu-id="3c348-267">**Program** クラスの **Main** メソッド内の **using**  ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) の、前の手順のコードの下に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-267">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. <span data-ttu-id="3c348-268">F5 キーを選択してソリューションをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="3c348-268">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="3c348-269">プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="3c348-269">When the program has completed running, choose any key to exit.</span></span>
    
4. <span data-ttu-id="3c348-270">Visio 2013 で Visio Package.vsdx ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="3c348-270">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="3c348-271">この時点で開始/終了図形にテキスト「Start process」が含まれているはずです。</span><span class="sxs-lookup"><span data-stu-id="3c348-271">The Start/End shape should now contain the text "Start process".</span></span>
  
## <a name="recalculate-data-in-the-file"></a><span data-ttu-id="3c348-272">ファイル内のデータを再計算する</span><span class="sxs-lookup"><span data-stu-id="3c348-272">Recalculate data in the file</span></span>
<span data-ttu-id="3c348-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span></span>

<span data-ttu-id="3c348-274">ファイル内のデータの変更には、ファイルを開いたときに、Visio で文書を再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-274">Some changes to the data in a file may require Visio to recalculate the document when it opens the file.</span></span> <span data-ttu-id="3c348-275">Visio はダイアグラム、特に、図形のリレーションシップ（つまり、ある図形が別の図形に依存する場合）や接続する図形などに多くのロジックを提供します。</span><span class="sxs-lookup"><span data-stu-id="3c348-275">Visio provides a lot of logic for a diagram, particularly for shape relationships (that is, when one shape depends on another) and connecting shapes.</span></span> <span data-ttu-id="3c348-276">カスタム ロジックで使用されるデータのいずれかを変更すると、Visio はファイル内で影響を受けるすべての集計データに変更を反映する 必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-276">If any of the data that the custom logic relies upon is changed, Visio needs to propagate the changes to all of the affected calculated data in the file.</span></span> 
  
<span data-ttu-id="3c348-277">Visio 2013 ファイル形式には、ファイル内のデータの再計算に使用できる手法がいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c348-277">The Visio 2013 file format includes a couple of techniques that you can use to recalculate data in the file.</span></span> <span data-ttu-id="3c348-278">次の 3 種類のシナリオは、Visio ファイルを再計算する必要があるかどうかと、再計算の方法を決めるときに考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-278">There are three types of scenarios that you must consider when you decide whether you need to recalculate the Visio file and how to do it:</span></span>
  
- <span data-ttu-id="3c348-279">データへの変更は、ファイル形式におけるその他の値には影響しません。</span><span class="sxs-lookup"><span data-stu-id="3c348-279">The changes to the data do not affect any other values in the file format.</span></span> <span data-ttu-id="3c348-280">ドキュメントを再計算する命令を Visio に追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3c348-280">You don't need to add any additional instructions to Visio to recalculate the document.</span></span> <span data-ttu-id="3c348-281">既に示したように、ドキュメントの再計算を実行せずに、図形のテキストを頻繁に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-281">As demonstrated previously, you can often change a shape's text without needing to recalculate the document.</span></span>
    
- <span data-ttu-id="3c348-282">データへの変更が XML 内のシェイプシート セルの値の変更に限定されており、このデータに依存している他のシェイプシート値がある場合。</span><span class="sxs-lookup"><span data-stu-id="3c348-282">The changes to the data are limited to changing the values of ShapeSheet cells in the XML, and there are other ShapeSheet values that depend on this data.</span></span> <span data-ttu-id="3c348-283">この場合、([XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) クラスを使用して) XML 処理命令を、変更された **Cell** 要素に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-283">In this case, you must add an XML processing instruction (using the [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) class) to the **Cell** element that has been changed.</span></span> <span data-ttu-id="3c348-284">たとえば、図形の **ThemeIndex**セルは、図形に含まれるその他いくつかの ShapeSheet セルの値に影響します。</span><span class="sxs-lookup"><span data-stu-id="3c348-284">For example, the **ThemeIndex** cell for a shape affects the values of several other ShapeSheet cells contained in the shape.</span></span> <span data-ttu-id="3c348-285">ファイル自体の **ThemeIndex** セル (たとえば、**N** 値が「ThemeIndex」の **Cell** 要素) を変更する場合、依存している値が更新されるように、**Cell** 要素に処理命令を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-285">If you change the **ThemeIndex** cell within the file itself (for example, the **Cell** element with an **N** value of "ThemeIndex"), you will need to add a processing instruction to the **Cell** element so that the dependent values are updated.</span></span> 
    
- <span data-ttu-id="3c348-286">データへの変更がコネクタの位置つまり接続ポイントに影響する場合。</span><span class="sxs-lookup"><span data-stu-id="3c348-286">The changes to the data affect the location of a connector or connection points.</span></span> <span data-ttu-id="3c348-287">別の状況として、シェイプシートのデータに多数の変更があり、(変更ごとに個別に処理命令を追加するのではなく) 1 つの命令でドキュメント全体を再計算しようとする場合もあります。</span><span class="sxs-lookup"><span data-stu-id="3c348-287">Another situation is when there are many changes to the ShapeSheet data and you want to recalculate the whole document with one instruction (rather than adding individual processing instructions for each change).</span></span> <span data-ttu-id="3c348-288">この場合、ドキュメントを開くときにそのドキュメント全体を再計算するように Visio に命令できます。</span><span class="sxs-lookup"><span data-stu-id="3c348-288">In this case you can instruct Visio to recalculate the entire document when it is opened.</span></span> <span data-ttu-id="3c348-289">そのためには、**RecalcDocument** プロパティを Visio パッケージのカスタム ファイル プロパティ パーツ (/docProps/custom.xml) に追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-289">You do this by adding a **RecalcDocument** property to the Custom File Properties part (/docProps/custom.xml) of the Visio package.</span></span> <span data-ttu-id="3c348-290">この種のシナリオの例としては、接続された図の中の図形の位置やサイズを調整する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-290">Adjusting the position or size of shapes in a connected diagram is an example of this type of scenario.</span></span> 
    
    <span data-ttu-id="3c348-291">パフォーマンスの観点からは、このシナリオが最もコストがかかるオプションであることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-291">Keep in mind that this is the most costly option from a performance standpoint.</span></span>
    
<span data-ttu-id="3c348-292">**Cell** 要素を **Shape** 要素内に挿入し、この新しい値のために同じ **Shape** 内の他の **Cell** 要素を再計算する必要がある場合には、次の手順を使用してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-292">Use the following procedure to insert a **Cell** element into a **Shape** element, where other **Cell** elements in the same **Shape** need to be recalculated because of the new value.</span></span> <span data-ttu-id="3c348-293">新しい **Cell** 要素には、ローカルな再計算を実行する必要があることを Visio に通知する処理命令が子要素として組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="3c348-293">The new **Cell** element includes a processing instruction as a child element, to inform Visio that it needs to perform some local recalculation.</span></span> 
  
### <a name="to-recalculate-values-for-a-single-shape"></a><span data-ttu-id="3c348-294">1 つの図形の値を再計算するには</span><span class="sxs-lookup"><span data-stu-id="3c348-294">To recalculate values for a single shape</span></span>

1. <span data-ttu-id="3c348-295">前述の 2 つの例 (図形のテキストの変更および `SaveXDocumentToPart`に対する呼び出し) の、**Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のコードを、次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3c348-295">Replace the code from the previous two examples (changing the shape's text and the call to  `SaveXDocumentToPart`) in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Insert a new Cell element in the Start/End shape that adds an arbitrary
    // local ThemeIndex value. This code assumes that the shape does not 
    // already have a local ThemeIndex cell.
    startEndShapeXML.Add(new XElement("Cell",
        new XAttribute("N", "ThemeIndex"),
        new XAttribute("V", "25"),
        new XProcessingInstruction("NewValue", "V")));
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Insert a new Cell element in the shape that adds an arbitrary local
    ' ThemeIndex value. This code assumes that the shape does not
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. <span data-ttu-id="3c348-296">F5 キーを選択してソリューションをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="3c348-296">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="3c348-297">プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="3c348-297">When the program has completed running, choose any key to exit.</span></span>
    
3. <span data-ttu-id="3c348-298">Visio 2013 で Visio Package.vsdx ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="3c348-298">Open the Visio Package.vsdx file in Visio 2013.</span></span> <span data-ttu-id="3c348-299">開始/終了図形の塗りつぶしの色が変わっているはずです。</span><span class="sxs-lookup"><span data-stu-id="3c348-299">The Start/End shape should now have a different fill color.</span></span>
    
<span data-ttu-id="3c348-300">図形の色は**ThemeIndex**セルの値により異なります。図形がどのアクティブなテーマを継承するかによって決まります。</span><span class="sxs-lookup"><span data-stu-id="3c348-300">The shape's color relies on the value of the **ThemeIndex** cell—it determines which of the active themes the shape inherits from.</span></span> <span data-ttu-id="3c348-301">前の例では、図形は別のテーマを継承する設定 (**ThemeIndex**セルが「25」の値に設定)になっています。</span><span class="sxs-lookup"><span data-stu-id="3c348-301">In the previous example, the shape is set to inherit from a different theme (the **ThemeIndex** cell is set to a value of "25").</span></span> <span data-ttu-id="3c348-302">処理命令を使用しない場合は、図形のテキストの色（同様に **ThemeIndex**セルの影響を受けます）は再計算されません。</span><span class="sxs-lookup"><span data-stu-id="3c348-302">If you don't use a processing instruction, the shape's text color—which is also affected by the **ThemeIndex** cell—isn't recalculated.</span></span> <span data-ttu-id="3c348-303">図形の塗りつぶしの色が白に変更されますが、テキストの色は白のままで、テキストは読み取り不可能な状態になります。</span><span class="sxs-lookup"><span data-stu-id="3c348-303">The shape's fill color would change to white, but its text would remain white—leaving the text unreadable.</span></span> <span data-ttu-id="3c348-304">また、処理命令を使用しない場合、ファイルは図形の書式設定の値が予期せず更新される可能性のある不安定な状態のままで、Visio が図形を更新するのは後日になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-304">Also, without the processing instruction, it is possible that Visio may update the shape at a later date, leaving the file in an unstable state where the formatting values of the shape could be updated unpredictably.</span></span> 
  
<span data-ttu-id="3c348-305">Visio でドキュメントを再計算する必要があるファイル内のデータを変更する場合は (たとえば、接続されている図形の位置を変更するので、コネクタを再接続する必要がある場合)、Visio ファイルに再計算の命令を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-305">If you change data in the file that requires Visio to recalculate the document (for example, changing a connected shape's position and, therefore, forcing the connectors to reroute), you must add a recalculation instruction to the Visio file.</span></span> <span data-ttu-id="3c348-306">この命令を作成するには、**name** 属性値が「RecalcDocument」の **property** 要素を Visio ファイル パッケージのカスタム ファイル プロパティ パーツの XML に追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-306">The instruction is created by adding a **property** element with a **name** attribute value of "RecalcDocument" to the XML of the Custom File Properties part of the Visio file package.</span></span> <span data-ttu-id="3c348-307">最善の方法として、カスタム ファイル プロパティ パーツをチェックして、ファイル内で「RecalcDocument」命令が既に登録されていないか確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-307">As a best practice, you should check the Custom File Properties part to be sure that a "RecalcDocument" instruction hasn't already been registered in the file.</span></span> 
  
<span data-ttu-id="3c348-308">前の例から、開始/終了図形の**PinY** セルの値を変更するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c348-308">Use the following code to change the value of the **PinY** cell of the Start/End shape from the previous examples.</span></span> <span data-ttu-id="3c348-309">このコードは、**N** 属性の値を使用して、**XElement**  オブジェクトとして**PinY** セルのデータを含む **Cell** 要素 を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-309">The code selects the **Cell** element that contains the **PinY** cell data as an **XElement** object by using the value of its **N** attribute.</span></span> <span data-ttu-id="3c348-310">その後このコードは、再計算の命令を Visio ファイルのカスタム ファイル プロパティ パーツに追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-310">The code then adds a recalculation instruction to the Custom File Properties part of the Visio file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3c348-311">このコードは、以前に作成した `GetPackagePart` メソッドと `SaveXDocumentToPart` メソッドに依存しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-311">This code relies on the  `GetPackagePart` and  `SaveXDocumentToPart` methods created previously.</span></span> 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a><span data-ttu-id="3c348-312">ドキュメントが開いている場合にそのドキュメント全体を再計算するには</span><span class="sxs-lookup"><span data-stu-id="3c348-312">To recalculate the entire document when it is opened</span></span>

1. <span data-ttu-id="3c348-313">前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `SaveXDocumentToPart` メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-313">After the  `SaveXDocumentToPart` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "https://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
            "custom-properties");
        XDocument customPartXML = GetXMLFromPart(customPart);
        // Check to see whether document recalculation has already been 
        // set for this document. If it hasn't, use the integer
        // value returned by CheckForRecalc as the property ID.
        int pidValue = CheckForRecalc(customPartXML);
        if (pidValue > -1)
        {
            XElement customPartRoot = customPartXML.Elements().ElementAt(0);
            // Two XML namespaces are needed to add XML data to this 
            // document. Here, we're using the GetNamespaceOfPrefix and 
            // GetDefaultNamespace methods to get the namespaces that 
            // we need. You can specify the exact strings for the 
            // namespaces, but that is not recommended.
            XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
            XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
            // Construct the XML for the new property in the XDocument.Add method.
            // This ensures that the XNamespace objects will resolve properly, 
            // apply the correct prefix, and will not default to an empty namespace.
            customPartRoot.Add(
                new XElement(customPropsSchemaNS + "property",
                    new XAttribute("pid", pidValue.ToString()),
                    new XAttribute("name", "RecalcDocument"),
                    new XAttribute("fmtid", 
                        "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                    new XElement(customVTypesNS + "bool", "true")
                ));
        }
        // Save the Custom Properties package part back to the package.
        SaveXDocumentToPart(customPart, customPartXML);
    }
    ```

    ```vb
    Private Sub RecalcDocument(filePackage As Package)
            ' Get the Custom File Properties part from the package and
            ' then extract the XML from it.
            Dim customPart As PackagePart = GetPackagePart(filePackage, _
                "https://schemas.openxmlformats.org/officeDocument/2006/" + _
                "relationships/custom-properties")
            Dim customPartXML As XDocument = GetXMLFromPart(customPart)
            ' Check to see whether document recalculation has already been
            ' set for this document. If it hasn't, use the integer
            ' value returned by CheckForRecalc as the property ID.
            Dim pidValue As Integer = CheckForRecalc(customPartXML)
            If (pidValue > 1) Then
                Dim customPartRoot As XElement = _
                    customPartXML.Elements().ElementAt(0)
                ' Two XML namespaces are needed to add XML data to this 
                ' document. Here, we're using the GetNamespaceOfPrefix and
                ' GetDefaultNamespace methods to get the namespaces that
                ' we need. You can specify the exact strings for the 
                ' namespaces, but that is not recommended.
                Dim customVTypesNS As XNamespace = _
                    customPartRoot.GetNamespaceOfPrefix("vt")
                Dim customPropsSchemaNS As XNamespace = _
                    customPartRoot.GetDefaultNamespace()
                ' Contruct the XML for the new property in the XDocument.Add
                ' method. This ensures that the XML namespaces resolve 
                ' properly, apply the correct prefix, and do not default to 
                ' an empty namespace.
                customPartRoot.Add( _
                    New XElement(customPropsSchemaNS + "property", _
                        New XAttribute("pid", pidValue.ToString()), _
                        New XAttribute("name", "RecalcDocument"), _
                        New XAttribute("fmtid", _
                            "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                        New XElement(customVTypesNS + "bool", "true") _
                ))
            ' Save the Custom Properties package part back to the package.
            SaveXDocumentToPart(customPart, customPartXML)
            End If
        End Sub
    ```

2. <span data-ttu-id="3c348-314">前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `RecalcDocument` メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-314">After the  `RecalcDocument` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static int CheckForRecalc(XDocument customPropsXDoc) 
    {
        
        // Set the inital pidValue to -1, which is not an allowed value.
        // The calling code tests to see whether the pidValue is 
        // greater than -1.
        int pidValue = -1;
        // Get all of the property elements from the document. 
        IEnumerable<XElement> props = GetXElementsByName(
            customPropsXDoc, "property");
        // Get the RecalcDocument property from the document if it exists already.
        XElement recalcProp = GetXElementByAttribute(props, 
            "name", "RecalcDocument");
        // If there is already a RecalcDocument instruction in the 
        // Custom File Properties part, then we don't need to add another one. 
        // Otherwise, we need to create a unique pid value.
        if (recalcProp != null)
        {
            return pidValue;
        }
        else
        {
            // Get all of the pid values of the property elements and then
            // convert the IEnumerable object into an array.
            IEnumerable<string> propIDs = 
                from prop in props
                where prop.Name.LocalName == "property"
                select prop.Attribute("pid").Value;
            string[] propIDArray = propIDs.ToArray();
            // Increment this id value until a unique value is found.
            // This starts at 2, because 0 and 1 are not valid pid values.
            int id = 2;
            while (pidValue == -1)
            {
                if (propIDArray.Contains(id.ToString()))
                {
                    id++;
                }
                else
                {
                    pidValue = id;
                }
            }
        }
        return pidValue;
    }
    
    ```

    ```vb
    Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
        ' Set the initial pidValue to -1, which is not an allowed value. 
        ' The calling code test to see whether the pidValue is
        ' greater than -1.
        Dim pidValue As Integer = -1
        ' Get all of the property elements from the document.
        Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
            customPropsXDoc, "property")
        ' Get the RecalcDocument property from the document if 
        ' it exists already.
        Dim recalcProp As XElement = GetXElementByAttribute(props, _
            "name", "RecalcDocument")
        ' If there is already a RecalcDocument instruction in the 
        ' Custom File Properties part, then we don't need another one.
        ' Otherwise, we need to create a unique pid value.
        If Not IsNothing(recalcProp) Then
            Return pidValue
        Else
            ' Get all of the pid values of the proeprty elements and then
            ' convert the IEnumerable object into an array.
            Dim propIDs As IEnumerable(Of String) = _
            From prop In props
            Where prop.Name.LocalName = "property"
            Select prop.Attribute("pid").Value
            Dim propIDArray As String() = propIDs.ToArray()
            ' Increment this id value until a unique value is found.
            ' This starts at 2, because 0 and 1 are not valid pid values.
            Dim id As Integer = 2
            While (pidValue = -1)
                If (propIDArray.Contains(id.ToString())) Then
                    id = id + 1
                Else
                    pidValue = id
                End If
            End While
        End If
        Return pidValue
    End Function
    ```

3. <span data-ttu-id="3c348-315">前述の例から、**Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のコードを、次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3c348-315">Replace the code from the previous example in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Change the shape's horizontal position on the page 
    // by getting a reference to the Cell element for the PinY 
    // ShapeSheet cell and changing the value of its V attribute.
    XElement pinYCellXML = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY");
    pinYCellXML.SetAttributeValue("V", "2");
    // Add instructions to Visio to recalculate the entire document
    // when it is next opened.
    RecalcDocument(visioPackage);
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Change the shape's horizontal position on the page
    ' by getting a reference to the Cell element for the PinY
    ' ShapeSheet cell and changing the value of its V attribute.
    Dim pinYCellXML As XElement = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY")
    pinYCellXML.SetAttributeValue("V", "2")
    ' Add instructions to Visio to recalculate the entire document
    ' when it is next opened.
    RecalcDocument(visioPackage)
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

4. <span data-ttu-id="3c348-316">F5 キーを選択してソリューションをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="3c348-316">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="3c348-317">プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="3c348-317">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="3c348-318">Visio 2013 で Visio Package.vsdx ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="3c348-318">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="3c348-319">開始/終了図形は図面の下端から 2 インチの位置にあるはずです。</span><span class="sxs-lookup"><span data-stu-id="3c348-319">The Start/End shape should now be 2 inches from the bottom edge of the drawing.</span></span> <span data-ttu-id="3c348-320">開始/終了図形と処理図形の間のコネクタは、レイアウトの変更に合わせて再接続されているはずです。</span><span class="sxs-lookup"><span data-stu-id="3c348-320">The connector between the Start/End shape and the Process shape should have rerouted to accommodate the change in layout.</span></span> <span data-ttu-id="3c348-321">**RecalcDocument** プロパティがファイルに追加されていないと、図形の位置は変わりますが、コネクタは新しい図形の位置に再接続されません。</span><span class="sxs-lookup"><span data-stu-id="3c348-321">If the **RecalcDocument** property had not been added to the file, the shape position would have been changed, but the connector would not have rerouted to the new location of the shape.</span></span> 
  
## <a name="add-a-new-package-part-to-a-package"></a><span data-ttu-id="3c348-322">新しいパッケージ パーツをパッケージに追加する</span><span class="sxs-lookup"><span data-stu-id="3c348-322">Add a new package part to a package</span></span>
<span data-ttu-id="3c348-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span></span>

<span data-ttu-id="3c348-324">ファイル パッケージを変更するための最も一般的なシナリオの 1 つは、新しい文書パーツをパッケージに追加することです。</span><span class="sxs-lookup"><span data-stu-id="3c348-324">One of the most common scenarios for modifying a file package is adding a new document part to the package.</span></span> <span data-ttu-id="3c348-325">たとえば、コンテンツをパッケージに追加することにより Visio 図面にページを追加する場合は、ページ コンテンツ パーツをパッケージに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-325">For example, if you want to add a page to the Visio drawing by adding content to the package, you need to add a Page Contents part to the package.</span></span> 
  
<span data-ttu-id="3c348-326">次のように、パッケージに新しいパーツを追加するプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="3c348-326">The process for adding a new part to the package is straightforward:</span></span> 
  
1. <span data-ttu-id="3c348-327">**PackagePart** のためのデータを含む XML ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c348-327">You create the XML document with the data for the **PackagePart**.</span></span> <span data-ttu-id="3c348-328">作成した特定の種類の XML ドキュメントのスキーマを制御する XML 名前空間に特別な注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c348-328">You need to pay special attention to the XML namespaces that govern the schema for the specific type of XML document that you create.</span></span>
    
2. <span data-ttu-id="3c348-329">この XML を含む新しいファイルを作成し、そのファイルを **Package** 内の場所に保存します。</span><span class="sxs-lookup"><span data-stu-id="3c348-329">You create a new file to contain the XML and save the file to a location in the **Package**.</span></span>
    
3. <span data-ttu-id="3c348-330">新しい **PackagePart** と\*\* Package\*\*、または他の **PackagePart** オブジェクトの間に、必要なリレーションシップを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c348-330">You create the necessary relationships between the new **PackagePart** and the **Package** or other **PackagePart** objects.</span></span> 
    
4. <span data-ttu-id="3c348-p144">新しいパーツを参照する必要がある既存のパーツを更新します。たとえば、新しいページ コンテンツ パーツ (新しいページ) をファイルに追加する場合は、ページ インデックス パーツ (/visio/pages/pages.xml ファイル) を更新し、新しいページに関する正しい情報を組み込む必要もあります。</span><span class="sxs-lookup"><span data-stu-id="3c348-p144">You update any existing parts that need to reference the new part. For example, if you add a new Page Contents part (a new page) to the file, you also need to update the Page Index part (/visio/pages/pages.xml file) to include the correct information about the new page.</span></span>
    
<span data-ttu-id="3c348-333">Visio ファイル内に新しいリボン機能拡張パーツを作成するには、次の手順を使用してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-333">Use the following procedure to create a new Ribbon Extensibility part in the Visio file.</span></span> <span data-ttu-id="3c348-334">新しいリボン機能拡張パーツは、1 つのボタンが含まれる 1 つのグループを持つ新しいタブをリボンに追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-334">The new Ribbon Extensibility part adds to the ribbon a new tab with a single group that contains a single button.</span></span>
  
### <a name="to-create-a-new-package-part"></a><span data-ttu-id="3c348-335">新しいパッケージ パーツを作成するには</span><span class="sxs-lookup"><span data-stu-id="3c348-335">To create a new package part</span></span>

1. <span data-ttu-id="3c348-336">前の手順の **Program** クラス (Visual Basic では **Module1**) 内の `CheckForRecalc` メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-336">After the  `CheckForRecalc` method in the **Program** class (or **Module1** in Visual Basic) from the previous procedure, add the following method.</span></span> 
    
    ```cs
    private static XDocument CreateCustomUI()
    {
        // Add a new Custom User Interface document part to the package.
        // This code adds a new CUSTOM tab to the ribbon for this
        // document. The tab has one group that contains one button.
        XNamespace customUINS = 
            "https://schemas.microsoft.com/office/2006/01/customui";
        XDocument customUIXDoc = new XDocument(
            new XDeclaration("1.0", "utf-8", "true"),
            new XElement(customUINS + "customUI",
                new XElement(customUINS + "ribbon",
                    new XElement(customUINS + "tabs",
                        new XElement(customUINS + "tab",
                            new XAttribute("id", "customTab"),
                            new XAttribute("label", "CUSTOM"),
                            new XElement(customUINS + "group",
                                new XAttribute("id", "customGroup"),
                                new XAttribute("label", "Custom Group"),
                                new XElement(customUINS + "button",
                                    new XAttribute("id", "customButton"),
                                    new XAttribute("label", "Custom Button"),
                                    new XAttribute("size", "large"),
                                    new XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        );
        return customUIXDoc;
    }
    ```

    ```vb
    Private Function CreateCustomUI() As XDocument
        ' Add a new Custom User Interface document part to the package.
        ' This code adds a new CUSTOM tab to the ribbon for this
        ' document. The tab has one group that contains one button.
        Dim customUINS As XNamespace = _
            "https://schemas.microsoft.com/office/2006/01/customui"
        Dim customUIXML = New XDocument( _
            New XDeclaration("1.0", "utf-8", "true"), _
            New XElement(customUINS + "customUI", _
                New XElement(customUINS + "ribbon",
                    New XElement(customUINS + "tabs",
                        New XElement(customUINS + "tab",
                            New XAttribute("id", "customTab"),
                            New XAttribute("label", "CUSTOM"),
                            New XElement(customUINS + "group",
                                New XAttribute("id", "customGroup"),
                                New XAttribute("label", "Custom Group"),
                                New XElement(customUINS + "button",
                                    New XAttribute("id", "customButton"),
                                    New XAttribute("label", "Custom Button"),
                                    New XAttribute("size", "large"),
                                    New XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        )
        Return customUIXML
    End Function
    ```

2. <span data-ttu-id="3c348-337">前のステップの **Program** クラス (Visual Basic では **Module1**) 内の `CreateCustomUI` メソッドの後に、次のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c348-337">After the  `CreateCustomUI` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void CreateNewPackagePart(Package filePackage, 
        XDocument partXML, Uri packageLocation, string contentType, 
        string relationship)
    {
        // Need to check first to see whether the part exists already.
        if (!filePackage.PartExists(packageLocation))
        {
            // Create a new blank package part at the specified URI 
            // of the specified content type.
            PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
                contentType);
            // Create a stream from the package part and save the 
            // XML document to the package part.
            using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
                FileAccess.ReadWrite))
            {
                partXML.Save(partStream);
            }
        }
        // Add a relationship from the file package to this
        // package part. You can also create relationships
        // between an existing package part and a new part.
        filePackage.CreateRelationship(packageLocation,
            TargetMode.Internal,
            relationship);
    }
    ```

    ```vb
    Private Sub CreateNewPackagePart(filePackage As Package, _
        partXML As XDocument, packageLocation As Uri, contentType As String, _
        relationship As String)
        ' Need to check first to see whether the part exists already.
        If Not (filePackage.PartExists(packageLocation)) Then
            ' Create a new blank package part at the specified URI
            ' of the specified content type.
            Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
                contentType)
            ' Create a stream from the package part and save the
            ' XML document to the package part.
            Using partStream As Stream = newPart.GetStream(FileMode.Create, _
                FileAccess.ReadWrite)
                partXML.Save(partStream)
            End Using
            ' Add a relationship from the file package to this
            ' package part. You can also create relationships
            ' between an existing package part and a new part.
            filePackage.CreateRelationship(packageLocation, _
                TargetMode.Internal, relationship)
        End If
    End Sub
    ```

3. <span data-ttu-id="3c348-338">**Program** クラスの **Main** メソッド内の **using** ブロック (Visual Basic では **Module1** 内の **Main** メソッドの **Using** ブロック) 内のすべてのコードを、次のコードで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3c348-338">Replace all the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Create a new Ribbon Extensibility part and add it to the file.
    XDocument customUIXML = CreateCustomUI();
    CreateNewPackagePart(visioPackage, customUIXML, 
        new Uri("/customUI/customUI1.xml", UriKind.Relative),
        "application/xml",
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
    ```

    ```vb
    ' Create a new Ribbon Extensibility part and add it to the file.
    Dim customUIXML As XDocument = CreateCustomUI()
    CreateNewPackagePart(visioPackage, customUIXML, _
        New Uri("/customUI/customUI1.xml", UriKind.Relative), _
        "application/xml", _
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
    ```

4. <span data-ttu-id="3c348-339">F5 キーを選択してソリューションをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="3c348-339">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="3c348-340">プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="3c348-340">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="3c348-341">Visio 2013 で Visio Package.vsdx ファイルを開いてから、**[カスタム]** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c348-341">Open the Visio Package.vsdx file in Visio 2013, and then choose the **CUSTOM** tab.</span></span> 
    
<span data-ttu-id="3c348-342">Visio 2013 でファイルを開くと、カスタム リボンは図 2 のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c348-342">The custom ribbon looks like Figure 2 when the file is opened in Visio 2013.</span></span>
  
 <span data-ttu-id="3c348-343">**図 2. Visio 2013リボン内のカスタム タブ**</span><span class="sxs-lookup"><span data-stu-id="3c348-343">**Figure 2. Custom tab in the Visio 2013 ribbon**</span></span>
  
![リボンのカスタム タブ](media/vis15_CustomRibbonTab.PNG)
  
<span data-ttu-id="3c348-345">次のような `CreateCustomUI` メソッドによって XML が作成されます。</span><span class="sxs-lookup"><span data-stu-id="3c348-345">The XML created by the  `CreateCustomUI` method looks like the following.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="https://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a><span data-ttu-id="3c348-346">謝辞</span><span class="sxs-lookup"><span data-stu-id="3c348-346">Acknowledgements</span></span>
<span data-ttu-id="3c348-347"><a name="vis15_ManipulateFF_Ackn"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-347"><a name="vis15_ManipulateFF_Ackn"> </a></span></span>

<span data-ttu-id="3c348-348">この技術文書に含まれるコード例を作成した Visio MVP **Al Edlund** の貢献に感謝いたします。</span><span class="sxs-lookup"><span data-stu-id="3c348-348">We would like to recognize the contribution and input of Visio MVP **Al Edlund** in creating the code examples contained in this technical article.</span></span> <span data-ttu-id="3c348-349">Al は、Visio XML 図面形式 (.vdx) と新しい Visio ファイル形式 (.vsdx) の両方を含む、Visio ファイル形式の操作に関する定評のある専門家です。</span><span class="sxs-lookup"><span data-stu-id="3c348-349">Al is a recognized expert in manipulating the Visio file format, including both the Visio XML Drawing format (.vdx) and the new Visio file format (.vsdx).</span></span> <span data-ttu-id="3c348-350">Al は、プログラムによって Visio ファイル形式を調べるプロジェクトを作成しており、その内部構造を公開しています。</span><span class="sxs-lookup"><span data-stu-id="3c348-350">Al has created projects that explore the Visio file formats programmatically and exposes the structures inside.</span></span> 
  
<span data-ttu-id="3c348-351">Al による Visio ファイル形式の処理の詳細については、下記の「その他の技術情報」セクションにあるリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c348-351">For more information about Al's work with the Visio file format, see the links in the Additional Resources section that follows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3c348-352">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c348-352">See also</span></span>
<span data-ttu-id="3c348-353"><a name="vis15_ManipulateFF_Additional"> </a></span><span class="sxs-lookup"><span data-stu-id="3c348-353"><a name="vis15_ManipulateFF_Additional"> </a></span></span>

- <span data-ttu-id="3c348-354">Al Edlund 提供:</span><span class="sxs-lookup"><span data-stu-id="3c348-354">By Al Edlund:</span></span>
    
  - <span data-ttu-id="3c348-355">codeplex における[pkgVisio - Visio 2013 XML 操作](https://pkgvisio.codeplex.com/documentation)プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="3c348-355">[pkgVisio - Visio 2013 XML manipulation](https://pkgvisio.codeplex.com/documentation) project on CodePlex.</span></span> 
    
  - <span data-ttu-id="3c348-356">YouTube における動画[pkgVisio_pt1](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be)。</span><span class="sxs-lookup"><span data-stu-id="3c348-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) video on YouTube.</span></span> 
    
  - <span data-ttu-id="3c348-357">YouTube における動画[pkgVisio_pt2](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be)。</span><span class="sxs-lookup"><span data-stu-id="3c348-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) video on YouTube.</span></span> 
    
- [<span data-ttu-id="3c348-358">Visio デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="3c348-358">Visio Developer Center</span></span>](https://developer.microsoft.com/visio)
    
- <span data-ttu-id="3c348-359">[Office Open XML 形式のドキュメントの操作](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa982683(v=office.12))</span><span class="sxs-lookup"><span data-stu-id="3c348-359">[Manipulate Office Open XML Formats Documents](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa982683(v=office.12))</span></span>
    
- <span data-ttu-id="3c348-360">[名前空間を持つドキュメントを作成する (C#) (LINQ to XML)](https://docs.microsoft.com/previous-versions/bb387075(v=vs.140))</span><span class="sxs-lookup"><span data-stu-id="3c348-360">[Create a Document with Namespaces (C#) (LINQ to XML)](https://docs.microsoft.com/previous-versions/bb387075(v=vs.140))</span></span>
    
- <span data-ttu-id="3c348-361">[Microsoft Office を起動せず、ドキュメントにカスタム XML パーツを追加する](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/bb608597(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="3c348-361">[Add Custom XML Parts to Documents Without Starting Microsoft Office](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/bb608597(v=vs.90))</span></span>
    

