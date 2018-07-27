---
title: サンドボックス ソリューションのサンプル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: このトピックでは、InfoPath セキュリティで保護されたソリューションでフォーム テンプレートを発行する方法として使用できる 2 つのコード例について説明します。
ms.openlocfilehash: b0874e34d843850df55eee87d689ce0d01112635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799214"
---
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="e5321-103">サンドボックス ソリューションのサンプル</span><span class="sxs-lookup"><span data-stu-id="e5321-103">Sample Sandboxed Solutions</span></span>

<span data-ttu-id="e5321-p101">マネージ コードを持つ InfoPath フォームを、InfoPath デザイン モードから SharePoint セキュリティで保護されたソリューション インフラストラクチャに発行できます。このトピックでは、InfoPath セキュリティで保護されたソリューションでフォーム テンプレートを発行する方法として使用できる 2 つのコード例について説明します。</span><span class="sxs-lookup"><span data-stu-id="e5321-p101">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer. This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="e5321-106">例 1: 注文フォーム内のデータの並べ替え</span><span class="sxs-lookup"><span data-stu-id="e5321-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="e5321-p102">InfoPath フォームでコードを使用して実行できる便利な作業の例として、繰り返しテーブルでのデータの並べ替えがあります。それには、InfoPath フォームに表示されている基になる XML ドキュメントのノードについて、それらをコードを使用して並べ替えます。このトピックで説明するシナリオでは InfoPath からセキュリティで保護されたソリューションとして直接発行することを目的としていますが、管理者承認用フォーム テンプレートとして展開することもできます。</span><span class="sxs-lookup"><span data-stu-id="e5321-p102">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table. To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form. Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="e5321-110">作業を始める前に、次の条件を満たしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e5321-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="e5321-111">フォームを発行する SharePoint Server 2010 または SharePoint Foundation 2010 サイトのサイト コレクション管理者であること。</span><span class="sxs-lookup"><span data-stu-id="e5321-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="e5321-p103">Microsoft SharePoint Foundation Sandboxed Code Service がサーバー上で動作していることを、ファーム管理者とともに確認します。詳細については、「[コードを含むフォームを発行する](publishing-forms-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5321-p103">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server. For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="e5321-114">フォーム テンプレートに対して選択したプログラミング言語が、以前のバージョン名が付いていない **C#** または **Visual Basic** のどちらかであること。</span><span class="sxs-lookup"><span data-stu-id="e5321-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="e5321-115">プログラミング言語とオブジェクト モデルの InfoPath 2007 互換バージョンと InfoPath 2003 互換バージョンでは。サンドボックス ソリューションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e5321-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="e5321-116">プログラミング言語を指定する方法の詳細については、「[Visual Studio での開発](how-to-develop-with-visual-studio.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5321-116">For more information about how to specify the programming language, see [How to: Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="e5321-117">フォームの **[繰り返しテーブル]** コントロールでデータを並べ替えるフォーム テンプレートを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e5321-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="e5321-118">フォーム内のデータをプログラムによって並べ替えるフォーム テンプレートを作成するには</span><span class="sxs-lookup"><span data-stu-id="e5321-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="e5321-p105">InfoPath デザイン モードで新しいフォーム テンプレートを作成し、 **繰り返しテーブル** コントロールをフォームに追加します。この例のサンプル コードではテーブルの 1 列目を基準として行を並べ替えていますが、任意の列を基準とするように簡単にコードを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e5321-p105">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form. The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="e5321-p106">**ボタン** コントロールをフォームに追加します。テーブルを並べ替えるためのコードはボタンの **Clicked** イベントのイベント ハンドラーに追加されますが、別のイベントを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="e5321-p106">Add a **Button** control to the form. The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="e5321-p107">ボタンを選択し、[ **プロパティ**] タブをクリックし、[ **ユーザー設定コード**] をクリックします。フォームをまだ保存していない場合は、保存を促すメッセージが表示され、コード エディターが開いてカーソルがボタンのイベント ハンドラーに設定されます。</span><span class="sxs-lookup"><span data-stu-id="e5321-p107">Select the button, click the **Properties** tab, and then click **Custom Code**. If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="e5321-p108">次のコードをボタンのイベント ハンドラーに貼り付けます。1 列目の要素が配列に格納され、配列が並べ替えられた後、その配列を基準として表が並べ替えられます。このコードでは、並べ替えられるデータを文字列データと仮定しています。</span><span class="sxs-lookup"><span data-stu-id="e5321-p108">Paste the following code into the button's event handler. The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array. This code assumes that the data being sorted is string data.</span></span>
    
   ```cs
    // Put the elements from the first column into an array.
    XPathNavigator root = this.CreateNavigator();
        
    // Create a node iterator which contains only the values that you want to sort.
    // For this form, the entire table is in "group1", each row is a "group2"
    // and the rows are "field1", "field2" and "field3" respectively.
    XPathNodeIterator nodeIterator = root.Select(
        "/my:myFields/my:group1/my:group2/my:field1", this.NamespaceManager);
        
    // Create arrays to use for sorting.
    string[] sortArrayWords = new string[nodeIterator.Count + 1];
    int[] sortArrayKeys = new int[nodeIterator.Count + 1];
    int arrayPosition = 1;
        
    // Populate the arrays for sorting.
    while (nodeIterator.MoveNext()) 
    {
        // Loop until there are no more elements
        sortArrayWords[arrayPosition] = nodeIterator.Current.Value;
        sortArrayKeys[arrayPosition] = arrayPosition;
        arrayPosition += 1;
    }
        
    // Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys);
    arrayPosition = 0;
        
    // Create new XML to update the table.
    string newTableXML = "";
    // Iterate through the sorted array of keys.
    for (int i = 1; i <= sortArrayWords.Length - 1; i++) 
    {
        nodeIterator = root.Select(
            "/my:myFields/my:group1/my:group2", this.NamespaceManager);
            
        // Go to the right position in the table.
        for (int j = 1; j <= sortArrayKeys[i]; j++) 
        {
            nodeIterator.MoveNext();
        }
            
        // Add the row to the XML.
        newTableXML += nodeIterator.Current.OuterXml;
    }
        
    // Set the table to use the new XML.
    root.SelectSingleNode(
        "/my:myFields/my:group1", this.NamespaceManager).InnerXml = newTableXML;
    
   ```

   ```vb
    ' Put the elements from the first column into an array.
    Dim root As XPathNavigator = Me.CreateNavigator
    ' Create a node iterator which contains only the values that you want to sort
    ' For this form, the entire table is in "group1",
    ' each row is a "group2"
    ' and the rows are "field1", "field2" and "field3" respectively.
    Dim nodeIterator As XPathNodeIterator = root.Select( _
        "/my:myFields/my:group1/my:group2/my:field1", Me.NamespaceManager)
    ' Create arrays to use for sorting.
    Dim sortArrayWords(nodeIterator.Count) As String
    Dim sortArrayKeys(nodeIterator.Count) As Integer
    Dim arrayPosition As Integer = 1
    ' Populate the arrays for sorting.
    While nodeIterator.MoveNext() ' Loop until there are no more elements
        sortArrayWords(arrayPosition) = nodeIterator.Current.Value
        sortArrayKeys(arrayPosition) = arrayPosition
        arrayPosition += 1
    End While
    ' Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys)
    arrayPosition = 0
    ' Create new XML to update the table.
    Dim newTableXML As String = ""
    ' Iterate through the sorted array of keys.
    For i As Integer = 1 To sortArrayWords.Length - 1
        nodeIterator = root.Select( _
            "/my:myFields/my:group1/my:group2", Me.NamespaceManager)
        ' Go to the right position in the table.
        For j As Integer = 1 To sortArrayKeys(i)
        nodeIterator.MoveNext()
        Next
    ' Add the row to the XML.
    newTableXML &amp;= nodeIterator.Current.OuterXml
    Next
    ' Set the table to use the new XML.
    root.SelectSingleNode("/my:myFields/my:group1", _
        Me.NamespaceManager).InnerXml = newTableXML
   ```

5. <span data-ttu-id="e5321-128">次の手順を実行してフォームを発行します。</span><span class="sxs-lookup"><span data-stu-id="e5321-128">Publish your form by using the following steps.</span></span>
    
    1. <span data-ttu-id="e5321-129">Backstage の **[発行]** タブで **[SharePoint Server]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="e5321-130">発行先の SharePoint サイトの URL を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="e5321-131">このフォーム テンプレートをセキュリティで保護されたソリューションとして発行するためには、このサイトのサイト コレクション管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5321-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="e5321-132">[ **フォーム ライブラリ**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="e5321-133">[ **新しいフォーム ライブラリを作成する**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="e5321-134">フォーム ライブラリの名前と説明を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="e5321-135">**[発行]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="e5321-136">例 2: SharePoint リストでのベンダーの管理</span><span class="sxs-lookup"><span data-stu-id="e5321-136">Example 2: Managing Vendors in a SharePoint List</span></span>

<span data-ttu-id="e5321-p109">この例では、Microsoft SharePoint Foundation 2010 のオブジェクト モデルに対するプログラミングを行います。それには、Microsoft.SharePoint.dll アセンブリへの参照を設定する必要があります。Microsoft.SharePoint.dll は、ライセンスが付与された SharePoint Server 2010 のコピーと共にインストールされています。</span><span class="sxs-lookup"><span data-stu-id="e5321-p109">This example involves programming against the Microsoft SharePoint Foundation 2010 object model. To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="e5321-p110">Microsoft.SharePoint.Server.dll は、既定で C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI にインストールされています。この DLL を、SharePoint オブジェクト モデルに対するプログラミングを行うプロジェクトにインクルードする必要があります。Visual Studio 2012 プロジェクトの中で Microsoft.SharePoint.dll への参照を設定するには、 **コード エディター**を開き、[ **プロジェクト**] メニューの [ **参照の追加**] をクリックします。[ **参照の追加**] ダイアログ ボックスで [ **参照**] タブをクリックし、Microsoft.SharePoint.dll ファイルの場所を指定して [ **OK**] をクリックします。これで、Microsoft.SharePoint.dll がプロジェクト ディレクトリにコピーされ、SharePoint Foundation 2010 オブジェクト モデルのメンバーを InfoPath ソリューションの中で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e5321-p110">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default. This DLL must be included in projects where you program against the SharePoint object model. To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu. In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**. This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="e5321-144">フォームのデザインとコードの作成</span><span class="sxs-lookup"><span data-stu-id="e5321-144">Designing the Form and Developing the Code</span></span>

<span data-ttu-id="e5321-p111">InfoPath フォームのコードから、SharePoint オブジェクト モデルを使用して参照リスト内にアイテムを作成できます。これは、SharePoint リストからドロップダウン ボックスを設定して、別のフォームを作成せずに新しい値を追加する場合に便利です。この例ではコンボ ボックスを使用して、現在リストにあるすべての値を表示し、まだ値が存在していない場合に値をリストに追加するプログラミング ロジックを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5321-p111">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists. This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form. This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="e5321-148">SharePoint リストに基づいてコンボ ボックスに新しいアイテムを追加できるフォーム テンプレートを作成するには</span><span class="sxs-lookup"><span data-stu-id="e5321-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="e5321-p112">SharePoint Server 2010 のサーバー上に簡単なユーザー設定リストを作成し、それに MyList という名前をつけます。以下の例では、このリストの **Title** フィールドにバインドされている **コンボ ボックス**を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5321-p112">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList. The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="e5321-151">InfoPath Designer に新しい **空白のフォーム**を作成し、フォーム上に **コンボ ボックス** コントロールを挿入して、コンボ ボックスにバインドされているフィールドの名前を myCombo に変更します。</span><span class="sxs-lookup"><span data-stu-id="e5321-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="e5321-152">次の手順を実行して、コンボ ボックスへの値の読み込みに使用するデータ接続をリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="e5321-152">Create the data connection to the list that will be used to populate the combo box by using the following steps.</span></span>
    
    1. <span data-ttu-id="e5321-153">**[データ]** タブの **[外部データの取得]** グループで **[SharePoint リストから]** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="e5321-154">リストのあるサイトの URL を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="e5321-155">リストを選択し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="e5321-p113">追加するフィールドを選択します。この例では、Title と ID を選択します。 Title には参照用の値が格納されます。[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-p113">Select the fields that you want to include, for this example, select Title and ID. Title contains the values for lookup. Click **Next**.</span></span>
        
    5. <span data-ttu-id="e5321-159">次の画面で [ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="e5321-160">データ接続に LookupList という名前を指定し、**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="e5321-161">次の手順を実行して、コンボ ボックス内の値をリストから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="e5321-161">Populate the values in the combo box from the list by using the following steps.</span></span>
    
    1. <span data-ttu-id="e5321-162">手順 1 で作成したコンボ ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5321-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="e5321-163">リボンの [コントロール ツール] の [ **プロパティ**] タブで [ **選択肢の編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="e5321-164">[ **外部データ ソースから選択肢を取得する**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="e5321-165">[ **データ ソース**] に、手順 2. で作成したデータ接続が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5321-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="e5321-166">値と表示名を Title に設定します。</span><span class="sxs-lookup"><span data-stu-id="e5321-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="e5321-167">[ **ブラウザー フォーム**] タブで、[ **ポストバックの設定**] の下の [ **常に送信する**] を選択してから、[ **OK**] をクリックしてプロパティ ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e5321-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="e5321-168">コンボ ボックスが選択されたままであることを確認し、リボンの [ **開発**] タブの [ **Changed イベント**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="e5321-p114">フォームをまだ保存していない場合は、保存を促すメッセージが表示されます。その後、コード エディターのウィンドウが開いて、カーソルが  `myCombo_Changed` イベント ハンドラーの中に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5321-p114">If your form is not saved yet, you are prompted to save it. And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="e5321-171">このトピックで前述したように、Microsoft.SharePoint.dll アセンブリへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="e5321-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="e5321-172">Microsoft.SharePoint アセンブリの参照に関する詳細については、「[SharePoint オブジェクト モデルのメンバーを使用する](how-to-use-sharepoint-object-model-members.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5321-172">For more information about referencing the Microsoft.SharePoint assembly, see [How to: Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="e5321-173">次のコードを `myCombo_Changed` イベント ハンドラーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="e5321-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
   ```cs
    // Use InfoPath OM's ServerInfo.SharePointSiteUrl property to programmatically
    // specify the site where the form is published.
    using (SPSite FormSite = new SPSite(ServerInfo.SharePointSiteUrl.ToString()))
    {
        using (SPWeb FormWeb = FormSite.OpenWeb())
        {
            // Get the SharePoint list.
            SPList LookupList = FormWeb.Lists["MyList"];
            // Query for the item.
            SPQuery MyQuery = new SPQuery();
            // "Title" is the field (column) to search in the SharePoint list.
            // /my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" + 
                GetDomValue("/my:myFields/my:myCombo") + "</Value></Eq></Where>";
            SPListItemCollection ReturnedItems = LookupList.GetItems(MyQuery);
            // Add the item to the SharePoint list if no items were returned in the query.
            if (ReturnedItems.Count == 0)
            {
                SPListItem NewItem = LookupList.Items.Add();
                // Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem["Title"] = GetDomValue("/my:myFields/my:myCombo");
                // Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = true;
                NewItem.Update();
                // Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = false;
            }
        }
    }
   ```

   ```vb
    ' Use InfoPath OM's ServerInfo.SharePointSiteUrl property to specify the site where the form is published.
    Using FormSite As New SPSite(ServerInfo.SharePointSiteUrl.ToString())
        Using FormWeb As SPWeb = FormSite.OpenWeb()
            ' Get the SharePoint list.
            Dim LookupList As SPList = FormWeb.Lists("MyList")
            ' Query for the item.
            Dim MyQuery As New SPQuery()
            ' "Title" is the field (column) to search in the SharePoint list.
            ' my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" &amp; _
                GetDomValue("/my:myFields/my:myCombo") &amp; "</Value></Eq></Where>"
            Dim ReturnedItems As SPListItemCollection = LookupList.GetItems(MyQuery)
            ' Add the item to the lookup list if no items were returned in the query.
            If ReturnedItems.Count = 0 Then
                Dim NewItem As SPListItem = LookupList.Items.Add()
                ' Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem("Title") = GetDomValue("/my:myFields/my:myCombo")
                ' Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = True
                NewItem.Update()
                ' Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = False
            End If
        End Using
    End Using
   ```

8. <span data-ttu-id="e5321-p116">上記のコード例は、`GetDomValue` ヘルパー関数に応じて異なります。`myCombo_Changed` イベント ハンドラー関数の下に、次の `GetDomValue` ヘルパー関数のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="e5321-p116">The preceding code example depends on the  `GetDomValue` helper function. Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
   ```cs
    private string GetDomValue(string XpathToGet)
    {
        return this.CreateNavigator().SelectSingleNode(XpathToGet, this.NamespaceManager).Value;
    }
   ```

   ```vb
    Private Function GetDomValue(XpathToGet As String) As String
        Return Me.CreateNavigator().SelectSingleNode(XpathToGet, Me.NamespaceManager).Value
    End Function
   ```

9. <span data-ttu-id="e5321-176">次の手順を実行してフォームを発行します。</span><span class="sxs-lookup"><span data-stu-id="e5321-176">Publish your form by using the following steps.</span></span>
    
    1. <span data-ttu-id="e5321-177">Backstage の **[発行]** タブで **[SharePoint Server]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="e5321-178">発行先の SharePoint サイトの URL を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="e5321-179">このフォーム テンプレートをセキュリティで保護されたソリューションとして発行するためには、このサイトのサイト コレクション管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5321-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="e5321-180">[ **フォーム ライブラリ**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="e5321-181">[ **新しいフォーム ライブラリを作成する**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="e5321-182">フォーム ライブラリの名前と説明を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="e5321-183">[ **発行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5321-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="e5321-p117">フォームの発行が成功したら、フォーム ライブラリからフォームを開き、コンボ ボックスに新しい値を追加して、コードをテストします。myCombo フィールドを出ると、新しい値は SharePoint リストに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="e5321-p117">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code. When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

