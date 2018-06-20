---
title: Visio ファイル形式をプログラムによって操作します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: ''
ms.openlocfilehash: 92ef2c084409dbe017951ff7dfdbf93839ff4b51
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805546"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a><span data-ttu-id="ae1e5-102">Visio ファイル形式をプログラムによって操作します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-102">Manipulate the Visio file format programmatically</span></span>

![方法トピック](media/mod_icon_howto.png)
  
<span data-ttu-id="ae1e5-104">Visio 2013 の新しいファイル形式のパッケージを読み取り、パッケージ内の部品を選択、一部のデータを変更および新しいパーツをパッケージに追加する、Visual Studio 2012 でソリューションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-104">Learn how to create a solution in Visual Studio 2012 to read the new file format package in Visio 2013, select parts in the package, change the data in a part, and add new parts to the package.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae1e5-105">**この資料に記載されて**         [Visio ファイル形式の操作の基礎](#vis15_ManipulateFF_Essentials)          [.Vsdx ファイルと新しい Visual Studio ソリューションを作成](#vis15_ManipulateFF_CreateFile)          [パッケージとして Visio 2013 ファイルを開く](#vis15_ManipulateFF_OpenPackage)          [選択しパッケージのパーツをパッケージからの読み取り](#vis15_ManipulateFF_SelectPart)          [選択しパッケージのパーツ内の XML データを変更します。](#vis15_ManipulateFF_ChangeXML)          [ファイル内のデータを再計算](#vis15_ManipulateFF_Recalculate)          [パッケージを新しいパッケージ パーツの追加](#vis15_ManipulateFF_AddNewPart)          [受信確認](#vis15_ManipulateFF_Ackn)          [その他のリソース](#vis15_ManipulateFF_Additional)</span><span class="sxs-lookup"><span data-stu-id="ae1e5-105">**In this article**         [Visio file format manipulation essentials](#vis15_ManipulateFF_Essentials)          [Create a .vsdx file and a new Visual Studio solution](#vis15_ManipulateFF_CreateFile)          [Open a Visio 2013 file as a package](#vis15_ManipulateFF_OpenPackage)          [Select and read package parts from a package](#vis15_ManipulateFF_SelectPart)          [Select and change XML data in a package part](#vis15_ManipulateFF_ChangeXML)          [Recalculate data in the file](#vis15_ManipulateFF_Recalculate)          [Add a new package part to a package](#vis15_ManipulateFF_AddNewPart)          [Acknowledgements](#vis15_ManipulateFF_Ackn)          [Additional resources](#vis15_ManipulateFF_Additional)</span></span>||
   
## <a name="visio-file-format-manipulation-essentials"></a><span data-ttu-id="ae1e5-106">Visio ファイル形式の操作の基本</span><span class="sxs-lookup"><span data-stu-id="ae1e5-106">Visio file format manipulation essentials</span></span>
<span data-ttu-id="ae1e5-107"><a name="vis15_ManipulateFF_Essentials"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-107"></span></span>

<span data-ttu-id="ae1e5-108">Visio の以前のバージョンでは、独自のバイナリ ファイル形式 (.vsd) またはシングル ドキュメント Visio XML 図面ファイル形式 (.vdx) ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-108">Previous versions of Visio saved files in a proprietary binary file format (.vsd) or a single-document Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="ae1e5-109">Visio 2013 には、XML と ZIP のアーカイブ ・ テクノロジーに基づいた新しいファイル形式 (.vsdx) が導入されています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-109">Visio 2013 introduces a new file format (.vsdx), which is based on XML and ZIP archive technologies.</span></span> <span data-ttu-id="ae1e5-110">Visio の以前のバージョンと同様に、ファイルは 1 つのコンテナーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-110">Just as in previous versions of Visio, files are saved in a single container.</span></span> <span data-ttu-id="ae1e5-111">従来のファイルとは異なりただし、新しいファイル形式を開く、読み取り、更新、変更すると、Visio 2013 のアプリケーションを自動化することがなく構築します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-111">Unlike legacy files, however, the new file format can be opened, read, updated, changed, and constructed without automating the Visio 2013 application.</span></span> <span data-ttu-id="ae1e5-112">XML を操作することや、 [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx)名前空間の操作に慣れている開発者がすぐに始める新しいファイル形式をプログラムによって操作します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-112">Developers who are familiar with manipulating XML or working with the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace can quickly get started working with the new file format programmatically.</span></span> <span data-ttu-id="ae1e5-113">以前のバージョンの Visio XML 図面形式を使用してきた開発者は、その形式の構造体の多く維持されていますが、新しいファイル形式を検索できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-113">Developers who have worked with the Visio XML Drawing format from previous versions can find that many of the structures from that format have been retained in the new file format.</span></span> 
  
<span data-ttu-id="ae1e5-114">この記事で考察プログラムで、Visio 2013 のファイル形式を使用する方法、Microsoft.NET Framework 4.5、C# または Visual Basic、および Visual Studio 2012 を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-114">In this article, we examine how to work with the Visio 2013 file format programmatically, using the Microsoft .NET Framework 4.5, C# or Visual Basic, and Visual Studio 2012.</span></span> <span data-ttu-id="ae1e5-115">Visio 2013 ファイルを開く、ファイル内の文書パーツを選択して、パーツのデータを変更および新しい文書パーツを作成する方法を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-115">You can see how to open a Visio 2013 file, select document parts within the file, change data in parts, and create a new document part.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae1e5-116">この資料のコード サンプルでは、 [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) 、 [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx)名前空間のクラスの基本的な知識があることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-116">The code samples in this article assume that you have a rudimentary understanding of the classes in the [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) and [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespaces.</span></span> <span data-ttu-id="ae1e5-117">> この資料では、概念とオープンのパッケージ化規則の用語を理解することも想定しています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-117">> This article also assumes that you understand the concepts and terminology of the Open Packaging Conventions.</span></span> <span data-ttu-id="ae1e5-118">パッケージ、文書パーツまたはパッケージのパーツおよびリレーションシップの概念をいくつかの知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-118">You should have some familiarity with the concepts of packages, document parts or package parts, and relationships.</span></span> <span data-ttu-id="ae1e5-119">詳細についてを参照してください[OPC: A 新しい標準的なパッケージのデータを](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-119">For more information, see [OPC: A New Standard for Packaging Your Data](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).</span></span> <span data-ttu-id="ae1e5-120">> のコードでは、XML を選択するクエリを LINQ (統合言語クエリ) を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-120">> The code demonstrates how to create LINQ (Language-Integrated Query) queries to select XML.</span></span> <span data-ttu-id="ae1e5-121">多くのコード サンプルは、LINQ クエリの作成のクエリの構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-121">Most of the code samples use the query syntax for building LINQ queries.</span></span> <span data-ttu-id="ae1e5-122">必要な場合は、LINQ のメソッドの構文を使用して、コードで提供される LINQ クエリのいずれかを書き直すことができます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-122">You can rewrite any of the LINQ queries provided in the code by using the LINQ method syntax, if necessary.</span></span> <span data-ttu-id="ae1e5-123">LINQ クエリ構文とメソッド構文の詳細については、 [LINQ のクエリ構文](http://msdn.microsoft.com/en-us/library/bb397947.aspx)を参照してください > 表 1 は、この資料を使用する前にに精通している必要があります重要なトピックを示します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-123">For more information about LINQ query syntax and method syntax, see [LINQ Query Syntax versus Method Syntax (C#)](http://msdn.microsoft.com/en-us/library/bb397947.aspx)> Table 1 shows the essential topics that you should be familiar with before you work through this article.</span></span> 
  
<span data-ttu-id="ae1e5-124">**表 1 です。Visio 2013 のファイル形式を操作するための中核となる概念**</span><span class="sxs-lookup"><span data-stu-id="ae1e5-124">**Table 1. Core concepts for manipulating the Visio 2013 file format**</span></span>

|<span data-ttu-id="ae1e5-125">**記事のタイトル**</span><span class="sxs-lookup"><span data-stu-id="ae1e5-125">**Article title**</span></span>|<span data-ttu-id="ae1e5-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae1e5-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae1e5-127">Visio ファイル形式 (.vsdx) の概要</span><span class="sxs-lookup"><span data-stu-id="ae1e5-127">Introduction to the Visio file format (.vsdx)</span></span>](introduction-to-the-visio-file-formatvsdx.md) <br/> |<span data-ttu-id="ae1e5-128">この概要では、Visio 2013 のファイル形式の主な機能のいくつかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-128">This high-level overview describes some of the major features of the Visio 2013 file format.</span></span> <span data-ttu-id="ae1e5-129">Visio 2013 のファイル形式に適用されていると、開いているパッケージ化の規則 (OPC) を説明します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-129">It discusses the Open Packaging Conventions (OPC) as they have been applied to the Visio 2013 file format.</span></span> <span data-ttu-id="ae1e5-130">また、いくつかの違いは、Visio 2013 のファイル形式と以前の Visio XML 図面ファイル形式 (.vdx) を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-130">It also lists some differences between the Visio 2013 file format and the previous Visio XML Drawing file format (.vdx).</span></span>  <br/> |
|[<span data-ttu-id="ae1e5-131">OPC: データをパッケージ化するための新しい標準</span><span class="sxs-lookup"><span data-stu-id="ae1e5-131">OPC: A New Standard for Packaging Your Data</span></span>](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx) <br/> |<span data-ttu-id="ae1e5-132">この MSDN マガジンの記事は、Open Packaging Conventions の概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-132">This MSDN Magazine article describes the Open Packaging Conventions as a concept.</span></span>  <br/> |
|[<span data-ttu-id="ae1e5-133">オープンなパッケージング規則の基礎</span><span class="sxs-lookup"><span data-stu-id="ae1e5-133">Essentials of the Open Packaging Conventions</span></span>](http://msdn.microsoft.com/en-us/library/ee361919.aspx) <br/> [<span data-ttu-id="ae1e5-134">Office (2007) オープン XML ファイル形式の概要</span><span class="sxs-lookup"><span data-stu-id="ae1e5-134">Introducing the Office (2007) Open XML File Formats</span></span>](http://msdn.microsoft.com/en-us/library/aa338205.aspx) <br/> |<span data-ttu-id="ae1e5-135">これら 2 つの資料では、Microsoft Office ファイルを開くのパッケージ化の規則を適用されている方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-135">These two articles discuss how the Open Packaging Conventions have been applied to Microsoft Office files.</span></span> <span data-ttu-id="ae1e5-136">関係のパッケージでの作業し、いくつかのコード サンプルも含まれての説明が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-136">They contain descriptions of how relationships work in a package and also include some code examples.</span></span>  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a><span data-ttu-id="ae1e5-137">.vsdx ファイルと新しい Visual Studio ソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="ae1e5-137">Create a .vsdx file and a new Visual Studio solution</span></span>
<span data-ttu-id="ae1e5-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-138"></span></span>

<span data-ttu-id="ae1e5-139">この資料の手順での作業を開始する前に、Visio 2013 ファイルを開き、操作を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-139">Before you can begin working through the procedures in this article, you need to create a Visio 2013 file to open and manipulate.</span></span> <span data-ttu-id="ae1e5-140">この資料のコード例で使用されている図面には、接続されている 2 つの図形で、[基本フローチャート] テンプレートから [開始/終了"の形をしている図形の 1 つで 1 つのページが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-140">The drawing used in the code examples in this article contains a single page with two connected shapes on it, one of the shapes being a "Start/End" shape from the "Basic Flowchart" template.</span></span>
  
<span data-ttu-id="ae1e5-141">この資料の残りの手順で使用するのに新しい Visio 2013 ファイルを作成するのにには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-141">Use the following procedure to create a new Visio 2013 file to use in the remaining procedures in this article.</span></span>
  
### <a name="to-create-new-file-in-visio-2013"></a><span data-ttu-id="ae1e5-142">Visio 2013 で、新しいファイルを作成するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-142">To create new file in Visio 2013</span></span>

1. <span data-ttu-id="ae1e5-143">Visio 2013 を開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-143">Open Visio 2013.</span></span>
    
2. <span data-ttu-id="ae1e5-144">**作成**、**カテゴリ**、**フローチャート**、 **[基本フローチャート]** を選択して [基本フローチャート] テンプレートに基づいた新しい文書を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-144">Create a new document based on the Basic Flowchart template by choosing **CATEGORIES**, **Flowchart**, **Basic Flowchart**, **Create**.</span></span>
    
3. <span data-ttu-id="ae1e5-145">**[図形**] ウィンドウからの**開始/終了**図形をキャンバスにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-145">From the **Shapes** window, drag a **Start/End** shape onto the canvas.</span></span> 
    
4. <span data-ttu-id="ae1e5-146">描画キャンバス上の新しい開始/終了図形を選択し、' プロセスの開始] を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-146">Select the new Start/End shape on the drawing canvas and type 'Begin Process'.</span></span>
    
5. <span data-ttu-id="ae1e5-147">**[図形**] ウィンドウから **[処理**] 図形をキャンバスにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-147">From the **Shapes** window, drag a **Process** shape onto the canvas.</span></span> 
    
6. <span data-ttu-id="ae1e5-148">描画キャンバス上に、新規の [処理] 図形を選択し、いくつかのタスクを実行する' を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-148">Select the new Process shape on the drawing canvas and type 'Perform some task'.</span></span>
    
7. <span data-ttu-id="ae1e5-149">開始/終了図形のショートカット メニューは、**ページの 1 つのコネクタを追加**を選択し、図 1 に示すように、カンバス上で、開始/終了プロセスの図形とコネクタを描画します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-149">On the shortcut menu for the Start/End shape, select **Add One Connector to the Page**, and then draw a connector between the Start/End and Process shapes on the canvas, as shown in Figure 1.</span></span>
    
    <span data-ttu-id="ae1e5-150">**図 1 です。Visio 2013 の簡単な描画**</span><span class="sxs-lookup"><span data-stu-id="ae1e5-150">**Figure 1. Simple Visio 2013 drawing**</span></span>
    
     ![処理図形に接続されている開始/終了図形](media/vis15_SimpleFlowchart.png)
  
8. <span data-ttu-id="ae1e5-152">**ファイル**、**名前を付けて**、**コンピューター**、**デスクトップ**を選択して、ファイルをデスクトップに .vsdx ファイルとして保存します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-152">Save the file to your Desktop as a .vsdx file by choosing **File**, **Save As**, **Computer**, **Desktop**.</span></span>
    
    <span data-ttu-id="ae1e5-153">**名前を付けて保存**] ダイアログ ボックスで、Visio のパッケージ**ファイル名**] ボックスで入力""を選択**Visio 図面 (\*.vsdx)** **ファイルの種類**の一覧、および [**保存**] ボタンを選択し。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-153">In the **Save As** dialog box, enter Visio Package in the **File name** box"", select **Visio Drawing (\*.vsdx)** in the **Save as type** list, and then choose the **Save** button.</span></span> 
    
