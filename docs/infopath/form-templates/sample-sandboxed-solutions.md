---
title: サンドボックス ソリューションのサンプル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: このトピックでは、InfoPath セキュリティで保護されたソリューションでフォーム テンプレートを発行する方法として使用できる 2 つのコード例について説明します。
ms.openlocfilehash: 56a9a2a765100ef327790265c7cf734903268bed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303501"
---
# <a name="sample-sandboxed-solutions"></a>サンドボックス ソリューションのサンプル

マネージ コードを持つ InfoPath フォームを、InfoPath デザイン モードから SharePoint セキュリティで保護されたソリューション インフラストラクチャに発行できます。このトピックでは、InfoPath セキュリティで保護されたソリューションでフォーム テンプレートを発行する方法として使用できる 2 つのコード例について説明します。
  
## <a name="example-1-sorting-data-in-an-order-form"></a>例 1: 注文フォーム内のデータの並べ替え

InfoPath フォームでコードを使用して実行できる便利な作業の例として、繰り返しテーブルでのデータの並べ替えがあります。それには、InfoPath フォームに表示されている基になる XML ドキュメントのノードについて、それらをコードを使用して並べ替えます。このトピックで説明するシナリオでは InfoPath からセキュリティで保護されたソリューションとして直接発行することを目的としていますが、管理者承認用フォーム テンプレートとして展開することもできます。
  
作業を始める前に、次の条件を満たしていることを確認してください。
  
- フォームを発行する SharePoint Server 2010 または SharePoint Foundation 2010 サイトのサイト コレクション管理者であること。
    
- Microsoft SharePoint Foundation Sandboxed Code Service がサーバー上で動作していることを、ファーム管理者とともに確認します。詳細については、「[コードを含むフォームを発行する](publishing-forms-with-code.md)」を参照してください。
    
- フォーム テンプレートに対して選択したプログラミング言語が、以前のバージョン名が付いていない **C#** または **Visual Basic** のどちらかであること。 プログラミング言語とオブジェクト モデルの InfoPath 2007 互換バージョンと InfoPath 2003 互換バージョンでは。サンドボックス ソリューションはサポートされていません。 プログラミング言語を指定する方法の詳細については、「[Visual Studio での開発](how-to-develop-with-visual-studio.md)」を参照してください。
    
フォームの **[繰り返しテーブル]** コントロールでデータを並べ替えるフォーム テンプレートを作成するには、次の手順を実行します。 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>フォーム内のデータをプログラムによって並べ替えるフォーム テンプレートを作成するには

1. InfoPath デザイン モードで新しいフォーム テンプレートを作成し、 **繰り返しテーブル** コントロールをフォームに追加します。この例のサンプル コードではテーブルの 1 列目を基準として行を並べ替えていますが、任意の列を基準とするように簡単にコードを変更できます。 
    
2. **ボタン** コントロールをフォームに追加します。テーブルを並べ替えるためのコードはボタンの **Clicked** イベントのイベント ハンドラーに追加されますが、別のイベントを使用することもできます。 
    
3. ボタンを選択し、[ **プロパティ**] タブをクリックし、[ **ユーザー設定コード**] をクリックします。フォームをまだ保存していない場合は、保存を促すメッセージが表示され、コード エディターが開いてカーソルがボタンのイベント ハンドラーに設定されます。
    
4. 次のコードをボタンのイベント ハンドラーに貼り付けます。1 列目の要素が配列に格納され、配列が並べ替えられた後、その配列を基準として表が並べ替えられます。このコードでは、並べ替えられるデータを文字列データと仮定しています。
    
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

5. 次の手順を実行してフォームを発行します。
    
    1. Backstage の **[発行]** タブで **[SharePoint Server]** をクリックします。 
        
    2. 発行先の SharePoint サイトの URL を入力し、[ **次へ**] をクリックします。 
        
       > [!IMPORTANT]
       > このフォーム テンプレートをセキュリティで保護されたソリューションとして発行するためには、このサイトのサイト コレクション管理者である必要があります。 
    
    3. [ **フォーム ライブラリ**] をクリックし、[ **次へ**] をクリックします。
        
    4. [ **新しいフォーム ライブラリを作成する**] をクリックし、[ **次へ**] をクリックします。
        
    5. フォーム ライブラリの名前と説明を入力し、[ **次へ**] をクリックします。
        
    6. **[発行]** をクリックします。
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>例 2: SharePoint リストでのベンダーの管理

この例では、Microsoft SharePoint Foundation 2010 のオブジェクト モデルに対するプログラミングを行います。それには、Microsoft.SharePoint.dll アセンブリへの参照を設定する必要があります。Microsoft.SharePoint.dll は、ライセンスが付与された SharePoint Server 2010 のコピーと共にインストールされています。
  
