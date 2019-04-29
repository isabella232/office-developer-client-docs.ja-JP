---
title: Application インターフェイス (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: Application インターフェイスには、OneNote の情報とコンテンツの取得、操作、および更新に役立つメソッドが含まれています。 こうしたメソッドは、次の 4 つの一般的なカテゴリに分けられます。
localization_priority: Priority
ms.openlocfilehash: 20b2fc42711aaf4f1b407efb2c70057bd88a9046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303109"
---
# <a name="application-interface-onenote"></a>Application インターフェイス (OneNote)

**Application** インターフェイスには、OneNote の情報とコンテンツの取得、操作、および更新に役立つメソッドが含まれています。 こうしたメソッドは、次の 4 つの一般的なカテゴリに分けられます。 
  
- **ノートブック構造** &ndash; ノートブックの構造を操作するためのメソッド。ノートブック、セクション グループ、およびセクションの探索、オープン、変更、クローズ、および削除に対応するメソッドが含まれます。 
    
- **ページ コンテンツ** &ndash; ページおよびページ コンテンツを操作するためのメソッド。ページ コンテンツの探索、変更、保存、および削除に対応するメソッドが含まれます。 ページ コンテンツには、バイナリ オブジェクト (インクやイメージなど)、およびテキスト オブジェクト (アウトラインなど) が含まれます。 
    
- **ナビゲーション** &ndash; ページおよびオブジェクトの検索、リンク、およびナビゲーションのためのメソッド。 
    
- **機能性** &ndash; その他すべてのメソッド。OneNote の特定のアクションを実行したり、パラメーターを設定したりするメソッドです。 
    
さらに、**Application** インターフェイスには、いくつかの*プロパティ*と*イベント*が含まれています。 
  
## <a name="notebook-structure-methods"></a>ノートブック構造のメソッド
<a name="ON14DevRef_Application_NotebookStructure"> </a>

このセクションで説明するメソッドを使用すると、OneNote のノートブック、セクション グループ、およびセクションを探索、オープン、変更、クローズ、および削除できます。
  
### <a name="gethierarchy-method"></a>GetHierarchy メソッド

|||
|:-----|:-----|
|**説明** <br/> |ノートブックのノード階層構造を取得します。指定したノード (すべてのノートブックまたは単一のノートブック、セクション グループ、またはセクション) から指定したレベルまでのすべての子孫を取得します。  <br/> |
|**構文** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**パラメーター** <br/> | _bstrStartNodeID_ &ndash; 取得対象の子孫を持つノード (ノートブック、セクション グループ、またはセクション)。 Null 文字列 ("") を渡すと、このメソッドではルート ノード以下のすべてのノード (すべてのノートブック、セクション グループ、およびセクション) が取得されます。 ノートブック、セクション グループ、またはセクションのノードを指定すると、そのノードの子孫のみが取得されます。  <br/><br/>_hsScope_ &ndash; 取得対象の最下位の子孫ノードのレベル。 たとえば、ページを指定すると、このメソッドではページ レベルまでのすべてのノードが取得されます。 セクションを指定すると、ノートブックの下位にあるセクション ノードのみが取得されます。 詳細については、「[列挙型](enumerations-onenote-developer-reference.md#odc_HierarchyScope)」トピックの **HierarchyScope** 列挙型を参照してください。  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; (出力パラメーター) 文字列へのポインター。OneNote は、その文字列に XML 出力を書き込みます。  <br/><br/>_xsSchema_ &ndash; (省略可能) 出力する OneNote XML スキーマのバージョン (**XMLSchema** 型)。 XML スキーマのバージョンは、2013、2010、2007、または現行のバージョンを指定できます。  <br/><br/>**注**: OneNote の将来のバージョンでもアドインが動作するように、**xsCurrent** を使用したり、空白のままにしたりするのではなく、OneNote のバージョン (**xs2013**) を指定するようにしてください。           |
   
GetHierarchy メソッドは、既定で OneNote 2013 XML 形式の文字列を返します。また、省略可能な _xsSchema_ パラメーターを使用すると、適切な XML スキーマのバージョンを設定できます。 
  
どのパラメーターを渡すかによって、**GetHierarchy** メソッドは異なるリストを返すようになります (たとえば、すべてのノートブック、すべてのノートブックに含まれるすべてのセクション、特定のセクション内のすべてのページ、特定のノートブック内のすべてのページなど)。 それぞれのノードごとに、プロパティ (セクションやページのタイトル、ID、最終更新時刻など) の情報を示す XML 文字列が返されます。 
  
開始ノードと範囲の組み合わせには有効でないものがあります。 たとえば、セクションの開始ノードとノートブックの範囲を指定すると、ノード階層でのノートブックはセクションよりも上位になるため、**GetHierarchy** は Null の結果を返します。 
  
次の C# の例は、**GetHierarchy** メソッドを使用して、すべてのノートブックを含む OneNote 階層全体をページ レベルまで取得する方法を示しています。 出力文字列はクリップボードにコピーされるため、その文字列はテキスト エディターに貼り付けて確認してください。 
  
```cs
static void GetEntireHierarchy()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(null, 
            OneNote.HierarchyScope.hsPages, out strXML);
        Clipboard.SetText(strXML);
        MessageBox.Show("The XML has been copied to the clipboard");
    }

```

### <a name="updatehierarchy-method"></a>UpdateHierarchy メソッド

|||
|:-----|:-----|
|**説明**|ノートブックの階層を変更または更新します。 たとえば、ノートブックへのセクションまたはセクション グループの追加、新しいノートブックの追加、ノートブック内でのセクションの移動、セクション名の変更、セクションへのページの追加、セクション内でのページ順序の変更などが可能です。|
|**構文**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**パラメーター**| _bstrChangesXmlIn_ &ndash; 階層への変更を指定する OneNote XML コードが含まれている文字列。 たとえば、新しいセクションを挿入する場合は、この XML 文字列に **Section** 要素を追加して、新しいセクションの追加位置を指定します。 また、既存のセクションの名前を変更する場合は、XML コード内でセクション ID を変更せずに、そのセクションの **name** 属性を変更します。<br/><br/>_xsSchema_ &ndash; (省略可能) 文字列 _bstrChangesXmln_ の OneNote スキーマ バージョン。 この省略可能な値は、_bstrChangesXmlIn_ 文字列の OneNote XML スキーマ バージョンを指定するために使用します。 この値が指定されてないと、OneNote は XML のスキーマ バージョンが _xsCurrent_ であると仮定します。 <br/><br/>**注**: OneNote の将来のバージョンでもアドインが動作するように、**xsCurrent** を使用したり、空白のままにしたりするのではなく、OneNote のバージョン (**xs2013**) を指定するようにしてください。           |
   
_bstrChangesXmlIn_ パラメーターに部分的な OneNote XML 文字列のみを渡すと、OneNote によって変更部分の推測が試行されます。 たとえば、1 つのセクションのみを含む **Notebook** 要素を含めると、OneNote は、そのセクションを既存のセクションの最後に追加します。 ただし、あいまいな操作の指定については、その結果を判断することが困難になります。 たとえば、既存のノートブックに 4 つのセクションが含まれているときに、そのノートブックと 4 番目のセクションおよび 1 番目のセクションのみが (この順序で) 含まれている XML 文字列を渡すと、OneNote は 2 番目と 3 番目のセクションを 4 番目のセクションの前に配置することも、1 番目のセクションの後に配置することもあります。 
  
**UpdateHierarchy** メソッドを使用して、ノートブックの一部を削除することはできません。 つまり、既存の階層の一部のみを含む XML 文字列を渡しても、その文字列に含まれていないセクションは削除されません。 階層の一部を削除する場合は、**DeleteHierarchy** メソッドを使用してください。 
  
次の C# コードは、**UpdateHierarchy** メソッドを使用して OneNote 階層を変更する方法の一例を示しています。このコードでは、既存のセクションの名前を変更します。 ここでは、ドライブ C のルートにある ChangeSectionName.xml というサンプル ファイルから XML コードを読み取って、XML ドキュメントに読み込んでから、そのドキュメントの XML 構造をメソッドに渡しています。 
  
```cs
static void UpdateExistingHierarchy()
    {
        OneNote.Application onApplication = new OneNote.Application();
        
        // Get the XML from the file.
        XmlTextReader reader = new XmlTextReader("C:\\ChangeSectionName.xml");
        reader.WhitespaceHandling = WhitespaceHandling.None;
        XmlDocument xmlDocIn = new XmlDocument();
        xmlDocIn.Load(reader);
        
        // Update the hierarchy.
        onApplication.UpdateHierarchy(xmlDocIn.OuterXml,
        OneNote.XMLSchema.xs2007);   
    }

```

次の XML コードは、前述の C# コードでメソッドに渡した ChangeSectionName.xml ファイルの抜粋です。 この XML を **UpdateHierarchy** メソッドに渡すと、既存の階層に含まれるセクションの 1 つの名前が変更されます (**name** 属性の値が "My Renamed Section" に変更されます)。 その後で、名前を変更したもの以外のすべてのセクションが削除されます。 さらに、このコードではターゲットの **Section** 要素から不要な属性 (**lastModifiedTime**、**isCurrentlyViewed**、**color** などの属性) が削除され、属性の **name**、**ID**、および **path** のみがそのまま残されます。 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="https://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

前述の XML コードは、**GetHierarchy** メソッドの例で示したコードを使用して取得したものですが、範囲をセクションに限定するために、次に示す変更が加えられています。 
  
```cs
static void GetAllSections()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(System.String.Empty, 
            OneNote.HierarchyScope.hsSections, out strXML);
        Clipboard.SetText(strXML.ToString());
        MessageBox.Show("The XML has been copied to the Clipboard");
    }

```

次の C# の例は、完全なコンソール アプリケーションを示しています。この例では、"`Sample_Section`" という名前のセクションを検索して、そのセクションの新しい名前を入力するようにユーザーに求め、**UpdateHierarchy** メソッドを使用して、セクション名をユーザーが入力した名前に変更します。 このコードの実行前に、OneNote 階層に存在するセクションの名前を "`Sample_Section`" に変更しておいてください。
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "https://schemas.microsoft.com/office/onenote/2013/onenote";
        string outputXML;
        Application onApplication = new Application();
        onApplication.GetHierarchy(null, HierarchyScope.hsSections, out outputXML);
        // Load a new XmlDocument.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.LoadXml(outputXML);
        XmlNamespaceManager nsmgr = new XmlNamespaceManager(xmlDoc.NameTable);
            nsmgr.AddNamespace("one", strNamespace);
        // Search for the section named "Sample_Section".
        XmlNode xmlNode = xmlDoc.SelectSingleNode("//one:Section[@name='Sample_Section']", nsmgr);
        // Prompt for a new section title.
        System.Console.Write("Please enter a new title for the section: ");
        string input = System.Console.ReadLine();
        xmlNode.Attributes["name"].Value = input; 
        // Update the section with the new title.
        onApp.UpdateHierarchy(xmlNode.OuterXml);
        System.Console.Write("Done!\n");
    }

```

### <a name="openhierarchy-method"></a>OpenHierarchy メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したセクション グループまたはセクションを開きます。  <br/> |
|**構文** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**パラメーター** <br/> | _bstrPath_ &ndash; 開くパス。 ノートブックの場合やノートブック内のセクション グループの場合、_bstrPath_ は .one セクション ファイルへのパスにすることも、フォルダー パスにすることもできます。 .one セクション ファイルへのパスを指定する場合は、ファイル パス文字列に .one 拡張子を含める必要があります。  <br/><br/>_bstrRelativeToObjectID_ &ndash; 新しく開くオブジェクトの親オブジェクト (ノートブックまたはセクション グループ) の OneNote ID。 _bstrPath_ パラメーターが絶対パスの場合は、空の文字列 ("") の _bstrRelativeToObjectID_ を渡すことができます。 また、作成するオブジェクト (セクションまたはセクション グループ) の格納先ノートブックまたはセクション グループのオブジェクト ID を渡して、その親オブジェクトの下に作成するオブジェクトのファイル名 (section1.one など) を指定することもできます。  <br/><br/>_pbstrObjectID_ &ndash; (出力パラメーター) **OpenHierarchy** メソッドで開くノートブック、セクション グループ、またはセクションに対応する OneNote から返されるオブジェクト ID。 このパラメーターは、このメソッドが ID を書き込む文字列へのポインターです。  <br/><br/>_cftlfNotExist_ &ndash; (省略可能) [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType) 列挙型の列挙値。 _cftIfNotExist_ で値を渡すと、**OpenHierarchy** メソッドは指定したパスにセクション グループまたはセクションのファイルを作成します (そのファイルが存在しない場合のみ)。  <br/> |
   
開いているノートブックに含まれていないセクション グループを指定すると、**OpenHierarchy** メソッドはセクション グループをノートブックとして開きます。 開いているノートブックに含まれていないセクションを指定すると、**OpenHierarchy** メソッドは Recent Opened Sections セクション グループにセクションを開きます。 開いているノートブックに含まれているセクション グループまたはセクションを指定しても何も起こりません。そのセクション グループまたはセクションは既に開いています。 どの場合も、**OpenHierarchy** は指定されたセクション グループ、ノートブック、またはセクションのオブジェクト ID を返します。その ID は別の操作で使用できます。 
  
また、新しいセクションを作成するために XML をインポートするのではなく、**OpenHierarchy** メソッドを使用することもできます。 
  
次のコードは、**OpenHierarchy** メソッドを使用して、Work ノートブックの Meetings セクションを開いて、そのセクションの ID を取得する方法を示しています。 そのセクションが存在していない場合は、OneNote によって指定の場所にセクションが作成されます。 
  
```cs
static void OpenSection()
    {
        String strID;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.OpenHierarchy("C:\\Documents and Settings\\user\\My Documents\\OneNote Notebooks\\Work\\Meetings.one", 
        System.String.Empty, out strID, OneNote.CreateFileType.cftSection);
    }

```

### <a name="deletehierarchy-method"></a>DeleteHierarchy メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote ノートブック階層から階層オブジェクト (セクション グループ、セクション、またはページ) を削除します。  <br/> |
|**構文** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**パラメーター** <br/> | _bstrObjectID_ &ndash; 削除するオブジェクトの OneNote ID。 このオブジェクトは、セクション グループ、セクション、またはページです。  <br/><br/>_dateExpectedLastModified_ &ndash; (省略可能) 削除するオブジェクトの最終更新日時と見なす日付と時刻。 このパラメーターに 0 以外の値を渡すと、OneNote は、渡された値とオブジェクトの実際の最終更新日時が一致する場合にのみ更新操作を続行します。 このパラメーターで値を渡すと、オブジェクトの最終更新時以降にユーザーが編集した内容の意図しない上書きを防止できます。  <br/><br/>_deletePermanently_ &ndash; (省略可能) コンテンツを完全に削除する場合は **true**。コンテンツを対応するノートブックの OneNote ごみ箱に移動する場合は **false** (既定)。 ノートブックが OneNote 2007 形式の場合は、ごみ箱が存在しないため、コンテンツは完全に削除されます。  <br/> |
   
### <a name="createnewpage-method"></a>CreateNewPage メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したセクションに新しいページを追加します。 新しいページは、セクションの最後のページとして追加されます。  <br/> |
|**構文** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**パラメーター** <br/> | _bstrSectionID_ &ndash; 新しいページの作成先セクションの OneNote ID を格納する文字列。  <br/><br/>_pbstrPageID_ &ndash; (出力パラメーター) 文字列へのポインター。このメソッドは、その文字列に新しく作成したページの OneNote ID を書き込みます。  <br/><br/>_npsNewPageStyle_ &ndash; **NewPageStyle** 列挙型の値。この値で、作成するページのスタイルを指定します。  <br/> |
   
OneNote API の **CreateNewPage** メソッドは、利便性を目的として含まれています。 **UpdateHierarchy** メソッドを呼び出すことで、同じ結果が得られます。この場合は、新しいページの階層内での配置方法を細かく制御できます。 また、**UpdateHierarchy** メソッドを使用すると、新しいページの作成と同時にサブページも作成できます。 
  
### <a name="closenotebook-method"></a>CloseNotebook メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したノートブックを閉じます。  <br/> |
|**構文** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**パラメーター** <br/> | _bstrNotebookID_ &ndash; 閉じるノートブックの OneNote ID。  <br/><br/>_force_ &ndash; (省略可能) ノートブックを閉じる前に OneNote では同期できない変更があったとしてもノートブックを閉じる場合は **true**。それ以外の場合は **false** (既定)。  <br/> |
   
**CloseNotebook** メソッドを使用すると、指定したノートブックを閉じることができます。 このメソッドを呼び出すと、OneNote はオフラインのファイルを現在のノートブック コンテンツと同期します (同期が必要な場合)。その後で、指定のノートブックを閉じます。 このメソッドから復帰すると、そのノートブックは OneNote ユーザー インターフェイス (UI) の開いているノートブックのリストに表示されなくなります。 
  
### <a name="gethierarchyparent-method"></a>GetHierarchyParent メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote オブジェクトの親オブジェクトの OneNote ID を取得します。  <br/> |
|**構文** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**パラメーター** <br/> | _bstrObjectID_ &ndash; オブジェクトの OneNote ID を格納する文字列。このオブジェクトの親オブジェクトを見つけます。  <br/><br/>_pbstrParentID_ &ndash; (出力パラメーター) 文字列へのポインター。このメソッドは、その文字列に親オブジェクトの OneNote ID を書き込みます。  <br/> |
   
親オブジェクトが存在しない OneNote オブジェクトの場合 (ユーザーがノートブックの親オブジェクトを取得しようとした場合など)、例外がスローされます。
  
### <a name="getspeciallocation-method"></a>GetSpecialLocation メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote の特定の特別なアイテム (バックアップ、落書きノート、既定のノートブックなど) の保存場所へのパスを見つけます。  <br/> |
|**構文** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**パラメーター** <br/> | _slToGet_ &ndash; [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) 列挙型の値。この値で、取得する特別なフォルダーの場所を指定します。  <br/><br/>_pbstrSpecialLocationPath_ &ndash; (出力パラメーター) 文字列へのポインター。OneNote は、その文字列に特別なフォルダーのパスを書き込みます。  <br/> |
   
このメソッドを使用すると、[落書きノート] フォルダーのディスク上の場所がわかります。 OneNote は、OneNote にアイテムをドラッグして作成したノートや、別のアプリケーションから取り込んだノート (Microsoft Outlook や Microsoft Internet Explorer の **[OneNote に送る]** をクリックした結果としてのノートなど) を、このフォルダーに保存します。 
  
## <a name="page-content-methods"></a>ページ コンテンツのメソッド
<a name="ON14DevRef_Application_PageContent"> </a>

このセクションで説明するメソッドを使用すると、OneNote ノートブックのページにあるコンテンツを探索、更新、および削除できます。また、OneNote コンテンツを発行することもできます。
  
### <a name="getpagecontent-method"></a>GetPageContent メソッド

|||
|:-----|:-----|
|**説明**|指定したページのすべてのコンテンツを取得します (OneNote XML 形式で取得)。|
|**構文**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**パラメーター**| _bstrPageId_ &ndash; 取得するコンテンツが含まれているページの OneNote ID。<br/><br/>_pbstrPageXmlOut_ &ndash; (出力パラメーター) 文字列へのポインター。OneNote は、その文字列に XML 出力を書き込みます。<br/><br/>_pageInfoToExport_ &ndash; (省略可能) **GetPageContent** メソッドが、XML コードに埋め込まれた base-64 エンコードのバイナリ コンテンツを返すかどうかを指定します。 バイナリ コンテンツには、イメージやインクなどのデータを含めることができます。 また、_pageInfoToExport_ パラメーターでは、**GetPageContent** メソッドから返される XML コード内で選択部分をマーク アップするかどうかも指定します。 [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo) 列挙型の列挙値を指定します。<br/><br/>_xsSchema_ &ndash; (省略可能) 出力する OneNote XML スキーマのバージョン (**XMLSchema** 型)。 XML スキーマのバージョンは、2013、2010、2007、または現行のバージョンを指定できます。 <br/><br/>**注**: OneNote の将来のバージョンでもアドインが動作するように、**xsCurrent** を使用したり、空白のままにしたりするのではなく、OneNote のバージョン (**xs2013**) を指定するようにしてください。           |
   
既定では、過度に長い XML 文字列を返さないようにするために、OneNote は XML コードにバイナリ コンテンツを埋め込みません。 同じ理由から、現在の選択部分を選択属性でマーク アップすることもありません。 バイナリ オブジェクトは、そのオブジェクトのタグに OneNote ID が含まれています。 バイナリ オブジェクトを取得するには、**GetBinaryPageContent** メソッドを呼び出して、**GetPageContent** メソッドから取得した OneNote ID を渡します。 **GetPageContent** メソッドは、その時点でバイナリ データが不要なときに使用します。 
  
### <a name="updatepagecontent-method"></a>UpdatePageContent メソッド

|||
|:-----|:-----|
|**説明**|ページのコンテンツを更新または変更します。|
|**構文**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**パラメーター**| _bstrPageChangesXmlIn_ &ndash; OneNote XML コードを格納する文字列。ページに対する変更内容は、このコードに含めます。<br/><br/>_dateExpectedLastModified_ &ndash; (省略可能) 更新するページの最終更新日時と見なす日付と時刻。 このパラメーターに 0 以外の値を渡すと、OneNote は、渡された値とページの実際の最終更新日時が一致する場合にのみ更新操作を続行します。 このパラメーターで値を渡すと、ページの最終更新時以降にユーザーが編集した内容の意図しない上書きを防止できます。<br/><br/>_xsSchema_ &ndash; (省略可能) 出力する OneNote XML スキーマのバージョン (**XMLSchema** 型)。 XML スキーマのバージョンは、2013、2010、2007、または現行バージョンを指定できます。 <br/><br/>**注**: OneNote の将来のバージョンでもアドインが動作するように、**xsCurrent** を使用したり、空白のままにしたりするのではなく、OneNote のバージョン (**xs2013**) を指定するようにしてください。<br/><br/>_force_ - (省略可能) OneNote の将来のバージョンからページに不明なデータが存在していてもページ コンテンツを更新する場合は **true**。それ以外の場合は **false** (既定)。 |
   
このメソッドを使用すると、さまざまな方法でページを変更できます。 たとえば、**UpdatePageContent** メソッドは、ページへのアウトアインの追加、アウトラインのコンテンツの変更、イメージの追加、インクの追加、コンテンツの移動、アウトラインのテキストの変更などに使用できます。 
  
具体的な例としては、**GetPageContent** メソッドを使用して既存のページをエクスポートし、ページの XML コードに変更を加えてから、**UpdatePageContent** メソッドを使用してページ全体を再度インポートします。 また、このメソッドを使用して、新しいページ オブジェクト (イメージなど) を既存のページの下部に追加することもできます。 
  
**UpdatePageContent** メソッドに渡す XML コードには、変更したページ レベルのオブジェクト (アウトライン、ページ上のイメージ、ページ上のインクなど) のみを含める必要があります。 このメソッドは、_bstrPageChangesXmlIn_ パラメーターで指定していないページ レベルのオブジェクトを変更または削除することはありません。 このメソッドは、渡されたオブジェクトの ID と一致する ID を持つページ レベルのオブジェクト (アウトラインなど) を完全に置き換えます。 そのため、コードでは、既存のコンテンツとそのコンテンツに加える変更内容を含めて、すべてのページ レベルのオブジェクトを完全に指定する必要があります。 
  
たとえば、ページにアウトラインと背景ページ イメージが含まれている場合は、XML コードで既存のアウトラインの ID を使用してアウトラインを完全に指定して、そのコードにイメージを含めないようにすることで、イメージを変更することなく、アウトラインを置き換えることができます。 既存のアウトラインはコードに含まれる改訂したアウトラインで完全に置き換えられるため、そのアウトラインのすべてのコンテンツを含める必要があります。
  
さらに、**UpdatePageContent** メソッドは、_bstrPageChangesXmlIn_ パラメーターで指定した要素のプロパティのみを変更します。 たとえば、**PageSettings** 要素のすべてのプロパティではなく、一部のプロパティを指定すると、指定していないプロパティは変更されません。 
  
次の例は、**UpdatePageContent** メソッドを使用して、ページのタイトルを変更し、そのページにいくつかのサンプル テキストを追加する方法を示しています。 このコードの実行前に、自分のコンピューターでコードが動作するように、コード内に示したページ ID を有効なページ ID に置換してください。 ページのページ ID は、**GetHierarchy** メソッドを使用して出力を調べることでわかります。 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"https://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
            ID=\"{3428B7BB-EF39-4B9C-A167-3FAE20630C37}{1}{B0}\">" +
            "    <one:PageSettings RTL=\"false\" color=\"automatic\">" +
            "        <one:PageSize>" +
            "            <one:Automatic/>" +
            "        </one:PageSize>" +
            "        <one:RuleLines visible=\"false\"/>" +
            "    </one:PageSettings>" +
            "    <one:Title style=\"font-family:Calibri;
                 font-size:17.0pt\" lang=\"en-US\">" +
            "        <one:OE alignment=\"left\">" +
            "            <one:T>" +
            "                <![CDATA[My Sample Page]]>" +
            "            </one:T>" +
            "        </one:OE>" +
            "    </one:Title>" +
            "    <one:Outline >" +
            "        <one:Position x=\"120\" y=\"160\"/>" +
            "        <one:Size width=\"120\" height=\"15\"/>" +
            "        <one:OEChildren>" +
            "            <one:OE alignment=\"left\">" +
            "                <one:T>" +
            "                    <![CDATA[Sample Text]]>" +
            "                </one:T>" +
            "            </one:OE>" +
            "        </one:OEChildren>" +
            "    </one:Outline>" +
            "</one:Page>";
        // Update the page content.
        onApplication.UpdatePageContent(strImportXML, System.DateTime.MinValue);
    }

```

### <a name="getbinarypagecontent-method"></a>GetBinaryPageContent メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote ページ上のバイナリ オブジェクト (インクやイメージなど) を base-64 エンコード文字列として返します。  <br/> |
|**構文** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**パラメーター** <br/> | _bstrPageID_ &ndash; 取得するバイナリ オブジェクトが含まれているページの OneNote ID。  <br/><br/>_bstrCallBackID_ &ndash; 取得するバイナリ オブジェクトの OneNote ID。 この ID (**callbackID**) は、**GetPageContent** メソッドで返されるページの OneNote XML コードに含まれています。  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; (出力パラメーター) 文字列へのポインター。OneNote は、その文字列に base-64 エンコード文字列としてバイナリ オブジェクトを書き込みます。  <br/> |
   
### <a name="deletepagecontent-method"></a>DeletePageContent メソッド

|||
|:-----|:-----|
|**説明** <br/> |ページから **Outline**、**Ink**、**Image** などのオブジェクトを削除します。  <br/> |
|**構文** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**パラメーター** <br/> | _bstrPageID_ &ndash; 削除するオブジェクトが含まれているページの OneNote ID。  <br/><br/>_bstrObjectID_ &ndash; 削除するオブジェクトの OneNote ID。  <br/><br/>_dateExpectedLastModified_ &ndash; (省略可能) 削除するコンテンツの最終更新日時と見なす日付と時刻。 このパラメーターに 0 以外の値を渡すと、OneNote は、渡された値とページの実際の最終更新日時が一致する場合にのみ削除操作を続行します。 このパラメーターで値を渡すと、ページの最終更新時以降にユーザーが編集した内容の意図しない上書きを防止できます。  <br/><br/>_force_ &ndash; (省略可能) OneNote の将来のバージョンからページに不明なデータが存在していてもページ コンテンツを更新する場合は **true**。それ以外の場合は **false** (既定)。  <br/> |
   
### <a name="publish-method"></a>Publish メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したページを OneNote がサポートしている形式でファイルにエクスポートします。  <br/> |
|**構文** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_ &ndash; エクスポートする階層の OneNote ID。  <br/><br/>_bstrTargetFilePath_ &ndash; 結果の出力ファイルを保存する場所への絶対パス。 指定したファイルは、その場所に存在していないことが必要です。  <br/><br/>_pfPublishFormat_ &ndash; [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) 列挙型の値。この値で、発行するページの形式 (MTHML や PDF など) を指定します。  <br/><br/>_bstrCLSIDofExporter_ &ndash; Microsoft Windows 拡張メタファイル (.emf) をエクスポートできる登録済み COM アプリケーションのクラス ID (CLSID)。 この COM アプリケーションは、**IMsoDocExporter** インターフェイスを実装している必要があります。 このパラメーターは、サード パーティの開発者がカスタム形式で OneNote コンテンツを発行する独自のコードを作成できるようにするために含まれています。 **IMsoDocExporter** インターフェイスの詳細については、「[Office (2007) 固定形式エクスポート機能の拡張](https://msdn.microsoft.com/library/office/aa338206%28v=office.12%29.aspx)」を参照してください。  <br/> |
   
現在、OneNote では次のファイル形式をサポートしています。
  
- MHTML ファイル (.mht)
- Adobe Acrobat PDF ファイル (.pdf)
- XML Paper Specification (XPS) ファイル (.xps)
- OneNote 2013、2010 または 2007 ファイル (.one)
- OneNote パッケージ ファイル (.onepkg)
- Microsoft Word 文書 (.doc or .docx)
- Microsoft Windows 拡張メタファイル (.emf)
- HTML ファイル (.html)
    
このメソッドは、UI の **[発行]** をクリックして形式を指定した場合と、まったく同じ結果を生成します。 
  
## <a name="navigation-methods"></a>ナビゲーションのメソッド
<a name="ON14DevRef_Application_Navigation"> </a>

このセクションで説明するメソッドを使用すると、OneNote ノートブック、セクション グループ、セクション、ページ、およびページ オブジェクトへのナビゲーション、リンク、および検索が可能になります。
  
### <a name="navigateto-method"></a>NavigateTo メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したオブジェクト (セクション、ページ、ページ内の **Outline** 要素など) にナビゲートします。  <br/> |
|**構文** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyObjectID_ &ndash; OneNote 階層内のナビゲート先オブジェクトの OneNote ID。  <br/><br/>_bstrObjectID_ &ndash; OneNote ページ上のナビゲート先オブジェクトの OneNote ID。  <br/><br/>_fNewWindow_ &ndash; (省略可能) 指定したオブジェクトを新しい OneNote ウィンドウで開く場合は **true**。 OneNote ウィンドウが開いているときには新しいウィンドウを開かない場合は **false**。  <br/> |
   
### <a name="navigatetourl-method"></a>NavigateToUrl メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote のリンクを渡された場合 (onenote://)、OneNote 内の対応する場所には、OneNote ウィンドウが開きます。 リンクが OneNote の外部へのリンク (https:// や file:// など) の場合は、セキュリティ ダイアログ ボックスが表示されます。 無視すると、OneNote はリンクを開こうとして、**HResult.hrObjectDoesNotExist** エラーが返されます。  <br/> |
|**構文** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**パラメーター** <br/> | _bstrUrl_ &ndash; ナビゲート先を示す文字列。 これは、OneNote のリンクにすることも、それ以外の任意の URL (Web リンクやネットワークの場所など) にすることもできます。  <br/><br/>_fNewWindow_ &ndash; (省略可能) 指定の URL を新しい OneNote ウィンドウで開く場合は **true**。 OneNote ウィンドウが開いているときには新しいウィンドウを開かない場合は **false**。  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>GetHyperLinkToObject メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定のノートブック、セクション グループ、セクション、ページ、またはページ オブジェクトへの OneNote ハイパーリンクを取得します。  <br/> |
|**構文** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_ &ndash; ハイパーリンクの取得対象のノートブック、セクション グループ、またはページの OneNote ID。  <br/><br/>_bstrPageContentObjectID_ &ndash; (省略可能) ハイパーリンクの取得対象のページ内にあるオブジェクトの OneNote ID。 たとえば、このオブジェクトはアウトラインであることも、**Outline** 要素であることもあります。 空の文字列 ("") を渡すと、_bstrHierarchyID_ パラメーターで指定したノートブック、セクション グループ、セクション、またはページをポイントするリンクが返されます。 _bstrPageContentObjectID_ パラメーターで空白でない文字列を渡す場合、_bstrHierarchyID_ パラメーターは指定したオブジェクトが含まれているページへの参照であることが必要です。  <br/><br/>_pbstrHyperlinkOut_ &ndash; (出力パラメーター) 文字列へのポインター。**GetHyperlinkToObject** メソッドは、その文字列に出力のハイパーリンク テキストを書き込みます。  <br/> |
   
結果のリンク先にナビゲートしようとすると、OneNote は指定のオブジェクトをブラウザーで開いて表示します。
  
### <a name="getwebhyperlinktoobject-method"></a>GetWebHyperlinktoObject メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote Web クライアントで開いたオブジェクトへのハイパーリンクを返します。  <br/> |
|**構文** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_ &ndash; Web ハイパーリンクの取得対象のノートブック、セクション グループ、セクションまたはページの OneNote ID。  <br/><br/>_bstrPageContentObjectID_ &ndash; (省略可能) ハイパーリンクの取得対象のページ内にあるオブジェクトの OneNote ID。 たとえば、このオブジェクトはアウトラインであることも、**Outline** 要素であることもあります。 空の文字列 ("") を渡すと、_bstrHierarchyID_ パラメーターで指定したノートブック、セクション グループ、セクション、またはページをポイントするリンクが返されます。 _bstrPageContentObjectID_ パラメーターで空白でない文字列を渡す場合、_bstrHierarchyID_ パラメーターは指定したオブジェクトが含まれているページへの参照であることが必要です。  <br/><br/>_pbstrHyperlinkOut_ &ndash; (出力パラメーター) 文字列へのポインター。**GetWebHyperlinkToObject** メソッドは、その文字列に出力のハイパーリンク テキストを書き込みます。 ノートブックに対する Web ハイパーリンクが作成できない場合は、Null 値が返されます。  <br/> |
   
### <a name="findpages-method"></a>FindPages メソッド

|||
|:-----|:-----|
|**説明**|指定したクエリ条件と一致するページのリストを返します。|
|**構文**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**パラメーター**| _bstrStartNodeID_ &ndash; コンテンツの検索対象にする最上位のノード (ルート、ノートブック、セクション グループ、セクション)。 このパラメーターによって、検索の範囲を設定します。<br/><br/>_bstrSearchString_ &ndash; 検索文字列。 OneNote UI の検索ボックスに入力する場合とまったく同じ文字列を渡します。 ビットごとの演算子 (**AND** や **OR** など) を使用できます。この演算子は、大文字表記にする必要があります。<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (出力パラメーター) 文字列へのポインター。OneNote は、その文字列に出力 XML 文字列を書き込みます。 結果の XML 文字列には、ルートから下位方向に検索文字列と一致するページまでのノートブック階層が格納されています。 たとえば、**FindPages** メソッドは、階層内で一致するページが存在しないセクションはリスト出力しません。 さらに、1 つのセクションの 1 つのページのみが文字列と一致する場合に返される階層には、そのセクションとページへのパスが含まれますが、それ以外のノートブック階層の部分へのパスは含まれません。<br/><br/>_fIncludeUnindexedPages_ &ndash; (省略可能) Windows Search でインデックスが作成されていないページを検索する場合は **true**。それ以外の場合は **false**。<br/><br/>_fDisplay_ &ndash; (省略可能) ユーザーが入力した場合と同じように UI でも検索を実行する場合は **true**。 UI の変化なしにクエリを実行する場合は **false** (既定)。<br/><br/>_xsSchema_ &ndash; (省略可能) 文字列 _pbstrHierarchyXmlOut_ の OneNote スキーマ バージョン。 この省略可能な値は、_pbstrHierarchyXmlOut_ 文字列を格納する OneNote XML スキーマのバージョンを指定するために使用します。 この値が指定されてないと、OneNote は XML のスキーマ バージョンが _xsCurrent_ であると仮定します。 <br/><br/>**注**: OneNote の将来のバージョンでもアドインが動作するように、**xsCurrent** を使用したり、空白のままにしたりするのではなく、OneNote のバージョン (**xs2013**) を指定するようにしてください。           |
   
 **FindPages** は、コンピューターに Microsoft Search 3.0 または 4.0 がインストールされている場合にのみ動作します。 Windows Vista および Windows 7 には、このコンポーネントが組み込まれています。 ただし、それより前のバージョンの Windows を実行している場合は、**FindPages** が動作するように、[Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) をインストールする必要があります。 
  
### <a name="findmeta-method"></a>FindMeta メソッド

|||
|:-----|:-----|
|**説明**|指定したクエリ条件と一致するメタデータを含んでいる OneNote オブジェクトのリストを返します。|
|**構文**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**パラメーター**| _bstrStartNodeID_ &ndash; コンテンツの検索対象にする最上位のノード (ルート、ノートブック、セクション グループ、セクション)。 このパラメーターによって、検索の範囲を設定します。<br/><br/>_bstrSearchStringName_ &ndash; 検索文字列。 メタデータ名の任意の部分を渡します。 空の文字列または Null 値を渡すと、メタデータが存在するすべてのオブジェクトがクエリと一致します。<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (出力パラメーター) 文字列へのポインター。OneNote は、その文字列に出力 XML 文字列を書き込みます。 結果の XML 文字列には、ルートから下位方向に検索文字列と一致するページまでのノートブック階層が格納されています。 たとえば、**FindPages** メソッドは、階層内で一致するページが存在しないセクションはリスト出力しません。 さらに、1 つのセクションの 1 つのページのみが文字列と一致する場合に返される階層には、そのセクションとページへのパスが含まれますが、それ以外のノートブック階層の部分へのパスは含まれません。  <br/><br/>_fIncludeUnindexedPages_ &ndash; (省略可能) Windows Search でインデックスが作成されていないページを検索する場合は **true**。それ以外の場合は **false**。<br/><br/>_xsSchema_ &ndash; (省略可能) 文字列 _pbstrHierarchyXmlOut_ の OneNote スキーマ バージョン。 この省略可能な値は、_pbstrHierarchyXmlOut_ 文字列を格納する OneNote XML スキーマのバージョンを指定するために使用します。 この値が指定されてないと、OneNote は XML のスキーマ バージョンが _xsCurrent_ であると仮定します。 <br/><br/>**注**: OneNote の将来のバージョンでもアドインが動作するように、**xsCurrent** を使用したり、空白のままにしたりするのではなく、OneNote のバージョン (**xs2013**) を指定するようにしてください。           |
   
**FindMeta** は、コンピューターに Microsoft Windows Search 3.0 または 4.0 がインストールされている場合にのみ動作します。 Windows Vista および Windows 7 には、このコンポーネントが組み込まれています。 ただし、それより前のバージョンの Windows を実行している場合は、**FindMeta** が動作するように、[Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) をインストールする必要があります。 
  
## <a name="functional-methods"></a>機能性のメソッド
<a name="ON14DevRef_Application_Functional"> </a>

このセクションで説明するメソッドを使用すると、OneNote アプリケーションで特定のアクションを実行することやパラメーターを設定することができます。
  
### <a name="mergefiles-method"></a>MergeFiles メソッド

|||
|:-----|:-----|
|**説明** <br/> |ユーザーが同じファイルの変更内容を 1 つに結合できるようにします。 複数のファイルが同一であると見なされるには、それらの OneNote ID が同じであることが必要です。  <br/> |
|**構文** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**パラメーター** <br/> | _bstrBaseFile_ &ndash; 初期状態のファイルの .one ファイルの場所へのパス文字列。  <br/><br/>_bstrClientFile_ &ndash; サーバー ファイルの変更がベースと結合された後でベース ファイルと結合される 2 番目の変更セットを含む .one ファイルの場所へのパス文字列。  <br/><br/>_bstrServerFile_ &ndash; ベース ファイルと結合される最初の変更セットを含む .one ファイルの場所へのパス文字列。  <br/><br/>_bstrTargetFile_ &ndash; 変更が結合されたファイルの .one ファイルの場所へのパス文字列。  <br/> |
   
**MergeFiles** メソッドは、複数バージョンの OneNote ファイルが存在する可能性のあるモバイル シナリオに向けられたものです。 
  
### <a name="mergesections-method"></a>MergeSections メソッド

|||
|:-----|:-----|
|**説明** <br/> |セクションのコンテンツを OneNote の別のセクションに結合します。  <br/> |
|**構文** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**パラメーター** <br/> | _bstrSectionSourceId_ &ndash; 結合されるセクションの OneNote ID。  <br/><br/>_bstrSectionDestinationId_ &ndash; 結合先のセクションの OneNote ID。 結合元のセクションが、この結合先セクションに結合されます。  <br/> |
   
このメソッドは、セクションを右クリックしたときに表示される **[別のセクションに結合]** 機能と同じ操作を実行します。 
  
### <a name="quickfiling-method"></a>QuickFiling メソッド

|||
|:-----|:-----|
|**説明** <br/> |[IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog) ダイアログ ボックスのインスタンスを返します。このダイアログ ボックスは、OneNote 階層ツリーの場所を選択する際に使用できます。  <br/> |
|**構文** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>SyncHierarchy メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したオブジェクトとディスク上のソース ファイルを OneNote で強制的に同期します。  <br/> |
|**構文** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_ &ndash; 同期対象オブジェクトの OneNote ID。  <br/> |
   
### <a name="setfilinglocation-method"></a>SetFilingLocation メソッド

|||
|:-----|:-----|
|**説明** <br/> |ユーザーが OneNote で特定の種類のコンテンツを分類整理する場所と方法を指定できるようにします。  <br/> |
|**構文** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**パラメーター** <br/> | _flToSet_ &ndash; 設定する分類整理の場所のオブジェクトの種類。  <br/><br/>_fltToSet_ &ndash; その種類を分類整理する場所。  <br/><br/>_bstrFilingSectionID_ &ndash; 設定する場所のセクションまたはページの OneNote ID。 該当しない場合、ユーザーは Null または空の文字列を渡すことができます。  <br/> |
   
分類整理できるコンテンツの種類には、Outlook アイテムおよび Internet Explorer からの Web ノートが含まれます。これらは、それぞれのアプリケーションの **[OneNote に送る]** コマンドで OneNote にインポートします。 OneNote に出力するアイテムをファイリングする場所は、このメソッドで設定することもできます。 
  
## <a name="properties"></a>プロパティ
<a name="ON14DevRef_Application_Properties"> </a>

このセクションでは、**Application** インターフェイスのプロパティについて説明します。 
  
|**Property**|**説明**|
|:-----|:-----|
|**Windows** <br/> |開いている OneNote ウィンドウにユーザーがアクセスできるようにします。 このプロパティによって、ユーザーが OneNote ウィンドウのセットを列挙して、特定のウィンドウのプロパティを変更できるようになります。 詳細については、「[Windows インターフェイス](window-interfaces-onenote.md)」を参照してください。  <br/> |
|**COMAddIns** <br/> |OneNote の **COMAddIns** コレクションを返します。 このコレクションには、OneNote で使用可能なすべての COM アドインが含まれています。 **COMAddins** コレクションの **Count** プロパティは、使用可能な COM アドインの数を返します。詳細については、「[COMAddIns](https://msdn.microsoft.com/library/office/ff865489.aspx) オブジェクト」を参照してください。  <br/> |
|**LanguageSettings** <br/> |OneNote の共通言語の設定を変更する一部の API にアクセスできます。  <br/> |
   
## <a name="events"></a>イベント
<a name="ON14DevRef_Application_Events"> </a>

このセクションでは、Application インターフェイスのイベントについて説明します。
  
> [!CAUTION]
> 現時点では、マネージ コードにイベントを追加することはできません。 
  
### <a name="onnavigate-event"></a>OnNavigate イベント

|||
|:-----|:-----|
|**説明** <br/> |現在の OneNote の場所から別の場所に OneNote UI がナビゲートされたときに呼び出す関数をユーザーが割り当てできます。  <br/> |
|**構文** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>OnHierarchyChange メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote 階層が変更されたとき (ページの追加時または削除時、セクションの移動時など) に必ず呼び出される関数をユーザーが割り当てできます。 階層の変更は一括処理されるため、複数の変更が同時またはほぼ同時に発生すると、OneNote はこのイベントを 1 回発せさせます。  <br/> |
|**構文** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**パラメーター** <br/> | _bstrActivePageID_ &ndash; アクティブなページの OneNote ID を渡します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [OneNote 開発者用リファレンス](onenote-developer-reference.md)