9. <span data-ttu-id="ae1e5-154">ファイルを閉じ、Visio 2013 を閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-154">Close the file and then close Visio 2013.</span></span>
    
> [!TIP]
> <span data-ttu-id="ae1e5-155">Visio を開いてファイルが正常に、ファイルに問題がある場合にも。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-155">Sometimes Visio opens a file successfully even if there are issues with the file.</span></span> <span data-ttu-id="ae1e5-156">Visio が通知するすべてのファイルの問題のためには、ファイルのパッケージのレベルでの Visio ファイルを操作するためのソリューションをテストする場合で、ファイル開くときの警告を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-156">To ensure that Visio notifies you of any file issues, you should enable file open warnings when testing solutions that manipulate Visio files at the file package level.</span></span> <span data-ttu-id="ae1e5-157">> Visio 2013 年で、ファイルを開いている警告を有効にするにはは、**ファイル**、**オプション**の**詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-157">> To enable file open warnings, in Visio 2013, choose **File**, **Options**, **Advanced**.</span></span> <span data-ttu-id="ae1e5-158">[**保存/開く**]、[**ファイルを開いている警告を表示する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-158">Under **Save/Open**, select **Show file open warnings**.</span></span> 
  
<span data-ttu-id="ae1e5-159">これらの手順は、「Visio Package.vsdx」ファイルを操作する Windows コンソール アプリケーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-159">These procedures use a Windows console application to manipulate the "Visio Package.vsdx" file.</span></span> <span data-ttu-id="ae1e5-160">Visual Studio 2012 で、新しい Windows コンソール アプリケーションを作成および設定するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-160">Use the following procedure to create and set up a new Windows console application in Visual Studio 2012.</span></span>
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a><span data-ttu-id="ae1e5-161">Visual Studio 2012 の新しいソリューションを作成するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-161">To create a new solution in Visual Studio 2012</span></span>

1. <span data-ttu-id="ae1e5-162">[**ファイル**] メニューの [**新規**作成]**プロジェクト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-162">On the **File** menu, choose **New**, **Project**.</span></span>
    