Microsoft.SharePoint.Server.dll は、既定で C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI にインストールされています。この DLL を、SharePoint オブジェクト モデルに対するプログラミングを行うプロジェクトにインクルードする必要があります。Visual Studio 2012 プロジェクトの中で Microsoft.SharePoint.dll への参照を設定するには、 **コード エディター**を開き、[ **プロジェクト**] メニューの [ **参照の追加**] をクリックします。[ **参照の追加**] ダイアログ ボックスで [ **参照**] タブをクリックし、Microsoft.SharePoint.dll ファイルの場所を指定して [ **OK**] をクリックします。これで、Microsoft.SharePoint.dll がプロジェクト ディレクトリにコピーされ、SharePoint Foundation 2010 オブジェクト モデルのメンバーを InfoPath ソリューションの中で使用できるようになります。
  
### <a name="designing-the-form-and-developing-the-code"></a>フォームのデザインとコードの作成

InfoPath フォームのコードから、SharePoint オブジェクト モデルを使用して参照リスト内にアイテムを作成できます。これは、SharePoint リストからドロップダウン ボックスを設定して、別のフォームを作成せずに新しい値を追加する場合に便利です。この例ではコンボ ボックスを使用して、現在リストにあるすべての値を表示し、まだ値が存在していない場合に値をリストに追加するプログラミング ロジックを作成します。
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>SharePoint リストに基づいてコンボ ボックスに新しいアイテムを追加できるフォーム テンプレートを作成するには

1. SharePoint Server 2010 のサーバー上に簡単なユーザー設定リストを作成し、それに MyList という名前をつけます。以下の例では、このリストの **Title** フィールドにバインドされている **コンボ ボックス**を使用します。 
    
2. InfoPath Designer に新しい **空白のフォーム**を作成し、フォーム上に **コンボ ボックス** コントロールを挿入して、コンボ ボックスにバインドされているフィールドの名前を myCombo に変更します。
    
3. 次の手順を実行して、コンボ ボックスへの値の読み込みに使用するデータ接続をリストに追加します。
    
    1. **[データ]** タブの **[外部データの取得]** グループで **[SharePoint リストから]** ボタンをクリックします。 
        
    2. リストのあるサイトの URL を入力し、[ **次へ**] をクリックします。
        
    3. リストを選択し、[ **次へ**] をクリックします。
        
    4. 追加するフィールドを選択します。この例では、Title と ID を選択します。 Title には参照用の値が格納されます。[ **次へ**] をクリックします。
        
    5. 次の画面で [ **次へ**] をクリックします。 
        
    6. データ接続に LookupList という名前を指定し、**[完了]** をクリックします。
    
4. 次の手順を実行して、コンボ ボックス内の値をリストから読み込みます。
    
    1. 手順 1 で作成したコンボ ボックスを選択します。
        
    2. リボンの [コントロール ツール] の [ **プロパティ**] タブで [ **選択肢の編集**] をクリックします。 
        
    3. [ **外部データ ソースから選択肢を取得する**] をクリックします。
        
    4. [ **データ ソース**] に、手順 2. で作成したデータ接続が設定されていることを確認します。 
        
    5. 値と表示名を Title に設定します。
        
    6. [ **ブラウザー フォーム**] タブで、[ **ポストバックの設定**] の下の [ **常に送信する**] を選択してから、[ **OK**] をクリックしてプロパティ ダイアログ ボックスを閉じます。 
    
5. コンボ ボックスが選択されたままであることを確認し、リボンの [ **開発**] タブの [ **Changed イベント**] をクリックします。 
    
    フォームをまだ保存していない場合は、保存を促すメッセージが表示されます。その後、コード エディターのウィンドウが開いて、カーソルが  `myCombo_Changed` イベント ハンドラーの中に表示されます。 
    
6. このトピックで前述したように、Microsoft.SharePoint.dll アセンブリへの参照を追加します。 Microsoft.SharePoint アセンブリの参照に関する詳細については、「[SharePoint オブジェクト モデルのメンバーを使用する](how-to-use-sharepoint-object-model-members.md)」を参照してください。
    
7. 次のコードを `myCombo_Changed` イベント ハンドラーに貼り付けます。 
    
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

8. 上記のコード例は、`GetDomValue` ヘルパー関数に応じて異なります。`myCombo_Changed` イベント ハンドラー関数の下に、次の `GetDomValue` ヘルパー関数のコードを貼り付けます。 
    
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

9. 次の手順を実行してフォームを発行します。
    
    1. Backstage の **[発行]** タブで **[SharePoint Server]** をクリックします。 
        
    2. 発行先の SharePoint サイトの URL を入力し、[ **次へ**] をクリックします。 
        
       > [!IMPORTANT]
       > このフォーム テンプレートをセキュリティで保護されたソリューションとして発行するためには、このサイトのサイト コレクション管理者である必要があります。 
    
    3. [ **フォーム ライブラリ**] をクリックし、[ **次へ**] をクリックします。
        
    4. [ **新しいフォーム ライブラリを作成する**] をクリックし、[ **次へ**] をクリックします。
        
    5. フォーム ライブラリの名前と説明を入力し、[ **次へ**] をクリックします。
        
    6. [ **発行**] をクリックします。
        
    7. フォームの発行が成功したら、フォーム ライブラリからフォームを開き、コンボ ボックスに新しい値を追加して、コードをテストします。myCombo フィールドを出ると、新しい値は SharePoint リストに書き込まれます。 
    

