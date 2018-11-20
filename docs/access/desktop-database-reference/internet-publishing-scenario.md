---
title: Internet Publishing シナリオ
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f481c4bc5cf11f9345458b3859c099b40a79885
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026450"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="a86d0-102">Internet Publishing シナリオ</span><span class="sxs-lookup"><span data-stu-id="a86d0-102">Internet publishing scenario</span></span>

<span data-ttu-id="a86d0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a86d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a86d0-p101">ここに示すコード例では、ADO を Microsoft OLE DB Provider for Internet Publishing と共に使用する方法を示します。このシナリオでは、 **Recordset** 、 **Record** 、および **Stream** の各オブジェクトを使用して Internet Publishing Provider で発行されたリソースのコンテンツを表示する Visual Basic アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-p101">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing. In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="a86d0-106">このシナリオを作成するには、次の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="a86d0-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="a86d0-107">Visual Basic プロジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="a86d0-108">メイン リスト ボックスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="a86d0-109">フィールドのリスト ボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="a86d0-110">[詳細] テキスト ボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="a86d0-111">手順 1: Visual Basic プロジェクトのセットアップします。</span><span class="sxs-lookup"><span data-stu-id="a86d0-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="a86d0-112">このシナリオでは、システムに Microsoft Visual Basic 6.0 以降、ADO 2.5 以降、および Microsoft OLE DB Provider for Internet Publishing がインストールされていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="a86d0-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="a86d0-113">ADO プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-113">Create an ADO project</span></span>

1.  <span data-ttu-id="a86d0-114">Microsoft Visual Basic で、新規の標準 EXE プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="a86d0-115">**プロジェクト**] メニューの [**参照設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a86d0-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="a86d0-116">**Microsoft ActiveX データ オブジェクトの 2.5 ライブラリ**を選択し、し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a86d0-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="a86d0-117">メイン フォーム上のコントロールを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="a86d0-118">Form1 に ListBox コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="a86d0-119">**Name**プロパティを**lstMain**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="a86d0-120">Form1 にもう 1 つの ListBox コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="a86d0-121">**Name**プロパティを**lstDetails**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="a86d0-122">Form1 に TextBox コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="a86d0-123">**Name**プロパティを**txtDetails**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="a86d0-124">手順 2: Main リスト ボックスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="a86d0-125">グローバル レコードとレコード セット オブジェクトを宣言します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="a86d0-126">Form1 の (General) (Declarations) に次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="a86d0-127">このコードによって、このシナリオで後ほど使用する **Record** オブジェクトと **Recordset** オブジェクトへのグローバル オブジェクト参照を宣言します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="a86d0-128">URL に接続し、lstMain に設定</span><span class="sxs-lookup"><span data-stu-id="a86d0-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="a86d0-129">Form1 の Form Load イベント ハンドラーに次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
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
    
   <span data-ttu-id="a86d0-130">このコードによって、グローバルな **Record** オブジェクトと **Recordset** オブジェクトのインスタンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a86d0-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="a86d0-131">**レコード** `grec` **ActiveConnection**として指定された URL を使用して開かれました。</span><span class="sxs-lookup"><span data-stu-id="a86d0-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="a86d0-132">URL が存在する場合は開かれますが、存在しない場合は作成されます。</span><span class="sxs-lookup"><span data-stu-id="a86d0-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="a86d0-133">交換する必要があることに注意`https://servername/foldername/`お客様の環境からの有効な URL を使用しています。</span><span class="sxs-lookup"><span data-stu-id="a86d0-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="a86d0-134">**レコード セット** `grs` **レコード**の子に対して開かれた`grec`。</span><span class="sxs-lookup"><span data-stu-id="a86d0-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="a86d0-135">LstMain には、URL に公開されたリソースのファイル名が、表示されます。</span><span class="sxs-lookup"><span data-stu-id="a86d0-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="a86d0-136">手順 3: フィールド リスト ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="a86d0-137">lstMain の Click イベント ハンドラーに次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-137">Insert the following code into the Click event handler of lstMain:</span></span>

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

   <span data-ttu-id="a86d0-138">このコードを宣言し、ローカルの**レコード**と**レコード セット**オブジェクトのインスタンスを作成する`rec`と`rs`それぞれ。</span><span class="sxs-lookup"><span data-stu-id="a86d0-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="a86d0-139">LstMain 内で選択されたリソースに対応する行の現在の行を加え、 `grs`。</span><span class="sxs-lookup"><span data-stu-id="a86d0-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="a86d0-140">**詳細**のリスト ボックスをオフにし、および`rec`の現在の行で開かれた`grs`ソースとして。</span><span class="sxs-lookup"><span data-stu-id="a86d0-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="a86d0-141">リソースの場合、コレクションを記録 (指定されている**RecordType**によって)、ローカル**レコード セット**`rs`の子で開かれた`rec`。</span><span class="sxs-lookup"><span data-stu-id="a86d0-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="a86d0-142">lstDetails の行から値を入力し、 `rs`。</span><span class="sxs-lookup"><span data-stu-id="a86d0-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="a86d0-143">リソースが、単純なレコードの場合`recFields`と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a86d0-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="a86d0-144">詳細については`recFields`、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a86d0-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="a86d0-145">リソースが構造化ドキュメントである場合は、コードは実装されません。</span><span class="sxs-lookup"><span data-stu-id="a86d0-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="a86d0-146">手順 4: [詳細] テキスト ボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="a86d0-147">という名前のサブルーチンを作成する`recFields`し、次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="a86d0-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

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

   <span data-ttu-id="a86d0-148">このコード フィールドが lstDetails に設定し、単純なレコードの値に渡される`recFields`。</span><span class="sxs-lookup"><span data-stu-id="a86d0-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="a86d0-149">リソースがテキスト ファイルである場合は、テキスト **Stream** がリソース レコードから開かれます。</span><span class="sxs-lookup"><span data-stu-id="a86d0-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="a86d0-150">コードかどうかを文字セットは ASCII に**ストリーム**の内容をコピー `txtDetails`。</span><span class="sxs-lookup"><span data-stu-id="a86d0-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