2. <span data-ttu-id="ae1e5-163">**新しいプロジェクト**] ダイアログ ボックスでは、 **Visual C#** または**Visual Basic**では、いずれかを展開し、 **Windows****コンソール アプリケーション**を選択し、します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-163">In the **New Project** dialog box, expand either **Visual C#** or **Visual Basic**, and then choose **Windows**, **Console Application**.</span></span>
    
    <span data-ttu-id="ae1e5-164">[**名**] ボックスで、'VisioFileAccessor' を入力して、プロジェクトの場所を選択、 **[OK** ] を選択し。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-164">In the **Name** box, enter ' VisioFileAccessor', select a location for the project, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="ae1e5-165">[ **プロジェクト**] メニューの [ **参照の追加**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-165">On the **Project** menu, choose **Add Reference**.</span></span> 
    
    <span data-ttu-id="ae1e5-166">**参照マネージャー**ダイアログ ボックスの [**アセンブリ**のでは、**フレームワーク**を選択し、 **System.Xml** 、 **WindowsBase**コンポーネントへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-166">In the **Reference Manager** dialog box, under **Assemblies**, choose **Framework**, and then add a reference to the **System.Xml** and **WindowsBase** components.</span></span> 
    
4. <span data-ttu-id="ae1e5-167">Program.cs または Module1.vb ファイル、プロジェクトに、次の**using**ディレクティブ (Visual Basic では**Imports**ステートメント) を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-167">In the Program.cs or Module1.vb file for the project, add the following **using** directives (**Imports** statements in Visual Basic):</span></span> 
    
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

5. <span data-ttu-id="ae1e5-168">Program.cs または Module1.vb ファイル (Visual Basic では**Module1** )**プログラム**のクラスの**Main**メソッドの末尾までのコンソール アプリケーションの実行を停止する次のコードを追加する前に、キーを押した。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-168">Also in the Program.cs or Module1.vb file, before the end of the **Main** method of the **Program** class (**Module1** in Visual Basic), add the following code that stops execution of the console application until the user presses a key.</span></span> 
    
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

## <a name="open-a-visio-2013-file-as-a-package"></a><span data-ttu-id="ae1e5-169">パッケージとして Visio 2013 ファイルを開く</span><span class="sxs-lookup"><span data-stu-id="ae1e5-169">Open a Visio 2013 file as a package</span></span>
<span data-ttu-id="ae1e5-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-170"></span></span>

<span data-ttu-id="ae1e5-171">ファイル内のデータのいずれかを操作することができます、前に、最初に、 [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx)名前空間内に含まれる[パッケージ](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx)オブジェクト内でファイルを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-171">Before you can manipulate any of the data within the file, you need to first open the file within a [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) object, which is contained within the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace.</span></span> <span data-ttu-id="ae1e5-172">**パッケージ**オブジェクトは、全体として Visio ファイルを表します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-172">The **Package** object represents the Visio file as a whole.</span></span> <span data-ttu-id="ae1e5-173">ファイルのパッケージ内の個々 の文書パーツを選択することを許可するメンバーを公開します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-173">It exposes members that allow you to select individual document parts within the file package.</span></span> <span data-ttu-id="ae1e5-174">具体的には、**パッケージ**のクラスは、パッケージとしてファイルを開くに使用する静的な[(文字列、FileMode、FileAccess) の Open](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx)メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-174">In particular, the **Package** class exposes the static [Open(String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) method that you use to open a file as a package.</span></span> <span data-ttu-id="ae1e5-175">また、一度パッケージを閉じるための[Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx)メソッドを公開処理を終了します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-175">It also exposes a [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) method for closing the package once you've finished with it.</span></span> 
  
> [!TIP]
> <span data-ttu-id="ae1e5-176">最善の方法としては、**パッケージ**オブジェクトの Visio ファイルを開き、それが終わったときに、ファイルのパッケージを明示的に閉じる必要はありません**を使用して**ブロックを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-176">As a best practice, use a **using** block to open the Visio file in the **Package** object so that you don't have to explicitly close the file package when you're done with it.</span></span> <span data-ttu-id="ae1e5-177">**Finally**ブロック内の**catch または finally**構築の**Package.Close**メソッドを明示的に呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-177">You can also explicitly call the **Package.Close** method in the **finally** block of a **try/catch/finally** construction.</span></span> 
  
<span data-ttu-id="ae1e5-178">**Package.Open**メソッドに引数としてパスを渡す、呼び出し元のコードに、**パッケージ**オブジェクトを返す、 [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx)オブジェクトを使用して、「Visio Package.vsdx」ファイルの完全パスを取得するには、次コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-178">Use the following code to get the full path for the "Visio Package.vsdx" file by using a [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) object, pass the path as an argument to the **Package.Open** method, and then return a **Package** object to the calling code.</span></span> 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a><span data-ttu-id="ae1e5-179">.vsdx ファイルをパッケージとして開くには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-179">To open a .vsdx file as a package</span></span>

1. <span data-ttu-id="ae1e5-180">**メイン**の後は、**プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-180">After the **Main** method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

2. <span data-ttu-id="ae1e5-181">**プログラム**クラス (または Visual Basic では**Module1** ) の**Main**メソッドに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-181">In the **Main** method of the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

## <a name="select-and-read-package-parts-from-a-package"></a><span data-ttu-id="ae1e5-182">パッケージからパッケージ パーツを選択して読み取る</span><span class="sxs-lookup"><span data-stu-id="ae1e5-182">Select and read package parts from a package</span></span>
<span data-ttu-id="ae1e5-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-183"></span></span>

<span data-ttu-id="ae1e5-184">パッケージを開き、Visio 2013 ファイルを作成したら、 **System.IO.Packaging**名前空間に含まれている[PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx)クラスを使用してその中の文書パーツにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-184">Once you have the Visio 2013 file open as a package, you can access the document parts within it using the [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) class included in the **System.IO.Packaging** namespace.</span></span> <span data-ttu-id="ae1e5-185">**PackagePart**オブジェクトは、個別にまたはコレクションとしてインスタンス化することができます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-185">**PackagePart** objects can be instantiated individually or as a collection.</span></span> <span data-ttu-id="ae1e5-186">**パッケージ**のクラスでは、 [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx)メソッドと**パッケージ**からの**PackagePart**オブジェクトを取得するための[GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx)メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-186">The **Package** class exposes a [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) method and a [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) method for getting **PackagePart** objects out of the **Package**.</span></span> <span data-ttu-id="ae1e5-187">**Package.GetParts**メソッドを実装するその他のコレクションと同様に操作できますし、 [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx)クラスのインスタンスを取得する、 [IEnumerator\<T\>](https://msdn.microsoft.com/library/System.Collections.Generic.IEnumerator`1.aspx)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-187">The **Package.GetParts** method returns an instance of the [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) class, which you can then interact with like any other collection that implements the [IEnumerator\<T\>](https://msdn.microsoft.com/library/System.Collections.Generic.IEnumerator`1.aspx) interface.</span></span> 
  
<span data-ttu-id="ae1e5-188">コレクションと**パッケージ**から、 **PackagePartCollection**オブジェクトを取得、 **PackagePart**オブジェクトのコレクションを反復処理して、URI と各**PackagePart のコンテンツ タイプを作成、次の手順でコードを使用してください。** コンソールにします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-188">Use the code in the following procedure to get a **PackagePartCollection** object from the **Package** as a collection, iterate through the **PackagePart** objects in the collection, and write the URI and content type of each **PackagePart** to the console.</span></span> 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a><span data-ttu-id="ae1e5-189">パッケージ内のパッケージ パーツを反復処理するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-189">To iterate through the package parts in a package</span></span>

1. <span data-ttu-id="ae1e5-190">後、 `OpenPackage` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-190">After the  `OpenPackage` method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

2. <span data-ttu-id="ae1e5-191">(Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック)**プログラム**のクラスの**Main**メソッド**を使用して**ブロック内の次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-191">Add the following code inside the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic):</span></span> 
    
  ```cs
  // Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage);
  
  ```

  ```vb
  ' Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage)
  
  ```

3. <span data-ttu-id="ae1e5-p112">F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-p112">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
<span data-ttu-id="ae1e5-194">コンソール アプリケーションは、次のような出力を生成します (簡潔にするため、出力の一部が省略されています)。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-194">The console application produces output similar to the following (some of the output has been omitted for brevity):</span></span>
  
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
  
<span data-ttu-id="ae1e5-195">ほとんどの場合、それらのすべてを反復処理することがなく 1 つの**PackagePart**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-195">More often than not, you need to select one **PackagePart** without having to iterate over all of them.</span></span> <span data-ttu-id="ae1e5-196">**パッケージ**からの**PackagePart**オブジェクトを取得するには、**パッケージ**または別の**PackagePart**の関係を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-196">You can get a **PackagePart** object from a **Package** by using its relationship to the **Package** or another **PackagePart**.</span></span> <span data-ttu-id="ae1e5-197">Visio 2013 がファイル形式は、ドキュメント パーツの関係について説明する別個のエンティティのリレーションシップ ファイル パッケージまたは 2 つの文書パーツは、相互に関連します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-197">A relationship in the Visio 2013 file format is a discrete entity that describes how a document part relates to the file package or how two document parts relate to each other.</span></span> <span data-ttu-id="ae1e5-198">などの Visio 2013 ファイル パッケージ自体と、Visio 図面の一部に関係があるし、Visio 図面の一部が Windows の一部に関係を持っています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-198">For example, the Visio 2013 file package itself has a relationship to its Visio Document part, and the Visio Document part has a relationship to the Windows part.</span></span> <span data-ttu-id="ae1e5-199">[PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx)または[PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx)のクラスのインスタンスとしては、これらの関係が表されます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-199">These relationships are represented as instances of the [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) or [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) classes.</span></span> 
  
<span data-ttu-id="ae1e5-200">**パッケージ**のクラスは、 **PackageRelationship**または**PackageRelationshipCollection**オブジェクトとして含まれている関係を取得するためのいくつかのメソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-200">The **Package** class exposes several methods for getting the relationships that it contains as **PackageRelationship** or **PackageRelationshipCollection** objects.</span></span> <span data-ttu-id="ae1e5-201">[GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx)メソッドを使用するには 1 つの特定の種類の**PackageRelationship**オブジェクトを格納する**PackageRelationshipCollection**オブジェクトをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-201">You can use the [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) method to instantiate a **PackageRelationshipCollection** object that contains **PackageRelationship** objects of a single specific type.</span></span> <span data-ttu-id="ae1e5-202">もちろん、 **Package.GetRelationshipsByType**メソッドを使用する場合は、必要なリレーションシップの種類が既にわかっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-202">Of course, using the **Package.GetRelationshipsByType** method requires that you already know the relationship type that you need.</span></span> <span data-ttu-id="ae1e5-203">関係タイプは、XML 名前空間の形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-203">Relationship types are strings in XML namespace format.</span></span> <span data-ttu-id="ae1e5-204">Visio 文書パーツの関連付けの種類は、たとえば、 http://schemas.microsoft.com/visio/2010/relationships/document。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-204">For example, the relationship type of the Visio Document part is http://schemas.microsoft.com/visio/2010/relationships/document.</span></span> 
  
<span data-ttu-id="ae1e5-205">**パッケージ**または別の**PackagePart**の**PackagePart**の関係さえわかっていれば (つまり、オブジェクトがある、 **PackageRelationship** **PackagePart**するを参照)、使用することができますその**PackagePart**の URI を取得する関係です。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-205">Once you know the relationship of a **PackagePart** to the **Package** or to another **PackagePart** (that is, you have a **PackageRelationship** object that references the **PackagePart** that you want), you can use that relationship to get the URI of that **PackagePart**.</span></span> <span data-ttu-id="ae1e5-206">**PackagePart**を返すために**Package.GetPart**メソッドに URI を渡すし。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-206">You then pass the URI to the **Package.GetPart** method to return the **PackagePart**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae1e5-207">すれば、特定の**PackagePart**への参照だけで、 **Package.GetPart**メソッドとの**PackagePart**では、URI を使用してパッケージを取得する、部品の関連手順をバイパスします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-207">You can also get a reference to a specific **PackagePart** by using just the **Package.GetPart** method and the URI of the **PackagePart**, bypassing the step where you get the package part's relationships.</span></span> <span data-ttu-id="ae1e5-208">ただし、Visio ファイルのパッケージのパッケージの一部は、パッケージ内の既定の場所以外の場所に保存できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-208">However, some package parts in the Visio file package can be saved to locations other than their default locations in a package.</span></span> <span data-ttu-id="ae1e5-209">パッケージの一部が常にすべてのファイルに対して同じ URI であるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-209">You cannot assume that a package part is always located at the same URI for every file.</span></span> <span data-ttu-id="ae1e5-210">> 代わりに、リレーションシップを使用して個々 の**PackagePart**オブジェクトにアクセスするベスト ・ プラクティスを勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-210">> Instead, it is a best practice to use relationships to access individual **PackagePart** objects.</span></span> 
  
<span data-ttu-id="ae1e5-211">**PackagePart** (Visio 図面の一部) を取得するのに部分を参照する**パッケージ**の**PackageRelationship**を使用して、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-211">Use the following procedure to get a **PackagePart** (the Visio Document part) by using the **PackageRelationship** from the **Package** that references the part.</span></span> 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a><span data-ttu-id="ae1e5-212">リレーションシップによりパッケージ内の特定のパッケージ パーツを選択するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-212">To select a specific package part in the package by relationship</span></span>

1. <span data-ttu-id="ae1e5-213">後、 `IteratePackageParts` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-213">After the  `IteratePackageParts` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="ae1e5-214">**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) の**Main**メソッド**を使用して**ブロック内のコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-214">Replace the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
  ```cs
  // Get a reference to the Visio Document part contained in the file package.
  PackagePart documentPart = GetPackagePart(visioPackage, 
      "http://schemas.microsoft.com/visio/2010/relationships/document");
  
  ```

  ```vb
  ' Get a reference to the Visio Document part contained in the file package.
  Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
      "http://schemas.microsoft.com/visio/2010/relationships/document")
  
  ```

<span data-ttu-id="ae1e5-215">前述のように、他の**PackagePart**オブジェクトとの関係を使用して**PackagePart**オブジェクトを取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-215">As mentioned previously, you can also get **PackagePart** objects by using their relationship to other **PackagePart** objects.</span></span> <span data-ttu-id="ae1e5-216">**PackagePart**オブジェクトのほとんどの複雑な Visio 図面では、**パッケージ**との関係を持っていないために、このことが重要です。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-216">This is important because, for a Visio document of any complexity, most of the **PackagePart** objects don't have a relationship to the **Package**.</span></span> <span data-ttu-id="ae1e5-217">たとえば、ファイル パッケージ (つまり、/visio/pages/page1.xml) 内の個々 のページのコンテンツ部品では、ファイルのパッケージ自体ではなく、ページのインデックスの一部 (つまり、/visio/pages/pages.xml) に関係があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-217">For example, an individual Page Content part in the file package (that is, /visio/pages/page1.xml) has a relationship to the Page Index part (that is, /visio/pages/pages.xml) but not to the file package itself.</span></span> <span data-ttu-id="ae1e5-218">個々 のページの正確な URI のパッケージをお持ちでない場合は、オブジェクトへの参照を取得するページのインデックスの一部の関係を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-218">If you don't have the exact URI of the individual page in the package, you can use its relationship to the Page Index part to get a reference to it.</span></span>
  
<span data-ttu-id="ae1e5-219">**PackagePart**クラスは、 **PackageRelationship**オブジェクトの 1 つだけの種類を含む**PackageRelationshipCollection**オブジェクトを返すために使用できる[GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx)メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-219">The **PackagePart** class exposes a [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) method that you can use to return a **PackageRelationshipCollection** object that contains only one type of **PackageRelationship** object.</span></span> <span data-ttu-id="ae1e5-220">**PackageRelationshipCollection**を作成したら、 **PackageRelationship**コレクションから必要があるし、 **PackagePart**オブジェクトを参照することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-220">Once you have the **PackageRelationshipCollection**, you can select the **PackageRelationship** that you need from the collection and then reference the **PackagePart** object.</span></span> 
  
<span data-ttu-id="ae1e5-221">(からの**PackageRelationship**オブジェクトを取得) の関係を使用して、**パッケージ**からの**PackagePart**を取得する次のコードを使用して別の**PackagePart**。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-221">Use the following code to get a **PackagePart** from the **Package** by using its relationship to (getting a **PackageRelationship** object from) another **PackagePart**.</span></span>
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a><span data-ttu-id="ae1e5-222">別のパッケージ パーツとのリレーションシップを利用して特定のパッケージ パーツを選択するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-222">To select a specific package part through its relationship to another package part</span></span>

1. <span data-ttu-id="ae1e5-223">後、 `GetPackagePart` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、次のオーバー ロード メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-223">After the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following overload method.</span></span> 
    
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

2. <span data-ttu-id="ae1e5-224">前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-224">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> <span data-ttu-id="ae1e5-225">(前の手順で追加したコードを削除しない)。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-225">(Do not delete the code that you added in the previous procedure.)</span></span> 
    
  ```cs
  // Get a reference to the collection of pages in the document, 
  // and then to the first page in the document.
  PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/pages");
  PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/page");
  
  ```

  ```vb
  ' Get a reference to the collection of pages in the document,
  ' and then to the first page in the document.
  Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/pages") 
  Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/page") 
  ```

<span data-ttu-id="ae1e5-226">ドキュメントの一部に含まれている XML に変更を行うことができます、前に、まず[XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx)クラスまたは[XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx)クラスを使用して、XML を読み取ることができるオブジェクトを XML ドキュメントをロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-226">Before you can make changes to the XML included in a document part, you need to first load the XML document into an object that allows you to read the XML, using the [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) class or [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) class.</span></span> <span data-ttu-id="ae1e5-227">両方のクラスは、XML ドキュメント内に含まれる XML 要素を選択するなどのタスクのメソッドを公開します。属性を書き込み、作成、読み取り、新しい XML 要素を文書に挿入します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-227">Both classes expose methods for tasks such as selecting XML elements contained within the XML documents; creating, reading, and writing attributes; and inserting new XML elements into a document.</span></span> 
  
<span data-ttu-id="ae1e5-228">、2 つの**XDocument**クラスでは、LINQ を使用して XML のクエリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-228">Of the two, the **XDocument** class allows you to query the XML using LINQ.</span></span> <span data-ttu-id="ae1e5-229">LINQ では、簡単に選択する個々 の要素の XML ドキュメントからクエリの作成ではなく、コレクション内の要素のすべてを反復処理してテストに必要な要素の。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-229">With LINQ, you can easily select individual elements from an XML document by creating queries, rather than iterating over all of the elements in a collection and testing for the elements that you need.</span></span> <span data-ttu-id="ae1e5-230">これらの理由から、この資料では、次の手順は、XML を操作するため、 **XDocument**クラスおよび**System.Xml.Linq**名前空間の他のクラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-230">For these reasons, the following procedures in this article use the **XDocument** class and other classes of the **System.Xml.Linq** namespace for working with XML.</span></span> 
  
<span data-ttu-id="ae1e5-231">次の手順を使用して、 **XDocument**オブジェクト内の XML ドキュメントとして、 **PackagePart**を開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-231">Use the following procedure to open a **PackagePart** as an XML document in an **XDocument** object.</span></span> 
  
### <a name="to-read-the-xml-in-a-package-part"></a><span data-ttu-id="ae1e5-232">パッケージ パーツ内の XML を読み取るには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-232">To read the XML in a package part</span></span>

1. <span data-ttu-id="ae1e5-233">最後のオーバー ロードした後、 `GetPackagePart` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-233">After the last overload for the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="ae1e5-234">前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-234">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
  ```cs
  // Open the XML from the Page Contents part.
  XDocument pageXML = GetXMLFromPart(pagePart);
  ```

  ```vb
  ' Open the XML from the Page Contents part.
  Dim pageXML As XDocument = GetXMLFromPart(pagePart)
  ```

## <a name="select-and-change-xml-data-in-a-package-part"></a><span data-ttu-id="ae1e5-235">パッケージ パーツ内の XML データを選択して変更する</span><span class="sxs-lookup"><span data-stu-id="ae1e5-235">Select and change XML data in a package part</span></span>
<span data-ttu-id="ae1e5-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-236"></span></span>

<span data-ttu-id="ae1e5-237">**XDocument**オブジェクトへのドキュメントの一部をロードする XML 要素を選択し、XML ドキュメントに変更を加えるに LINQ を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-237">Once you have loaded a document part into an **XDocument** object, you can use LINQ to select XML elements and make changes to the XML document.</span></span> <span data-ttu-id="ae1e5-238">XML データを変更、追加またはデータを削除して文書の一部に XML ドキュメントを保存できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-238">You can change XML data, add or remove data, and then save the XML document back to the document part.</span></span> 
  
<span data-ttu-id="ae1e5-239">Visio ファイル形式を操作するための最も一般的なタスクを選択する特定の XML 要素または要素のコレクションのドキュメント。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-239">The most common task for manipulating the Visio file format is selecting specific XML elements or collections of elements in the document.</span></span> <span data-ttu-id="ae1e5-240">**System.Xml.Linq**名前空間には、XML 要素を表す、 [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx)クラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-240">The **System.Xml.Linq** namespace includes the [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) class, which represents an XML element.</span></span> <span data-ttu-id="ae1e5-241">**XElement**クラスでは、(例) として **"入力規則"** の要素を個々 の**図形**要素より細かいレベルでの Visio ファイルに含まれるデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-241">The **XElement** class gives you access to the data contained in the Visio file at a granular level, from individual **Shape** elements to **ValidationRule** elements (as examples).</span></span> 
  
<span data-ttu-id="ae1e5-242">**XDocument** (ページの内容の一部を含む) からの**図形**要素を選択して、特定の**図形**要素を選択するのには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-242">Use the following code to select the **Shape** elements from an **XDocument** (containing a Page Contents part) and to then select a specific **Shape** element.</span></span> 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a><span data-ttu-id="ae1e5-243">パッケージ パーツ内の特定の要素を選択するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-243">To select a specific element in a package part</span></span>

1. <span data-ttu-id="ae1e5-244">後、 `GetXMLFromPart` **プログラム**クラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-244">After the  `GetXMLFromPart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="ae1e5-245">後、`GetXElementsByName`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-245">After the  `GetXElementsByName` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="ae1e5-246">前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-246">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
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

<span data-ttu-id="ae1e5-247">**XDocument**オブジェクト内に含まれる**XElement**オブジェクトへの参照を受けた場合は、いったんその他の XML データと同じように操作して、Visio ファイルに含まれるデータを変更できるため、します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-247">Once you have gotten a reference to a **XElement** object contained within an **XDocument** object, you can manipulate it like any other XML data and, thereby, change the data contained in the Visio file.</span></span> <span data-ttu-id="ae1e5-248">などの図形は、Visio で開いたときにテキストを持つ、対応する**図形**要素には少なくとも 1 つの**テキスト**要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-248">For example, if a shape has text when it is opened in Visio, the corresponding **Shape** element will contain at least one **Text** element.</span></span> <span data-ttu-id="ae1e5-249">その**テキスト**要素の値を変更すると、Visio でファイルを表示したときに図形のテキストが変更されます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-249">If you change the value of that **Text** element, the shape's text is changed when the file is viewed in Visio.</span></span> 
  
<span data-ttu-id="ae1e5-250">「プロセスの開始」から開始/終了図形内テキストを変更するには、**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) の**Main**メソッド**を使用して**ブロックを次のコードを追加します。スタート] ボタンを処理します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-250">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) to change the text in the Start/End shape from "Begin process" to "Start process".</span></span> 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName = "Text"
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
    Where element.Name.LocalName = "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> <span data-ttu-id="ae1e5-251">前のコード例では、既存の図形のテキストと置換に使用する文字列の文字の同じ数であります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-251">In the previous code example, the existing shape text and the string used to replace it have the same number of characters.</span></span> <span data-ttu-id="ae1e5-252">LINQ クエリが返される要素をこのケースでは、テキスト ノード) の最後の子ノードの値を変更することにも注意してください。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-252">Also note that the LINQ query changes the value of the last child node of the returned element (which, in this case, is a text node).</span></span> <span data-ttu-id="ae1e5-253">これは、は、**テキスト**要素の子である**cp**要素の設定を変更することを避けるために行われます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-253">This is done to avoid changing the settings of the **cp** element that is a child of the **Text** element.</span></span> <span data-ttu-id="ae1e5-254">> が不安定になるファイル**のテキスト**要素のすべての子を上書きすることによって図形のテキストをプログラムで変更する場合に考えられる。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-254">> It is possible to cause file instability if you alter shape text programmatically by overwriting all children of the **Text** element.</span></span> <span data-ttu-id="ae1e5-255">上記の例のようには、テキストの書式設定は、ファイル内の**テキスト**要素の下で**cp**要素によって表されます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-255">As in the example above, the text formatting is represented by **cp** elements under the **Text** element in the file.</span></span> <span data-ttu-id="ae1e5-256">書式設定の定義は、親**セクション**要素に格納されます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-256">The definition of the formatting is stored in the parent **Section** element.</span></span> <span data-ttu-id="ae1e5-257">これら 2 つの情報に不整合が生じる、し、ファイルは正常に動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-257">If these two pieces of information become inconsistent, then the file may not behave as expected.</span></span> <span data-ttu-id="ae1e5-258">Visio は、多くの矛盾を回復させますが、ファイルの最終的な動作を制御することができるように、プログラムで変更が矛盾がないことを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-258">Visio heals many inconsistencies, but it is better to ensure that any programmatic changes are consistent so that you are controlling the ultimate behavior of the file.</span></span> 
  
