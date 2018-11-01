---
title: Microsoft Visual Basic で ADO を使用する
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8644bd4f5b1a19848689adf92dca91ba30f324c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889848"
---
# <a name="using-ado-with-microsoft-visual-basic"></a><span data-ttu-id="9c70c-102">Microsoft Visual Basic での ADO の使用</span><span class="sxs-lookup"><span data-stu-id="9c70c-102">Using ADO with Microsoft Visual Basic</span></span>


<span data-ttu-id="9c70c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9c70c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c70c-p101">ADO プロジェクトのセットアップおよび ADO コードの作成は、Visual Basic と Visual Basic for Applications のどちらを使用する場合でもほとんど同じです。このトピックでは、Visual Basic と Visual Basic for Applications での ADO の使用方法と両者の相違点について説明します。</span><span class="sxs-lookup"><span data-stu-id="9c70c-p101">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications. This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="9c70c-106">ADO ライブラリの参照</span><span class="sxs-lookup"><span data-stu-id="9c70c-106">Referencing the ADO Library</span></span>

<span data-ttu-id="9c70c-107">プロジェクトでは ADO ライブラリを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c70c-107">The ADO library must be referenced by your project.</span></span>

<span data-ttu-id="9c70c-108">**Microsoft Visual Basic から ADO を参照するには**</span><span class="sxs-lookup"><span data-stu-id="9c70c-108">**To reference ADO from Microsoft Visual Basic**</span></span>

