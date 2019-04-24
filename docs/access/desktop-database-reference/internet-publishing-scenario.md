---
title: Internet Publishing シナリオ
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291273"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="a4211-102">Internet Publishing シナリオ</span><span class="sxs-lookup"><span data-stu-id="a4211-102">Internet publishing scenario</span></span>

<span data-ttu-id="a4211-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4211-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4211-p101">ここに示すコード例では、ADO を Microsoft OLE DB Provider for Internet Publishing と共に使用する方法を示します。このシナリオでは、 **Recordset** 、 **Record** 、および **Stream** の各オブジェクトを使用して Internet Publishing Provider で発行されたリソースのコンテンツを表示する Visual Basic アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a4211-p101">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing. In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="a4211-106">このシナリオを作成するには、次の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="a4211-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="a4211-107">Visual Basic プロジェクトをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="a4211-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="a4211-108">メインリストボックスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a4211-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="a4211-109">[Fields] リストボックスに値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a4211-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="a4211-110">[詳細] テキストボックスに値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a4211-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="a4211-111">手順 1: Visual Basic プロジェクトをセットアップする</span><span class="sxs-lookup"><span data-stu-id="a4211-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="a4211-112">このシナリオでは、システムに Microsoft Visual Basic 6.0 以降、ADO 2.5 以降、および Microsoft OLE DB Provider for Internet Publishing がインストールされていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="a4211-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="a4211-113">ADO プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="a4211-113">Create an ADO project</span></span>

1.  <span data-ttu-id="a4211-114">Microsoft Visual Basic で、新規の標準 EXE プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a4211-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="a4211-115">From the **Project** menu, choose **References**.</span><span class="sxs-lookup"><span data-stu-id="a4211-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="a4211-116">[ **Microsoft ActiveX データオブジェクト2.5 ライブラリ**] を選択し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a4211-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="a4211-117">メインフォームにコントロールを挿入する</span><span class="sxs-lookup"><span data-stu-id="a4211-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="a4211-118">Form1 に ListBox コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a4211-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="a4211-119">**Name**プロパティを**lstMain**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a4211-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="a4211-120">Form1 にもう 1 つの ListBox コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a4211-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="a4211-121">**Name**プロパティを**lstDetails**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a4211-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="a4211-122">Form1 に TextBox コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a4211-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="a4211-123">" **Name/名前**" プロパティを**txtdetails**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a4211-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="a4211-124">手順 2: メインリストボックスを初期化する</span><span class="sxs-lookup"><span data-stu-id="a4211-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="a4211-125">グローバルレコードオブジェクトと Recordset オブジェクトを宣言する</span><span class="sxs-lookup"><span data-stu-id="a4211-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="a4211-126">Form1 の (General) (Declarations) に次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a4211-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="a4211-127">このコードによって、このシナリオで後ほど使用する **Record** オブジェクトと **Recordset** オブジェクトへのグローバル オブジェクト参照を宣言します。</span><span class="sxs-lookup"><span data-stu-id="a4211-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="a4211-128">URL に接続し、lstMain に入力します。</span><span class="sxs-lookup"><span data-stu-id="a4211-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="a4211-129">Form1 の Form Load イベント ハンドラーに次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a4211-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   <span data-ttu-id="a4211-130">このコードによって、グローバルな **Record** オブジェクトと **Recordset** オブジェクトのインスタンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a4211-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="a4211-131">**ActiveConnection**として指定された URL を使用して、 **Record** `grec`が開かれます。</span><span class="sxs-lookup"><span data-stu-id="a4211-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="a4211-132">URL が存在する場合は開かれますが、存在しない場合は作成されます。</span><span class="sxs-lookup"><span data-stu-id="a4211-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="a4211-133">ご使用の環境から`https://servername/foldername/`有効な URL に置き換える必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a4211-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="a4211-134">**Recordset** `grs`は、 **Record** `grec`の子に対して開かれます。</span><span class="sxs-lookup"><span data-stu-id="a4211-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="a4211-135">lstMain には、URL に発行されたリソースのファイル名が設定されます。</span><span class="sxs-lookup"><span data-stu-id="a4211-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="a4211-136">手順 3: Fields リストボックスに値を設定する</span><span class="sxs-lookup"><span data-stu-id="a4211-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="a4211-137">lstMain の Click イベント ハンドラーに次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a4211-137">Insert the following code into the Click event handler of lstMain:</span></span>

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   <span data-ttu-id="a4211-138">このコードでは、ローカルの**Record**オブジェクトと`rec` **Recordset**オブジェクトの宣言とインスタンス化を`rs`それぞれ行います。</span><span class="sxs-lookup"><span data-stu-id="a4211-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="a4211-139">lstMain で選択されているリソースに対応する行が、の`grs`現在の行になります。</span><span class="sxs-lookup"><span data-stu-id="a4211-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="a4211-140">その後、**詳細**リストボックスがクリア`rec`され、ソースとして`grs`の現在の行を使用して開きます。</span><span class="sxs-lookup"><span data-stu-id="a4211-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="a4211-141">リソースが**RecordType**で指定されているようにコレクションレコードである場合、ローカルの**Recordset** `rs`はの`rec`子で開かれます。</span><span class="sxs-lookup"><span data-stu-id="a4211-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="a4211-142">lstDetails には、の`rs`行の値が入力されます。</span><span class="sxs-lookup"><span data-stu-id="a4211-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="a4211-143">リソースが単純なレコードである場合`recFields`は、が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a4211-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="a4211-144">の詳細につい`recFields`ては、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4211-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="a4211-145">リソースが構造化ドキュメントである場合は、コードは実装されません。</span><span class="sxs-lookup"><span data-stu-id="a4211-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="a4211-146">手順 4: [詳細] テキストボックスに値を設定する</span><span class="sxs-lookup"><span data-stu-id="a4211-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="a4211-147">という名前`recFields`の新しいサブルーチンを作成し、次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a4211-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   <span data-ttu-id="a4211-148">このコードによって、lstDetails に`recFields`、渡される単純なレコードのフィールドと値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="a4211-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="a4211-149">リソースがテキスト ファイルである場合は、テキスト **Stream** がリソース レコードから開かれます。</span><span class="sxs-lookup"><span data-stu-id="a4211-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="a4211-150">コードは、文字セットが ASCII であるかどうかを\*\*\*\* 判断し、 `txtDetails`ストリームの内容をにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a4211-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