<span data-ttu-id="ae1e5-p126">ドキュメント パーツの XML に変更を加える場合、その変更内容はメモリ内のみに存在します。ファイル内に変更を保持するには、ドキュメント パーツに XML を戻して保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-p126">When you make changes to the XML of a document part, those changes exist in memory only. To persist the changes in the file, you must save the XML back to the document part.</span></span>
  
<span data-ttu-id="ae1e5-261">パッケージの一部に戻る、XML を記述するのに[XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx)クラスと[XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx)クラスを使用するコードを次にします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-261">The following code uses the [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) class and [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) class to write the XML back to the package part.</span></span> <span data-ttu-id="ae1e5-262">[Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx)メソッドを使用するには、一部では、 **XmlWriter**に XML を保存すると、 **XmlWriterSettings**クラスを使用するエンコードの種類を指定するなど、出力をより細かく制御します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-262">Although you can use the [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) method to save the XML back to the part, the **XmlWriter** and **XmlWriterSettings** classes allow you finer control over the output, including specifying the type of encoding.</span></span> <span data-ttu-id="ae1e5-263">**XDocument**クラスでは、 **XmlWriter**オブジェクトを取得し、XML をストリームに書き込むための[WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx)メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-263">The **XDocument** class exposes a [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) method that takes an **XmlWriter** object and writes XML back to a stream.</span></span> 
  