1.  <span data-ttu-id="9c70c-109">Visual Basic で、[ **プロジェクト** ] メニューの [ **参照設定** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9c70c-109">In Visual Basic, from the **Project** menu, select **References...**.</span></span>

2.  <span data-ttu-id="9c70c-p102">一覧の [ **Microsoft ActiveX Data Objects x.x Library** ] をクリックします。少なくとも、次のライブラリが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9c70c-p102">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="9c70c-112">Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="9c70c-112">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="9c70c-113">Visual Basic ランタイム オブジェクトとプロシージャ</span><span class="sxs-lookup"><span data-stu-id="9c70c-113">Visual Basic runtime objects and procedures</span></span>
    
    - <span data-ttu-id="9c70c-114">Visual Basic オブジェクトとプロシージャ</span><span class="sxs-lookup"><span data-stu-id="9c70c-114">Visual Basic objects and procedures</span></span>
    
    - <span data-ttu-id="9c70c-115">OLE オートメーション</span><span class="sxs-lookup"><span data-stu-id="9c70c-115">OLE Automation</span></span>

3.  <span data-ttu-id="9c70c-116">[ **OK** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9c70c-116">Click **OK**.</span></span>

<span data-ttu-id="9c70c-117">たとえば、Microsoft Access を使用して、Visual Basic for Applications と同じように簡単に ADO を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c70c-117">You can use ADO just as easily with Visual Basic for Applications, using Microsoft Access, for example.</span></span>

<span data-ttu-id="9c70c-118">**Microsoft Access から ADO を参照するには**</span><span class="sxs-lookup"><span data-stu-id="9c70c-118">**To reference ADO from Microsoft Access**</span></span>

1.  <span data-ttu-id="9c70c-119">Microsoft Access の [ **データベース** ] ウィンドウの [ **モジュール** ] タブで、モジュールを選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="9c70c-119">In Microsoft Access, select or create a module from the **Modules** tab in the **Database** window.</span></span>

2.  <span data-ttu-id="9c70c-120">[ **ツール** ] メニューの [ **参照設定** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c70c-120">From the **Tools** menu, select **References...**.</span></span>

3.  <span data-ttu-id="9c70c-p103">一覧の [ **Microsoft ActiveX Data Objects x.x Library** ] をクリックします。少なくとも、次のライブラリが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9c70c-p103">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="9c70c-123">Visual Basic for Applications</span><span class="sxs-lookup"><span data-stu-id="9c70c-123">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="9c70c-124">Microsoft Access 11.0 オブジェクト ライブラリ (またはそれ以降のバージョン)</span><span class="sxs-lookup"><span data-stu-id="9c70c-124">Microsoft Access 11.0 Object Library (or later)</span></span>

4.  <span data-ttu-id="9c70c-125">[ **OK** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9c70c-125">Click **OK**.</span></span>

## <a name="creating-ado-objects-in-visual-basic"></a><span data-ttu-id="9c70c-126">Visual Basic で ADO オブジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="9c70c-126">Creating ADO Objects in Visual Basic</span></span>

<span data-ttu-id="9c70c-127">オートメーション変数を作成し、その変数に対するオブジェクトのインスタンスを作成するには、 **Dim** メソッドまたは **CreateObject** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c70c-127">To create an automation variable and an instance of an object for that variable, you can use two methods: **Dim** or **CreateObject**.</span></span>

## <a name="dim"></a><span data-ttu-id="9c70c-128">Dim</span><span class="sxs-lookup"><span data-stu-id="9c70c-128">Dim</span></span>

<span data-ttu-id="9c70c-129">**Dim** の **New** キーワードを使用すると、一度に ADO オブジェクトの作成とインスタンス化を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9c70c-129">You can use the **New** keyword with **Dim** to declare and instantiate ADO objects in one step:</span></span>

```vb 
 
Dim conn As New ADODB.Connection 
```

<span data-ttu-id="9c70c-130">または、 **Dim** ステートメントの宣言とオブジェクトのインスタンス化を 2 段階で行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="9c70c-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span></span>

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```


> [!NOTE]
> <P><span data-ttu-id="9c70c-p104">プロジェクトで ADO ライブラリが正しく参照されていれば、<STRONG>Dim</STRONG> ステートメントで ADODB progid を明示的に使用する必要はありません。ただし、明示的に使用することで、他のライブラリとの命名の競合を確実に回避できます。</span><span class="sxs-lookup"><span data-stu-id="9c70c-p104">It is not required to explicitly use the ADODB progid with the <STRONG>Dim</STRONG> statement, assuming you have properly referenced the ADO library in your project. However, using it ensures that you won't have naming conflicts with other libraries.</span></span></P>



<span data-ttu-id="9c70c-133">たとえば、同じプロジェクトに ADO と DAO に対する参照がどちらも含まれる場合は、 **Recordset** オブジェクトをインスタンス化するときに、次のコードで示すように、どちらのオブジェクト モデルを使用するのかを指定する修飾子を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c70c-133">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating **Recordset** objects, as in the following code:</span></span>  
<span data-ttu-id="9c70c-134">どちらを暗きます。レコード セット</span><span class="sxs-lookup"><span data-stu-id="9c70c-134">Dim adoRS As ADODB.Recordset</span></span>  
  
<span data-ttu-id="9c70c-135">Dim daoRS と仮定します。レコード セット</span><span class="sxs-lookup"><span data-stu-id="9c70c-135">Dim daoRS As DAO.Recordset</span></span>

## <a name="createobject"></a><span data-ttu-id="9c70c-136">CreateObject</span><span class="sxs-lookup"><span data-stu-id="9c70c-136">CreateObject</span></span>

<span data-ttu-id="9c70c-137">**CreateObject** メソッドでは、2 つの異なる手順で宣言とオブジェクトのインスタンス化を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c70c-137">With the **CreateObject** method, the declaration and object instantiation must be two discrete steps:</span></span>

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

<span data-ttu-id="9c70c-p105">**CreateObject** でインスタンス化されたオブジェクトは、実行時にバインドされます。つまり、型が明確に決定されていないため、完全にコマンド ラインを確定できません。ただし、プロジェクトから ADO ライブラリに対する参照を省略することはでき、特定のバージョンのオブジェクトをインスタンス化できます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9c70c-p105">Objects instantiated with **CreateObject** are late-bound, which means that they are not strongly typed and command-line completion is disabled. However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects. For example:</span></span>

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

<span data-ttu-id="9c70c-141">また、ADO Version 2.0 タイプ ライブラリに対する参照を明確に作成し、オブジェクトを作成することで、これを実現することもできます。</span><span class="sxs-lookup"><span data-stu-id="9c70c-141">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</span></span>

<span data-ttu-id="9c70c-142">**CreateObject** メソッドでのオブジェクトのインスタンス化は、通常、 **Dim** ステートメントを使用する場合より時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="9c70c-142">Instantiating objects with the **CreateObject** method is typically slower than using the **Dim** statement.</span></span>

## <a name="handling-events"></a><span data-ttu-id="9c70c-143">イベントの処理</span><span class="sxs-lookup"><span data-stu-id="9c70c-143">Handling Events</span></span>

<span data-ttu-id="9c70c-p106">Microsoft Visual Basic で ADO イベントを処理するには、 **WithEvents** キーワードを使用してモジュール レベルの変数を宣言する必要があります。変数は、クラス モジュールの一部としてのみ宣言することができ、モジュール レベルで宣言する必要があります。ADO イベントの処理方法の詳細については、「 [7 章: ADO イベントを処理する](chapter-7-handling-ado-events.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c70c-p106">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword. The variable can be declared only as part of a class module and must be declared at the module level. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

## <a name="visual-basic-examples"></a><span data-ttu-id="9c70c-147">Visual Basic の例</span><span class="sxs-lookup"><span data-stu-id="9c70c-147">Visual Basic Examples</span></span>

<span data-ttu-id="9c70c-148">ADO のマニュアルには、Visual Basic での例が数多く含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c70c-148">Many Visual Basic examples are included with the ADO documentation.</span></span> <span data-ttu-id="9c70c-149">詳細については、 [Microsoft Visual Basic で ADO コードの例](ado-code-examples-in-microsoft-visual-basic.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c70c-149">For more information, see [ADO code examples in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span></span>