<span data-ttu-id="ae1e5-264">Visio のページからページの内容の一部に XML を保存するのにには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-264">Use the following procedure to save the XML from the Visio page back to the Page Contents part.</span></span>
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a><span data-ttu-id="ae1e5-265">変更した XML をパッケージに戻して保存するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-265">To save the changed XML back to the package</span></span>

1. <span data-ttu-id="ae1e5-266">後、`GetXElementByAttribute`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-266">After the  `GetXElementByAttribute` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

2. <span data-ttu-id="ae1e5-267">前の手順**を使用して**、 **Main**メソッド内のブロック コードの下にある**プログラム**のクラス (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック) に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-267">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
  ```cs
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

3. <span data-ttu-id="ae1e5-p128">F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-p128">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
4. <span data-ttu-id="ae1e5-270">Visio 2013 では、Visio の Package.vsdx ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-270">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="ae1e5-271">この時点で開始/終了図形にテキスト「Start process」が含まれているはずです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-271">The Start/End shape should now contain the text "Start process".</span></span>
  
## <a name="recalculate-data-in-the-file"></a><span data-ttu-id="ae1e5-272">ファイル内のデータを再計算する</span><span class="sxs-lookup"><span data-stu-id="ae1e5-272">Recalculate data in the file</span></span>
<span data-ttu-id="ae1e5-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-273"></span></span>

<span data-ttu-id="ae1e5-274">ファイル内のデータをいくつかの変更には、Visio ファイルを開くときにドキュメントを再計算が必要です。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-274">Some changes to the data in a file may require Visio to recalculate the document when it opens the file.</span></span> <span data-ttu-id="ae1e5-275">Visio では、図については、図形の関係の特に多くのロジックが用意されています (つまりと 1 つの図形に依存別) の図形を接続するとします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-275">Visio provides a lot of logic for a diagram, particularly for shape relationships (that is, when one shape depends on another) and connecting shapes.</span></span> <span data-ttu-id="ae1e5-276">カスタム ロジックに基づいて、データのいずれかが変更された場合、Visio はすべてのファイルに影響を受ける集計データに変更を反映する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-276">If any of the data that the custom logic relies upon is changed, Visio needs to propagate the changes to all of the affected calculated data in the file.</span></span> 
  
<span data-ttu-id="ae1e5-277">Visio 2013 のファイル形式には、ファイル内のデータを再計算するために使用できる技術のいくつかが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-277">The Visio 2013 file format includes a couple of techniques that you can use to recalculate data in the file.</span></span> <span data-ttu-id="ae1e5-278">3 種類の Visio のファイルとそれを行う方法を再計算する必要があるかどうかを決定する際に考慮する必要があるシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-278">There are three types of scenarios that you must consider when you decide whether you need to recalculate the Visio file and how to do it:</span></span>
  
- <span data-ttu-id="ae1e5-279">データへの変更は、ファイル形式でその他の値には影響しません。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-279">The changes to the data do not affect any other values in the file format.</span></span> <span data-ttu-id="ae1e5-280">Visio ドキュメントを再計算するために、追加の手順を追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-280">You don't need to add any additional instructions to Visio to recalculate the document.</span></span> <span data-ttu-id="ae1e5-281">既に示したように、ドキュメントを再計算することがなく多くの場合、図形のテキストを変更できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-281">As demonstrated previously, you can often change a shape's text without needing to recalculate the document.</span></span>
    
- <span data-ttu-id="ae1e5-282">データへの変更は、XML 内のシェイプ シート セルの値を変更して、このデータに依存するその他のシェイプ シートの値があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-282">The changes to the data are limited to changing the values of ShapeSheet cells in the XML, and there are other ShapeSheet values that depend on this data.</span></span> <span data-ttu-id="ae1e5-283">この例では、XML 処理命令が ( [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)のクラスを使用する) に変更されている**セル**要素を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-283">In this case, you must add an XML processing instruction (using the [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) class) to the **Cell** element that has been changed.</span></span> <span data-ttu-id="ae1e5-284">たとえば、図形の**ThemeIndex**セルでは、図形に含まれているいくつか他のシェイプ シート セルの値に影響します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-284">For example, the **ThemeIndex** cell for a shape affects the values of several other ShapeSheet cells contained in the shape.</span></span> <span data-ttu-id="ae1e5-285">ファイル自体 ("ThemeIndex"の**N**値を持つ**セル**要素など) に**ThemeIndex**のセルを変更する場合は、従属変数の値が更新されるように**セル**要素に処理命令を追加する必要があります。.</span><span class="sxs-lookup"><span data-stu-id="ae1e5-285">If you change the **ThemeIndex** cell within the file itself (for example, the **Cell** element with an **N** value of "ThemeIndex"), you will need to add a processing instruction to the **Cell** element so that the dependent values are updated.</span></span> 
    
- <span data-ttu-id="ae1e5-286">データへの変更には、コネクタまたは接続ポイントの位置が影響します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-286">The changes to the data affect the location of a connector or connection points.</span></span> <span data-ttu-id="ae1e5-287">別の状況は、[シェイプ シートのデータに多くの変更がありますし (それぞれの変更については、個々 の処理を追加するのではなく) 1 つの命令で文書全体を再計算するときです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-287">Another situation is when there are many changes to the ShapeSheet data and you want to recalculate the whole document with one instruction (rather than adding individual processing instructions for each change).</span></span> <span data-ttu-id="ae1e5-288">ここで開いたときにドキュメント全体を再計算するのには Visio に指示できます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-288">In this case you can instruct Visio to recalculate the entire document when it is opened.</span></span> <span data-ttu-id="ae1e5-289">カスタム ファイル プロパティ パーツに**RecalcDocument**プロパティを追加することによってこれを行う (または docProps/custom.xml) の Visio のパッケージです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-289">You do this by adding a **RecalcDocument** property to the Custom File Properties part (/docProps/custom.xml) of the Visio package.</span></span> <span data-ttu-id="ae1e5-290">位置または接続されている図で図形のサイズを調整することは、この種のシナリオの例です。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-290">Adjusting the position or size of shapes in a connected diagram is an example of this type of scenario.</span></span> 
    
    <span data-ttu-id="ae1e5-291">パフォーマンスの観点からは、このシナリオが最もコストがかかるオプションであることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-291">Keep in mind that this is the most costly option from a performance standpoint.</span></span>
    
<span data-ttu-id="ae1e5-292">同じ**図形**の場合は、他の**セル**要素の新しい値が再計算する必要があるか、**図形**の要素に**セル**要素を挿入するのには次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-292">Use the following procedure to insert a **Cell** element into a **Shape** element, where other **Cell** elements in the same **Shape** need to be recalculated because of the new value.</span></span> <span data-ttu-id="ae1e5-293">新しい**セル**要素には、いくつかローカルの再計算を実行する必要のある Visio に通知するために、子要素として処理命令が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-293">The new **Cell** element includes a processing instruction as a child element, to inform Visio that it needs to perform some local recalculation.</span></span> 
  
### <a name="to-recalculate-values-for-a-single-shape"></a><span data-ttu-id="ae1e5-294">1 つの図形の値を再計算するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-294">To recalculate values for a single shape</span></span>

1. <span data-ttu-id="ae1e5-295">前の 2 つの例のコードに置き換えます (図形のテキストとの呼び出しを変更する`SaveXDocumentToPart`) ( **Using**ブロックで、 **module1 という名前**の**Main**メソッドの**プログラム**のクラスの**Main**メソッド**を使用して**ブロックでVisual Basic) で次のコードにします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-295">Replace the code from the previous two examples (changing the shape's text and the call to  `SaveXDocumentToPart`) in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
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
  ' alrady have a local ThemeIndex cell.
  startEndShapeXML.Add(New XElement("Cell", _
      New XAttribute("N", "ThemeIndex"),
      New XAttribute("V", "25"),
      New XProcessingInstruction("NewValue", "V")))
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

2. <span data-ttu-id="ae1e5-p135">F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-p135">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
3. <span data-ttu-id="ae1e5-298">Visio 2013 では、Visio の Package.vsdx ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-298">Open the Visio Package.vsdx file in Visio 2013.</span></span> <span data-ttu-id="ae1e5-299">開始/終了図形の塗りつぶしの色ができました。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-299">The Start/End shape should now have a different fill color.</span></span>
    
<span data-ttu-id="ae1e5-300">図形の色は、 **ThemeIndex**のセルの値に依存しています: アクティブなテーマの形状を継承することを決定します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-300">The shape's color relies on the value of the **ThemeIndex** cell—it determines which of the active themes the shape inherits from.</span></span> <span data-ttu-id="ae1e5-301">前の例では、図形 ( **ThemeIndex**セルは、「25」の値に設定されます)、別のテーマを継承するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-301">In the previous example, the shape is set to inherit from a different theme (the **ThemeIndex** cell is set to a value of "25").</span></span> <span data-ttu-id="ae1e5-302">処理命令では、図形のテキストの色を使用しないかどうかは- **ThemeIndex**セルでも影響を受けるが、再計算されていません。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-302">If you don't use a processing instruction, the shape's text color—which is also affected by the **ThemeIndex** cell—isn't recalculated.</span></span> <span data-ttu-id="ae1e5-303">図形の塗りつぶしの色を白に変更は、そのテキストは白のまま、テキストを読み取り不可能なままです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-303">The shape's fill color would change to white, but its text would remain white—leaving the text unreadable.</span></span> <span data-ttu-id="ae1e5-304">また、処理命令は、それがないこと Visio が図形の更新後で、図形の書式設定の値を予期しない更新することが不安定な状態に残します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-304">Also, without the processing instruction, it is possible that Visio may update the shape at a later date, leaving the file in an unstable state where the formatting values of the shape could be updated unpredictably.</span></span> 
  
<span data-ttu-id="ae1e5-305">(たとえば、接続されている図形の位置を変更して、そのため、強制的に再ルーティングするコネクタなど)、ドキュメントを再計算するのには Visio が必要なファイル内のデータを変更する場合は、Visio ファイルに再命令を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-305">If you change data in the file that requires Visio to recalculate the document (for example, changing a connected shape's position and, therefore, forcing the connectors to reroute), you must add a recalculation instruction to the Visio file.</span></span> <span data-ttu-id="ae1e5-306">命令を作成するには、Visio ファイルのパッケージのファイルのプロパティをカスタム部分の XML を"RecalcDocument"の**名前**の属性値を持つ**プロパティ**要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-306">The instruction is created by adding a **property** element with a **name** attribute value of "RecalcDocument" to the XML of the Custom File Properties part of the Visio file package.</span></span> <span data-ttu-id="ae1e5-307">最善の方法としては、"RecalcDocument"の命令がファイルに登録されていない既にことを確認するカスタム ファイル プロパティの一部を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-307">As a best practice, you should check the Custom File Properties part to be sure that a "RecalcDocument" instruction hasn't already been registered in the file.</span></span> 
  
<span data-ttu-id="ae1e5-308">前の例と、[開始/終了] 図形の **[piny]** セルの値を変更するのにには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-308">Use the following code to change the value of the **PinY** cell of the Start/End shape from the previous examples.</span></span> <span data-ttu-id="ae1e5-309">コードは、 **N**属性の値を使用しての**XElement**オブジェクトとして **[piny]** セルのデータを含む**セル**要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-309">The code selects the **Cell** element that contains the **PinY** cell data as an **XElement** object by using the value of its **N** attribute.</span></span> <span data-ttu-id="ae1e5-310">コードは、Visio ファイルのカスタム ファイル プロパティ パーツにし、再計算の命令を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-310">The code then adds a recalculation instruction to the Custom File Properties part of the Visio file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ae1e5-311">このコードに依存しています、`GetPackagePart`と`SaveXDocumentToPart`メソッドが以前に作成します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-311">This code relies on the  `GetPackagePart` and  `SaveXDocumentToPart` methods created previously.</span></span> 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a><span data-ttu-id="ae1e5-312">ドキュメントが開いている場合にそのドキュメント全体を再計算するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-312">To recalculate the entire document when it is opened</span></span>

1. <span data-ttu-id="ae1e5-313">後、`SaveXDocumentToPart`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-313">After the  `SaveXDocumentToPart` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
  ```cs
  private static void RecalcDocument(Package filePackage)
  {
      // Get the Custom File Properties part from the package and
      // and then extract the XML from it.
      PackagePart customPart = GetPackagePart(filePackage, 
          "http://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
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
              "http://schemas.openxmlformats.org/officeDocument/2006/" + _
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

2. <span data-ttu-id="ae1e5-314">後、`RecalcDocument`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-314">After the  `RecalcDocument` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="ae1e5-315">(Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック)、**プログラム**のクラスの**Main**メソッド内に、 **using**ブロックの前の例のコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-315">Replace the code from the previous example in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
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

4. <span data-ttu-id="ae1e5-p140">F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-p140">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="ae1e5-318">Visio 2013 では、Visio の Package.vsdx ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-318">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="ae1e5-319">開始/終了図形には、図面の下端からの 2 インチがはずです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-319">The Start/End shape should now be 2 inches from the bottom edge of the drawing.</span></span> <span data-ttu-id="ae1e5-320">開始/終了図形と、[処理] 図形間のコネクタは、レイアウトの変更に対応するために再ルーティングがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-320">The connector between the Start/End shape and the Process shape should have rerouted to accommodate the change in layout.</span></span> <span data-ttu-id="ae1e5-321">**RecalcDocument**プロパティは、ファイルに追加されていませんが、図形の位置が変更されていること、ですが、コネクタは図形の新しい場所に再ルーティングがありません。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-321">If the **RecalcDocument** property had not been added to the file, the shape position would have been changed, but the connector would not have rerouted to the new location of the shape.</span></span> 
  
## <a name="add-a-new-package-part-to-a-package"></a><span data-ttu-id="ae1e5-322">新しいパッケージ パーツをパッケージに追加する</span><span class="sxs-lookup"><span data-stu-id="ae1e5-322">Add a new package part to a package</span></span>
<span data-ttu-id="ae1e5-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-323"></span></span>

<span data-ttu-id="ae1e5-324">新しいドキュメント パーツをパッケージに追加ファイルのパッケージを変更するための最も一般的なシナリオの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-324">One of the most common scenarios for modifying a file package is adding a new document part to the package.</span></span> <span data-ttu-id="ae1e5-325">たとえば、パッケージにコンテンツを追加することで図面にページを追加する場合は、ページの内容の一部をパッケージに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-325">For example, if you want to add a page to the Visio drawing by adding content to the package, you need to add a Page Contents part to the package.</span></span> 
  
<span data-ttu-id="ae1e5-326">次のように、パッケージに新しいパーツを追加するプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-326">The process for adding a new part to the package is straightforward:</span></span> 
  
1. <span data-ttu-id="ae1e5-327">**PackagePart**のデータを使用して XML ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-327">You create the XML document with the data for the **PackagePart**.</span></span> <span data-ttu-id="ae1e5-328">XML 名前空間を作成する XML ドキュメントの特定の種類のスキーマを管理するには特に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-328">You need to pay special attention to the XML namespaces that govern the schema for the specific type of XML document that you create.</span></span>
    
2. <span data-ttu-id="ae1e5-329">XML が含まれているし、**パッケージ**内の場所にファイルを保存する新しいファイルを作成するとします。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-329">You create a new file to contain the XML and save the file to a location in the **Package**.</span></span>
    
3. <span data-ttu-id="ae1e5-330">新しい**PackagePart**や**パッケージ**またはその他の**PackagePart**オブジェクトの間で必要な関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-330">You create the necessary relationships between the new **PackagePart** and the **Package** or other **PackagePart** objects.</span></span> 
    
4. <span data-ttu-id="ae1e5-p144">新しいパーツを参照する必要がある既存のパーツを更新します。たとえば、新しいページ コンテンツ パーツ (新しいページ) をファイルに追加する場合は、ページ インデックス パーツ (/visio/pages/pages.xml ファイル) を更新し、新しいページに関する正しい情報を組み込む必要もあります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-p144">You update any existing parts that need to reference the new part. For example, if you add a new Page Contents part (a new page) to the file, you also need to update the Page Index part (/visio/pages/pages.xml file) to include the correct information about the new page.</span></span>
    
<span data-ttu-id="ae1e5-333">Visio ファイルに新しいリボン機能拡張パーツを作成するのにには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-333">Use the following procedure to create a new Ribbon Extensibility part in the Visio file.</span></span> <span data-ttu-id="ae1e5-334">新しいリボンの機能拡張の一部は、1 つのボタンを含む 1 つのグループを使用して新しいタブをリボンに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-334">The new Ribbon Extensibility part adds to the ribbon a new tab with a single group that contains a single button.</span></span>
  
### <a name="to-create-a-new-package-part"></a><span data-ttu-id="ae1e5-335">新しいパッケージ パーツを作成するには</span><span class="sxs-lookup"><span data-stu-id="ae1e5-335">To create a new package part</span></span>

1. <span data-ttu-id="ae1e5-336">後、`CheckForRecalc`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-336">After the  `CheckForRecalc` method in the **Program** class (or **Module1** in Visual Basic) from the previous procedure, add the following method.</span></span> 
    
  ```cs
  private static XDocument CreateCustomUI()
  {
      // Add a new Custom User Interface document part to the package.
      // This code adds a new CUSTOM tab to the ribbon for this
      // document. The tab has one group that contains one button.
      XNamespace customUINS = 
          "http://schemas.microsoft.com/office/2006/01/customui";
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
          "http://schemas.microsoft.com/office/2006/01/customui"
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

2. <span data-ttu-id="ae1e5-337">後、`CreateCustomUI`から前の手順では、**プログラム**のクラス (または Visual Basic では**Module1** ) 内のメソッドは、以下のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-337">After the  `CreateCustomUI` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="ae1e5-338">次のコード**を使用して**コードをブロックする (Visual Basic では、 **module1 という名前**の**メイン**メソッドの**Using**ブロック)、**プログラム**のクラスの**Main**メソッド内のすべてを交換してください。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-338">Replace all the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
  ```cs
  // Create a new Ribbon Extensibility part and add it to the file.
  XDocument customUIXML = CreateCustomUI();
  CreateNewPackagePart(visioPackage, customUIXML, 
      new Uri("/customUI/customUI1.xml", UriKind.Relative),
      "application/xml",
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
  ```

  ```vb
  ' Create a new Ribbon Extensibility part and add it to the file.
  Dim customUIXML As XDocument = CreateCustomUI()
  CreateNewPackagePart(visioPackage, customUIXML, _
      New Uri("/customUI/customUI1.xml", UriKind.Relative), _
      "application/xml", _
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
  ```

4. <span data-ttu-id="ae1e5-p146">F5 キーを選択してソリューションをデバッグします。プログラムの実行が完了したら、任意のキーを選択して終了します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-p146">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="ae1e5-341">Visio 2013 年に Package.vsdx の Visio ファイルを開くし、[**ユーザー設定**] タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-341">Open the Visio Package.vsdx file in Visio 2013, and then choose the **CUSTOM** tab.</span></span> 
    
<span data-ttu-id="ae1e5-342">カスタム リボンは、Visio 2013 でファイルを開いたときに、図 2 のように見えます。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-342">The custom ribbon looks like Figure 2 when the file is opened in Visio 2013.</span></span>
  
 <span data-ttu-id="ae1e5-343">**図 2 になります。Visio 2013 のリボンの [カスタム] タブ**</span><span class="sxs-lookup"><span data-stu-id="ae1e5-343">**Figure 2. Custom tab in the Visio 2013 ribbon**</span></span>
  
![リボンのカスタム タブ](media/vis15_CustomRibbonTab.PNG)
  
<span data-ttu-id="ae1e5-345">によって作成された、XML、`CreateCustomUI`メソッドは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-345">The XML created by the  `CreateCustomUI` method looks like the following.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="http://schemas.microsoft.com/office/2006/01/customui">
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

## <a name="acknowledgements"></a><span data-ttu-id="ae1e5-346">謝辞</span><span class="sxs-lookup"><span data-stu-id="ae1e5-346">Acknowledgements</span></span>
<span data-ttu-id="ae1e5-347"><a name="vis15_ManipulateFF_Ackn"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-347"></span></span>

<span data-ttu-id="ae1e5-348">貢献し、この技術情報に含まれているコード例を作成するのには、Visio の MVP **Al Edlund**の入力を認識しております。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-348">We would like to recognize the contribution and input of Visio MVP **Al Edlund** in creating the code examples contained in this technical article.</span></span> <span data-ttu-id="ae1e5-349">Al は、Visio XML 図面 (.vdx) 形式と新しい Visio ファイル形式 (.vsdx) の両方を含め、Visio のファイル形式を操作するときに認識されているエキスパートです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-349">Al is a recognized expert in manipulating the Visio file format, including both the Visio XML Drawing format (.vdx) and the new Visio file format (.vsdx).</span></span> <span data-ttu-id="ae1e5-350">Al は、プログラムで、Visio のファイル形式を表示するプロジェクトが作成し、内部構造を公開します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-350">Al has created projects that explore the Visio file formats programmatically and exposes the structures inside.</span></span> 
  
<span data-ttu-id="ae1e5-351">Visio ファイル形式での作業の詳細については、以下については、ここにリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-351">For more information about Al's work with the Visio file format, see the links in the Additional Resources section that follows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae1e5-352">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae1e5-352">See also</span></span>
<span data-ttu-id="ae1e5-353"><a name="vis15_ManipulateFF_Additional"> </a></span><span class="sxs-lookup"><span data-stu-id="ae1e5-353"></span></span>

- <span data-ttu-id="ae1e5-354">Al Edlund 提供:</span><span class="sxs-lookup"><span data-stu-id="ae1e5-354">By Al Edlund:</span></span>
    
  - <span data-ttu-id="ae1e5-355">CodePlex で[pkgVisio の Visio 2013 の XML の操作](http://pkgvisio.codeplex.com/documentation)のプロジェクトです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-355">[pkgVisio - Visio 2013 XML manipulation](http://pkgvisio.codeplex.com/documentation) project on CodePlex.</span></span> 
    
  - <span data-ttu-id="ae1e5-356">[pkgVisio_pt1](http://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) YouTube のビデオです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-356">[pkgVisio_pt1 ](http://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) video on YouTube.</span></span> 
    
  - <span data-ttu-id="ae1e5-357">[pkgVisio_pt2](http://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) YouTube のビデオです。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-357">[pkgVisio_pt2 ](http://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) video on YouTube.</span></span> 
    
- [<span data-ttu-id="ae1e5-358">Visio デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="ae1e5-358">Visio Developer Center</span></span>](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [<span data-ttu-id="ae1e5-359">Office オープン XML 形式のドキュメントを操作します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-359">Manipulate Office Open XML Formats Documents</span></span>](http://msdn.microsoft.com/en-us/library/aa982683%28v=office.12%29.aspx)
    
- [<span data-ttu-id="ae1e5-360">名前空間 (C#) (LINQ to XML) ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-360">Create a Document with Namespaces (C#) (LINQ to XML)</span></span>](http://msdn.microsoft.com/en-us/library/bb387075.aspx)
    
- [<span data-ttu-id="ae1e5-361">Microsoft Office を起動することがなく、ドキュメントにカスタム XML 部分を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae1e5-361">Add Custom XML Parts to Documents Without Starting Microsoft Office</span></span>](http://msdn.microsoft.com/en-us/library/bb608597%28VS.90%29.aspx)
    

