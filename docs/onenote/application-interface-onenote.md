---
title: アプリケーション ・ インタ フェース (OneNote の場合)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: アプリケーションのインターフェイスには、メソッドのヘルプの取得が含まれています、操作、および OneNote の情報とコンテンツを更新します。 メソッドは、次の 4 つの一般的なカテゴリには。
ms.openlocfilehash: 25bb1aa570f6c36aa04140d9256d277bee65152b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799278"
---
# <a name="application-interface-onenote"></a>アプリケーション ・ インタ フェース (OneNote の場合)

**アプリケーション**のインターフェイスには、メソッドのヘルプの取得が含まれています、操作、および OneNote の情報とコンテンツを更新します。 メソッドは、次の 4 つの一般的なカテゴリには。 
  
- **ノートブックの構造**&ndash;を検出する、および開くのため、変更、終了するには、ノートブック、セクション グループとセクションを削除するものも含めて、ノートブックの構造を操作するためのメソッドです。 
    
- **ページのコンテンツ**&ndash;ページとページのコンテンツなどを検出する、変更、保存、およびページのコンテンツを削除するためのメソッドです。 ページのコンテンツには、インクやイメージなどのバイナリ オブジェクト、およびアウトラインなどのテキスト オブジェクトが含まれています。 
    
- **ナビゲーション**&ndash;の検索、リンク、およびページやオブジェクトに移動するためのメソッドです。 
    
- **機能**&ndash;の特定のアクションを実行または OneNote のパラメーターを設定する他のすべての方法です。 
    
さらに、**アプリケーション**のインターフェイスには、多数*プロパティ*と*イベント*にはが含まれています。 
  
## <a name="notebook-structure-methods"></a>ノートブックの構造体のメソッド
<a name="ON14DevRef_Application_NotebookStructure"> </a>

このセクションで説明する方法を使用すると、検出、開く、変更、閉じると、OneNote のノートブック、セクション グループとセクションを削除します。
  
### <a name="gethierarchy-method"></a>GetHierarchy メソッド

|||
|:-----|:-----|
|**説明** <br/> |ノートブックのノードの階層構造体を取得、指定したノードから開始 (すべてのノートブックまたは 1 つのノートブック、セクション グループ、またはセクション)、および指定したレベルでのすべての子孫に下方向に拡張します。  <br/> |
|**構文** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**パラメーター** <br/> | _bstrStartNodeID_&ndash; (ノートブック、セクション グループ、またはセクション) 目的の子ノードです。 Null 文字列を渡す場合 ("")、メソッドは、ルート ノード (つまり、すべてのノートブック、セクション グループ、およびセクション) の下のすべてのノードを取得します。 ノートブック、セクション グループ、またはセクションのノードを指定する場合、メソッドは、そのノードの子孫のみを取得します。  <br/><br/>_hsScope_&ndash;最下位の子孫ノードのレベルです。 などのページを指定する場合、メソッドは、取得のすべてのノードまでページ レベルとして。 セクションを指定すると、メソッドは、ノートブックの下のセクション ノードのみを取得します。 詳細については、 **HierarchyScope**列挙体[の列挙体](enumerations-onenote-developer-reference.md#odc_HierarchyScope)のトピックを参照してください。  <br/><br/>_pbstrHierarchyXmlOut_&ndash; (出力パラメーター) A のポインターへの XML 出力を記述する文字列にします。  <br/><br/>_xsSchema_&ndash; (オプション) の **「xml スキーマ」** では、種類の、OneNote の XML スキーマ バージョンを出力することです。 2007 年は、2013 年 2010 年のバージョンの XML スキーマがかどうかを指定するか、現在のバージョンです。  <br/><br/>**注**: お勧め ( **xs2013**) などには、OneNote のバージョンを指定する**xsCurrent**を使用するか、オフのままにするのではなく、アドインを将来のバージョンの OneNote を使用することができます。           |
   
GetHierarchy メソッドは、既定またはする OneNote 2013 の XML 形式の文字列は、オプションの_xsSchema_パラメーターを使用して推奨される XML スキーマのバージョンを設定できますを返します。 
  
**GetHierarchy**メソッドは、渡されたパラメーターによって (すべてのノートブック、ノートブックのすべて、指定されたセクション内のすべてのページまたは特定のノートブック内のすべてのページのすべてのセクションなど) のさまざまなリストを返すことができます。 返される XML 文字列は、各ノードのプロパティ (たとえばのセクションまたはページのタイトル、ID、および最終変更時刻) を提供します。 
  
開始ノードとスコープのすべての組み合わせが有効です。 たとえば、セクションの開始ノードとノートブックの範囲を指定する場合**GetHierarchy**結果を返します null ノートブックのセクションよりも上位のノード階層があるため。 
  
**GetHierarchy**メソッドを使用して、ページ レベルに至るまで、すべてのノートブックを含む、OneNote の階層全体を取得する方法を次の C# の例に示します。 確認のためのテキスト エディターに、文字列を貼り付けることができます、クリップボードに出力する文字列をコピーします。 
  
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
|**説明**|変更またはノートブックの階層を更新します。 ノートブック内のセクションを移動するセクションまたはノートブック、セクション グループの追加、新しいノートブックを追加することができます、セクションの名前を変更、ページをセクションに追加など、セクション内のページの順序を変更します。|
|**構文**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**パラメーター**| _bstrChangesXmlIn_&ndash;を作成する階層の変更内容を指定する OneNote の XML コードを含む文字列です。 たとえば、新しいセクションを挿入する場合は、新しいセクションを追加する場所を指定する XML 文字列の**セクション**要素を追加できます。 または、既存のセクションの名前を変更する場合は、同じセクションの ID を保持し、XML コードでは、その**name**属性を変更できます。<br/><br/>_xsSchema_&ndash;文字列_bstrChangesXmln_の [OneNote の (オプション) スキーマのバージョン。 このオプションの値を使用して、 _bstrChangesXmlIn_の文字列が、OneNote の XML スキーマのバージョンを指定します。 この値を指定しない場合は、OneNote が XML スキーマのバージョン_xsCurrent_であると仮定します。 <br/><br/>**注**: お勧め ( **xs2013**) などには、OneNote のバージョンを指定する**xsCurrent**を使用するか、オフのままにするのではなく、アドインを将来のバージョンの OneNote を使用することができます。           |
   
_BstrChangesXmlIn_パラメーターにのみ部分的な OneNote の XML 文字列を渡すと、OneNote は必要な変更を推論しようとします。 などの場合は 1 つだけのセクションが含まれている**ノートブック**の要素を含めると、OneNote は、既存のセクションの後セクションを追加します。 ただし、指定した操作があいまいな場合は、結果は判断が困難のようにできます。 たとえば、既存のノートブックには、4 つのセクションが含まれている場合は、指定した XML 文字列には、ノートブックとその順序で 4 番目と最初のセクションのみが含まれています。 OneNote を配置 2 番目と 3 番目のセクションで最初のセクションの前後には、4 番目のセクション. 
  
ノートブックの一部を削除するのには、 **UpdateHierarchy**メソッドを使用することはできません。 既存の階層構造の一部だけを含む XML 文字列を渡すことも含まれていない文字列のセクションは削除されません。 階層の一部を削除するには、 **DeleteHierarchy**メソッドを使用します。 
  
次の C# コードは、既存のセクションの名前を変更することで、OneNote の階層を変更するのには、 **UpdateHierarchy**メソッドを使用する方法を示しています。 それを読み取り、C ドライブのルートに ChangeSectionName.xml をという名前のサンプル ファイルからの XML コードが XML ドキュメントに読み込まれ、そのドキュメントの XML 構造体をメソッドに渡します。 
  
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

次の XML コードは、上記の C# のコードがメソッドに渡される ChangeSectionName.xml ファイルの抜粋です。 XML が**UpdateHierarchy**メソッドに渡されると、(「自分の名前を変更」には、 **name**属性の値を変更する)、既存の階層内セクションのいずれかの名前を変更します。 名前が変更された 1 つを除くすべてのセクションを削除します。 ターゲット**セクション**要素、属性を含む、 **lastModifiedTime**、 **isCurrentlyViewed**、および**色**、**名前**、 **ID**、および**のみを残してから、コードが不要な属性を削除するさらに、パス**属性をそのまま使用します。 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="http://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

**GetHierarchy**メソッドは、変更されると、次のように、セクションには、スコープを制限するための例に示すようにコードを使用して、上記の XML コードが取得されました。 
  
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

次の C# の例は、名前付きセクションを検索する完全なコンソール アプリケーションを示しています" `Sample_Section`」、セクションの新しい名前を入力するように求めると、 **UpdateHierarchy**メソッドを使用して、セクション名を名前に変更するユーザー。型指定されます。 コードを実行する前に次のように変更します。" `Sample_Section`"、OneNote の階層内に存在するセクションの名前にします。
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "http://schemas.microsoft.com/office/onenote/2013/onenote";
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
|**説明** <br/> |セクション グループまたは指定したセクションが表示されます。  <br/> |
|**構文** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**パラメーター** <br/> | _bstrPath_&ndash;パスを開きます。 、ノートブックまたはノートブック内のセクション グループは、 _bstrPath_フォルダーのパスまたはできます、セクションの .one ファイルへのパス。 セクションの .one ファイルにパスを指定する場合は、ファイル ・ パス文字列の拡張子が .one を含める必要があります。  <br/><br/>_bstrRelativeToObjectID_&ndash;使用する新しいオブジェクトを開くには、親オブジェクト (ノートブックまたはセクション グループ) の [OneNote の ID です。 _BstrPath_パラメーターが絶対パスである場合は、空の文字列を渡すことができます ("") の_bstrRelativeToObjectID_です。 または、することができますオブジェクトの ID を渡しますノートブックまたはセクション グループを作成するオブジェクト (セクションまたはセクション グループ) が含まれているし、オブジェクトのファイル名 (section1.one など) を指定する必要があります、その下にあるを作成します。親オブジェクトです。  <br/><br/>_pbstrObjectID_&ndash; (出力パラメーター) を表すオブジェクト OneNote ノートブック、セクション グループ、または**OpenHierarchy**メソッドが表示されるセクションのオブジェクト ID。 このパラメーターは、ID を作成するメソッドを挿入する文字列へのポインター  <br/><br/>_cftlfNotExist_&ndash; [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType)列挙型の列挙値 (省略可能)。 _CftIfNotExist_の値を渡す場合、 **OpenHierarchy**メソッドを作成、セクション グループまたはセクション ファイル指定のパスにファイルが存在しない場合にのみ。  <br/> |
   
ノートブックを開くには、セクション グループを指定する場合、 **OpenHierarchy**メソッドはノートブックとセクション グループを開きます。 ノートブックを開くにはないセクションを指定する場合、 **OpenHierarchy**メソッドは、最近開かれたセクションのセクション グループにセクションを開きます。 セクション グループまたはノートブックを開くには既にのセクションを指定する場合は、セクション グループまたはセクションで既に開いているため、同様に何も起こりません。 どのような場合は、 **OpenHierarchy**は、他の操作で使用することができますように、セクション グループ、ノートブック、または、指定したセクションのオブジェクト ID を返します。 
  
XML をインポートすることによってこれを行うのではなく、新しいセクションを作成するのには、 **OpenHierarchy**メソッドを使用することもできます。 
  
仕事ノートブックで、[会議] セクションを開き、セクションの ID を取得する**OpenHierarchy**メソッドを使用する方法を次に示します。 セクションが既に存在しない場合が、指定した場所に作成されます。 
  
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
|**説明** <br/> |OneNote ノートブックの階層から階層オブジェクト (セクション グループ、セクション、またはページ) を削除します。  <br/> |
|**構文** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**パラメーター** <br/> | _bstrObjectID_&ndash;を削除するオブジェクトの [OneNote の ID です。 オブジェクトには、セクション グループ、セクション、またはページができます。  <br/><br/>_dateExpectedLastModified_&ndash; (省略可能) を削除するオブジェクトが最後と思われる日付と時刻を変更します。 このパラメーターに 0 以外の値を渡した場合、OneNote は、渡す値は、実際の日付と時刻オブジェクトが最後に修正されたと一致する場合にのみ更新を続行します。 このパラメーターにより、誤って上書きしないように、値を渡すオブジェクトが変更された最後の時間以降に行われたユーザーを編集します。  <br/><br/>_deletePermanently_&ndash; (オプション)**場合は true**コンテンツを完全に削除するのには**false** OneNote にコンテンツを移動するのには [ごみ箱に対応するノートブック (既定値)。 ノートブックは、OneNote 2007 形式では、ごみ箱が存在しない場合、コンテンツが完全に削除するようにします。  <br/> |
   
### <a name="createnewpage-method"></a>CreateNewPage メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定するセクションに新しいページを追加します。 セクションの最後のページに新規ページを追加します。  <br/> |
|**構文** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**パラメーター** <br/> | _bstrSectionID_&ndash;のセクションの新しいページを作成する OneNote の ID を含む文字列です。  <br/><br/>_pbstrPageID_&ndash;メソッドが新しく作成されたページを OneNote の ID を書き込む先の文字列 (出力パラメーター) A のポインター。  <br/><br/>_npsNewPageStyle_&ndash;を作成するページのスタイルを指定する**NewPageStyle**列挙からの値です。  <br/> |
   
OneNote の API には、利便性のための**CreateNewPage**メソッドが含まれています。 階層で、 **UpdateHierarchy**メソッドを呼び出して、新しいページを配置する方法をより細かく制御に、同じ結果を実現できます。 **UpdateHierarchy**メソッドを使用して、新しいページを作成すると同時にサブページを作成することもできます。 
  
### <a name="closenotebook-method"></a>CloseNotebook メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したノートブックを閉じます。  <br/> |
|**構文** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**パラメーター** <br/> | _bstrNotebookID_&ndash;を終了するノートブックの [OneNote の ID です。  <br/><br/>_強制的に_&ndash; (オプション) **true**を閉じる前に同期できませんのノートブックに変更が加えられた場合でも、ノートブックを閉じますそれ以外の場合、 **false** (既定値)。  <br/> |
   
指定したノートブックを閉じるには、 **CloseNotebook**メソッドを使用できます。 このメソッドを呼び出すと、OneNote は必要に応じて、現在のノートブックの内容をすべてのオフライン ファイルを同期し、後、指定したノートブックを閉じます。 メソッドから制御が戻った後、ノートブックは、OneNote のユーザー インターフェイス (UI) で開いているノートブックの一覧に表示されなくなります。 
  
### <a name="gethierarchyparent-method"></a>GetHierarchyParent メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote オブジェクトの親オブジェクトには、OneNote の ID を取得します。  <br/> |
|**構文** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**パラメーター** <br/> | _bstrObjectID_&ndash;オブジェクトの親オブジェクトを検索する先のオブジェクトの OneNote の ID を含む文字列です。  <br/><br/>_pbstrParentID_&ndash; (出力パラメーター) A のポインターには、メソッドは、OneNote の ID オブジェクトの親オブジェクトを書き込みます。 文字列にします。  <br/> |
   
OneNote オブジェクトには、親のオブジェクト (たとえば、ユーザーがノートブックの親を取得する場合など) がなければ、例外がスローされます。
  
### <a name="getspeciallocation-method"></a>GetSpecialLocation メソッド

|||
|:-----|:-----|
|**説明** <br/> |バックアップ、落書きノートは、既定のノートブックなど、特定の特別なアイテムの保存先の場所へのパスを検索します。  <br/> |
|**構文** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**パラメーター** <br/> | _slToGet_&ndash;を取得する特別なフォルダーの場所を指定する[SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation)列挙値のいずれかです。  <br/><br/>_pbstrSpecialLocationPath_&ndash; (出力パラメーター) A のポインターへの特別なフォルダーのパスを記述する文字列にします。  <br/> |
   
落書きノート フォルダーは、ディスク上の場所を決定するのにには、このメソッドを使用します。 ノートが OneNote にアイテムをドラッグするときに作成されると、ノートを他のアプリケーション (Microsoft Outlook または Microsoft **OneNote に送る**をクリックする場合に発生するものから直接 OneNote を格納するフォルダーです。Internet Explorer の場合)。 
  
## <a name="page-content-methods"></a>ページのコンテンツの方法
<a name="ON14DevRef_Application_PageContent"> </a>

このセクションで説明する方法を使用すると、検索、更新、および OneNote のノートブック内のページ上のコンテンツを削除すると、OneNote のコンテンツを発行することができます。
  
### <a name="getpagecontent-method"></a>GetPageContent メソッド

|||
|:-----|:-----|
|**説明**|OneNote の XML の形式で指定されたページのコンテンツのすべてを取得します。|
|**構文**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**パラメーター**| _bstrPageId_&ndash;を取得するコンテンツ ページの [OneNote の ID です。<br/><br/>_pbstrPageXmlOut_&ndash; (出力パラメーター) A のポインターへの XML 出力の書き込みを挿入する文字列にします。<br/><br/>_pageInfoToExport_&ndash; (オプション) では、base 64 でエンコードされた、XML コードに埋め込まれている**GetPageContent**メソッドは、バイナリ コンテンツを返す、かどうかを指定します。 バイナリ コンテンツには、たとえば、画像、インク データが含まれます。 _PageInfoToExport_パラメーターを使用して、 **GetPageContent**メソッドが返す XML コードの選択範囲をマークするかどうかも指定します。 [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo)列挙の列挙値が必要です。<br/><br/>_xsSchema_&ndash; (オプション) の **「xml スキーマ」** では、種類の、OneNote の XML スキーマ バージョンを出力することです。 2007 年は、2013 年 2010 年のバージョンの XML スキーマがかどうかを指定するか、現在のバージョンです。 <br/><br/>**注**: お勧め ( **xs2013**) などには、OneNote のバージョンを指定する**xsCurrent**を使用するか、オフのままにするのではなく、アドインを将来のバージョンの OneNote を使用することができます。           |
   
既定では、返された XML 文字列に余分な長さを避けるために OneNote 埋め込みませんバイナリ コンテンツ XML コードにします。 同じ理由から、選択範囲の属性を使用して現在の選択範囲をマークされません。 バイナリ オブジェクトには、そのタグに、OneNote の ID が含まれます。 バイナリ オブジェクトを取得するには、 **GetBinaryPageContent**メソッドを呼び出すし、 **GetPageContent**メソッドから取得した OneNote の ID を渡すことです。 バイナリ データをすぐに必要はありません、 **GetPageContent**メソッドを使用します。 
  
### <a name="updatepagecontent-method"></a>UpdatePageContent メソッド

|||
|:-----|:-----|
|**説明**|ページ上のコンテンツを変更または更新されます。|
|**構文**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**パラメーター**| _bstrPageChangesXmlIn_&ndash;ページを作成する OneNote の XML コードの変更が含まれる文字列です。<br/><br/>_dateExpectedLastModified_&ndash; (省略可能) ページを更新した最後の日付と時刻を変更します。 このパラメーターに 0 以外の値を渡す場合、OneNote は、渡す値は、実際の日付と時刻のページが最後に修正されたと一致する場合にのみ更新プログラムを続行します。 このパラメーターにより、誤って上書きしないようにするために値を渡すことは、ページが変更された最後の時間以降に行われたユーザーを編集します。<br/><br/>_xsSchema_&ndash; (オプション) の **「xml スキーマ」** では、種類の、OneNote の XML スキーマ バージョンを出力することです。 2007 年は、XML スキーマのバージョン 2013、2010 年がかどうかを指定するか、現在のバージョンです。 <br/><br/>**注**: お勧め ( **xs2013**) などには、OneNote のバージョンを指定する**xsCurrent**を使用するか、オフのままにするのではなく、アドインを将来のバージョンの OneNote を使用することができます。<br/><br/>_強制的に_(省略可能)**true**の将来のバージョンの OneNote のページ上に不明なデータがある場合でも、ページのコンテンツを更新するにはそれ以外の場合、 **false** (既定値)。 |
   
さまざまな方法でページを変更するのにには、このメソッドを使用します。 たとえば、アウトラインをページに追加、概要の内容を変更、画像を追加、インクを追加する、コンテンツを移動またはアウトラインのテキストを変更する**UpdatePageContent**メソッドを使用することができます。 
  
具体的な例としては、既存のページをエクスポートする、ページの XML コードを変更してページ全体を再度インポートするのには、 **UpdatePageContent**メソッドを使用する**GetPageContent**メソッドを使用する可能性があります。 または、既存のページの一番下に、画像などのページ上の新しいオブジェクトを追加するのにはこのメソッドを使用する場合があります。 
  
**UpdatePageContent**メソッドに渡す XML コードに含める必要のある唯一のオブジェクトは、(アウトライン、ページで、イメージまたはページ上のインク) のように変更されたページ レベルのオブジェクトです。 このメソッドを変更したりしない、 _bstrPageChangesXmlIn_パラメーターを指定しないページ レベルのオブジェクトを削除します。 メソッドは、アウトラインは、Id と一致するオブジェクトを渡すなど、ページ レベルのオブジェクト全体を置き換えます。 したがって、コードなどの既存のコンテンツ変更を加えたりすることで完全にすべてのページ レベルのオブジェクトを指定してください。 
  
などの場合は、ページには、アウトライン、背景ページのイメージが含まれていますは、アウトラインを交換し、XML コードのアウトラインを完全に指定する、既存のアウトラインでは、ID を使用して、コードでイメージを含まない、そのままのイメージのままにします。 変更されたアウトライン コードに完全に挿入するには、既存のアウトラインが置き換えられる、ためには、アウトラインのすべての内容を含める必要があります。
  
また、 **UpdatePageContent**メソッドは、 _bstrPageChangesXmlIn_パラメーターで指定した要素のプロパティのみを変更します。 などのプロパティを指定するすべてではなく、一部の**PageSettings**要素、するが指定されていないプロパティは変更されません。 
  
次の例では、ページのタイトルを変更し、ページにいくつかのサンプル テキストを追加する**UpdatePageContent**メソッドを使用する方法を示します。 コードを実行する前に、コンピューター上のコードが動作するよう、コードに示すようにページ ID の有効なページ ID に置き換えてください。 **GetHierarchy**メソッドを使用して、出力を調べることによって、ページのページ ID を取得できます。 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"http://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
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
|**説明** <br/> |インクまたは base 64 エンコード文字列として OneNote ページ上のイメージなどのバイナリ オブジェクトを返します。  <br/> |
|**構文** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**パラメーター** <br/> | _bstrPageID_&ndash;バイナリを取得するオブジェクトを含むページの [OneNote の ID です。  <br/><br/>_bstrCallBackID_&ndash; OneNote ID を取得するバイナリ オブジェクトです。 **GetPageContent**メソッドによって返されるページの OneNote の XML コードでは、この ID は、 **callbackID**と呼ばれます。  <br/><br/>_pbstrBinaryObectB64Out_&ndash; (出力パラメーター) A のポインターには、OneNote は base 64 エンコード文字列としてバイナリ オブジェクトを書き込みます。 文字列にします。  <br/> |
   
### <a name="deletepagecontent-method"></a>DeletePageContent メソッド

|||
|:-----|:-----|
|**説明** <br/> |オブジェクトを削除&ndash;ページからオブジェクト**のアウトライン**、**インク**、または**イメージ**のようです。  <br/> |
|**構文** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**パラメーター** <br/> | _bstrPageID_&ndash;を削除するオブジェクトを含むページの [OneNote の ID です。  <br/><br/>_bstrObjectID_&ndash;を削除するオブジェクトの [OneNote の ID です。  <br/><br/>_dateExpectedLastModified_&ndash; (省略可能) を削除するコンテンツを含むページが最後と思われる日付と時刻を変更します。 このパラメーターに 0 以外の値を渡した場合、OneNote は、渡す値は、実際の日付と時刻のページが最後に修正されたと一致する場合にのみ削除を続行します。 このパラメーターの値を渡すことでは、前回のページが変更された後、ユーザーによって行われた編集内容を誤って上書きを防止します。  <br/><br/>_強制的に_&ndash; (オプション)**場合は true**から将来のバージョンの OneNote のページ上に不明なデータがある場合でも、ページのコンテンツを更新するにはそれ以外の場合、 **false** (既定値)。  <br/> |
   
### <a name="publish-method"></a>Publish メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote をサポートする任意の形式でファイルに指定したページをエクスポートします。  <br/> |
|**構文** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_&ndash;エクスポートする階層の [OneNote の ID です。  <br/><br/>_bstrTargetFilePath_&ndash;結果の出力ファイルを保存する場所への絶対パス。 指定したファイルは、その場所にまだ存在していない 1 つである必要があります。  <br/><br/>_pfPublishFormat_&ndash;公開されているページ (例、MTHML、PDF などの) を形式を指定する[PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat)列挙値のいずれかです。  <br/><br/>_bstrCLSIDofExporter_&ndash;拡張メタファイル (.emf) を Microsoft Windows をエクスポートすることができます登録済みの COM アプリケーションのクラス ID (CLSID)。 COM アプリケーションには、 **IMsoDocExporter**インターフェイスを実装する必要があります。 このパラメーターは、カスタム書式指定の OneNote のコンテンツを発行する独自のコードを記述するサード パーティの開発者を許可するように含まれています。 **IMsoDocExporter**インターフェイスの詳細については、 [Office 2007 の固定形式エクスポート機能を拡張する](http://msdn.microsoft.com/en-us/library/office/aa338206%28v=office.12%29.aspx)を参照してください。  <br/> |
   
現時点では、OneNote には、次のファイル形式がサポートされています。
  
- MHTML ファイル (.mht)
- Adobe Acrobat の PDF ファイル (.pdf)
- XML 用紙仕様 (XPS) ファイル (.xps)
- 2013、2010 または 2007 の OneNote (.one) のファイル
- OneNote パッケージ ファイル (.onepkg)
- Microsoft Word の文書 (.doc または .docx)
- Microsoft Windows は拡張メタファイル (.emf)
- HTML ファイル (.html)
    
このメソッドは、UI の **[発行**] をクリックし、形式を指定することによって取得したまったく同じ結果を生成します。 
  
## <a name="navigation-methods"></a>ナビゲーション方法
<a name="ON14DevRef_Application_Navigation"> </a>

このセクションで説明する方法を使用すると、検索し、移動して、OneNote のノートブック、セクション グループ、セクション、ページ、およびページのオブジェクトにリンクできます。
  
### <a name="navigateto-method"></a>NavigateTo メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定されたオブジェクト (たとえば、セクション、ページ、およびページ内で、**アウトライン**の要素) に移動します。  <br/> |
|**構文** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyObjectID_&ndash; OneNote の階層内を移動するオブジェクトの [OneNote の ID です。  <br/><br/>_bstrObjectID_&ndash; OneNote のページ上に移動するオブジェクトの [OneNote の ID です。  <br/><br/>_fNewWindow_&ndash; (オプション)**場合は true**に指定したオブジェクトを新しい OneNote ウィンドウで開きます。 **false**は開くことができません OneNote の新しいウィンドウが開いている場合。  <br/> |
   
### <a name="navigatetourl-method"></a>NavigateToUrl メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote のリンクを渡された場合 (onenote://)、OneNote 内の対応する場所には、OneNote ウィンドウが開きます。 OneNote (http:// または file://) などの外部のリンクが表示された場合、[セキュリティ] ダイアログ ボックスが表示されます。 解雇、OneNote がリンクを開こうとするとされ、 **HResult.hrObjectDoesNotExist**エラーが返されます。  <br/> |
|**構文** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**パラメーター** <br/> | _bstrUrl_&ndash;に移動する場所を示す文字列。 OneNote のリンク、または他の URL、web リンク、またはネットワーク上の場所などが考えられます。  <br/><br/>_fNewWindow_&ndash; (オプション)**場合は true**を新しい OneNote ウィンドウで指定された URL を開きます。 **false**は開くことができません OneNote の新しいウィンドウが開いている場合。  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>GetHyperLinkToObject メソッド

|||
|:-----|:-----|
|**説明** <br/> |指定したノートブック、セクション グループ、セクション、ページ、またはページのオブジェクトへのハイパーリンクを OneNote を取得します。  <br/> |
|**構文** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_&ndash;ノートブック、セクション グループ、セクション、またはページのハイパーリンクの対象となるため、OneNote の ID です。  <br/><br/>_bstrPageContentObjectID_&ndash;内のハイパーリンクの対象となるページのオブジェクトの [OneNote の ID を (省略可能)。 たとえば、オブジェクトには、アウトラインまたは**アウトライン**の要素ができます。 空の文字列を渡す場合 ("")、返されるリンク、ノートブック、セクション グループ、セクション、または_bstrHierarchyID_パラメーターで指定したページです。 _BstrPageContentObjectID_パラメーターに空でない文字列を渡すと、 _bstrHierarchyID_パラメーターは、指定したオブジェクトを含むページへの参照をする必要があります。  <br/><br/>_pbstrHyperlinkOut_&ndash; (出力パラメーター) A のポインターには、 **GetHyperlinkToObject**メソッドはハイパーリンクのテキストを出力を書き込みます。 文字列にします。  <br/> |
   
結果のリンクに移動しようとすると、OneNote を開き、ブラウザーで指定したオブジェクトが表示されます。
  
### <a name="getwebhyperlinktoobject-method"></a>GetWebHyperlinktoObject メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote の Web クライアントで表示されるオブジェクトへのハイパーリンクを返します。  <br/> |
|**構文** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_&ndash; ID にノートブックを OneNote のセクション グループ、セクション、または web のハイパーリンクの対象となるページです。  <br/><br/>_bstrPageContentObjectID_&ndash;内のハイパーリンクの対象となるページのオブジェクトの [OneNote の ID を (省略可能)。 たとえば、オブジェクトには、アウトラインまたは**アウトライン**の要素ができます。 空の文字列を渡す場合 ("")、返されるリンク、ノートブック、セクション グループ、セクション、または_bstrHierarchyID_パラメーターで指定したページです。 _BstrPageContentObjectID_パラメーターに空でない文字列を渡すと、 _bstrHierarchyID_パラメーターは、指定したオブジェクトを含むページへの参照をする必要があります。  <br/><br/>_pbstrHyperlinkOut_&ndash; (出力パラメーター) A のポインターには、 **GetWebHyperlinkToObject**メソッドはハイパーリンクのテキストを出力を書き込みます。 文字列にします。 ノートブックの web のハイパーリンクを作成できない場合は、null 値が返されます。  <br/> |
   
### <a name="findpages-method"></a>FindPages メソッド

|||
|:-----|:-----|
|**説明**|指定したクエリ用語に一致するページの一覧を返します。|
|**構文**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**パラメーター**| _bstrStartNodeID_&ndash;のコンテンツを検索する次のノード (ルート、ノートブック、セクション グループ、またはセクション)。 このパラメーターは、検索のスコープを設定します。<br/><br/>_bstrSearchString_&ndash;検索文字列。 まったく同じ文字列は、OneNote のユーザー インターフェイスで [検索] ボックスに入力を渡します。 すべて大文字でなければならない**** など、**または**、ビットごとの演算子を使用できます。<br/><br/>_pbstrHierarchyXmlOut_&ndash; (出力パラメーター) A のポインターを出力する XML 文字列を作成するのには OneNote を挿入する文字列。 結果の XML 文字列には、ルートから下に向かって、して、検索文字列に一致するすべてのページを含むノートブックの階層が含まれています。 たとえば、 **FindPages**メソッドがないページと一致する、階層内のセクションが表示されません。 のみ 1 つのセクションで、1 ページには、文字列が一致すると、返された階層にはノートブックの階層の他のパーツはないですが、そのセクションとページで、パスが含まれます。<br/><br/>_fIncludeUnindexedPages_&ndash; (オプション)**場合は true** Windows 検索でインデックス付けされていないページを検索するには。それ以外の場合、 **false を指定**します。<br/><br/>_fDisplay_&ndash; (オプション)**場合は true**の場合と同様、ユーザー入力自体も、ユーザーの UI で検索を実行します。 **false** (既定値) の UI の変更は行われていないクエリを実行します。<br/><br/>_xsSchema_&ndash;文字列_pbstrHierarchyXmlOut_の [OneNote の (オプション) スキーマのバージョン。 このオプションの値を使用して、 _pbstrHierarchyXmlOut_の文字列が含まれている OneNote の XML スキーマのバージョンを指定します。 この値を指定しない場合は、OneNote が XML スキーマのバージョン_xsCurrent_であると仮定します。 <br/><br/>**注**: お勧め ( **xs2013**) などには、OneNote のバージョンを指定する**xsCurrent**を使用するか、オフのままにするのではなく、アドインを将来のバージョンの OneNote を使用することができます。           |
   
 **FindPages**は、Microsoft 検索 3.0 または 4.0 がコンピューターにインストールされている場合にのみ動作します。 Windows Vista と Windows 7 には、このコンポーネントが含まれます。 ただし、Windows の以前のバージョンを実行している場合は、 [Windows の検索](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx)機能に**FindPages**をインストールしてください。 
  
### <a name="findmeta-method"></a>FindMeta メソッド

|||
|:-----|:-----|
|**説明**|指定したクエリ条件に一致するメタデータを格納している OneNote オブジェクトの一覧を返します。|
|**構文**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**パラメーター**| _bstrStartNodeID_&ndash;のコンテンツを検索する次のノード (ルート、ノートブック、セクション グループ、またはセクション)。 このパラメーターは、検索のスコープを設定します。<br/><br/>_bstrSearchStringName_&ndash;検索文字列。 メタデータ名の一部を渡します。 場合は空文字列または null 値を渡すと、メタデータを持つすべてのオブジェクトがクエリに一致します。<br/><br/>_pbstrHierarchyXmlOut_&ndash; (出力パラメーター) A のポインターを出力する XML 文字列を作成するのには OneNote を挿入する文字列。 結果の XML 文字列には、ルートから下に向かって、して、検索文字列に一致するすべてのページを含むノートブックの階層が含まれています。 たとえば、 **FindPages**メソッドがないページと一致する、階層内のセクションが表示されません。 のみ 1 つのセクションで、1 ページには、文字列が一致すると、返された階層にはノートブックの階層の他のパーツはないですが、そのセクションとページで、パスが含まれます。  <br/><br/>_fIncludeUnindexedPages_&ndash; (オプション)**場合は true** Windows 検索でインデックス付けされていないページを検索するには。それ以外の場合、 **false を指定**します。<br/><br/>_xsSchema_&ndash;文字列_pbstrHierarchyXmlOut_の [OneNote の (オプション) スキーマのバージョン。 このオプションの値を使用して、 _pbstrHierarchyXmlOut_の文字列が含まれている OneNote の XML スキーマのバージョンを指定します。 この値を指定しない場合は、OneNote が XML スキーマのバージョン_xsCurrent_であると仮定します。 <br/><br/>**注**: お勧め ( **xs2013**) などには、OneNote のバージョンを指定する**xsCurrent**を使用するか、オフのままにするのではなく、アドインを将来のバージョンの OneNote を使用することができます。           |
   
**FindMeta**は、Microsoft Windows 検索 3.0 または 4.0 がコンピューターにインストールされている場合にのみ動作します。 Windows Vista と Windows 7 には、このコンポーネントが含まれます。 ただし、Windows の以前のバージョンを実行している場合は、 [Windows の検索](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx)機能に**FindMeta**をインストールしてください。 
  
## <a name="functional-methods"></a>機能のメソッド
<a name="ON14DevRef_Application_Functional"> </a>

このセクションで説明する方法を使用すると、特定のアクションを実行したり、OneNote アプリケーション内でパラメーターを設定できます。
  
### <a name="mergefiles-method"></a>MergeFiles メソッド

|||
|:-----|:-----|
|**説明** <br/> |1 つに同じファイルの変更をマージすることができます。 ファイルが同じと見なされること、同じ OneNote の ID が必要  <br/> |
|**構文** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**パラメーター** <br/> | _bstrBaseFile_&ndash;ファイルの初期状態の .one ファイルの場所へのパスの文字列です。  <br/><br/>_bstrClientFile_&ndash;ベースのサーバーのファイルの変更をマージした後、ベースのファイルをマージする変更の 2 番目のセットの .one ファイルの場所へのパスの文字列です。  <br/><br/>_bstrServerFile_&ndash;ベースのファイルをマージする変更の最初のセットの .one ファイルの場所へのパスの文字列です。  <br/><br/>_bstrTargetFile_&ndash;マージの変更を含むファイルの .one ファイルの場所へのパスの文字列です。  <br/> |
   
**MergeFiles**メソッドは、OneNote ファイルの複数のバージョンが存在するモバイルのシナリオの目的としています。 
  
### <a name="mergesections-method"></a>MergeSections メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote 内の別の 1 つのセクションの内容をマージします。  <br/> |
|**構文** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**パラメーター** <br/> | _bstrSectionSourceId_&ndash; OneNote ID セクションをマージするのです。  <br/><br/>_bstrSectionDestinationId_&ndash;に結合されるセクションの [OneNote の ID です。 ソース] セクションは、この目的のセクションに結合されます。  <br/> |
   
このメソッドは、セクションを右クリックしたときに表示されている**別のセクションにマージ**フィーチャーと同じ操作を実行します。 
  
### <a name="quickfiling-method"></a>QuickFiling メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote の階層ツリー内の場所を選択するのには使用することができます [ [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog) ] ダイアログ ボックスのインスタンスを返します。  <br/> |
|**構文** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>SyncHierarchy メソッド

|||
|:-----|:-----|
|**説明** <br/> |ディスク上のソース ファイルで指定したオブジェクトの同期を強制します。  <br/> |
|**構文** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**パラメーター** <br/> | _bstrHierarchyID_&ndash; OneNote の ID オブジェクトを同期します。  <br/> |
   
### <a name="setfilinglocation-method"></a>SetFilingLocation メソッド

|||
|:-----|:-----|
|**説明** <br/> |OneNote で特定の種類のコンテンツを提出する必要があります場所と方法を指定することができます。  <br/> |
|**構文** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**パラメーター** <br/> | _flToSet_&ndash;を設定するファイルの場所のオブジェクトの種類です。  <br/><br/>_fltToSet_&ndash;で、先にファイルの種類です。  <br/><br/>_bstrFilingSectionID_&ndash;のどの位置を設定するセクションまたはページの [OneNote の ID です。 表示しない場合は、該当する場合、ユーザーは null または空の文字列で渡すことができます。  <br/> |
   
ファイリングできるコンテンツの種類には、Outlook アイテムおよび OneNote にインポートすると各アプリケーションの [ **OneNote に送る**] コマンドを使用する Internet Explorer の Web ノートが含まれます。 このメソッドを使用して OneNote に印刷される項目のファイルの場所を設定することもできます。 
  
## <a name="properties"></a>プロパティ
<a name="ON14DevRef_Application_Properties"> </a>

このセクションでは、**アプリケーション**のインターフェイスのプロパティについて説明します。 
  
|**プロパティ**|**説明**|
|:-----|:-----|
|**Windows** <br/> |開いている OneNote ウィンドウにユーザー アクセスを示します。 このプロパティでは、OneNote ウィンドウの集合を列挙し、特定のウィンドウのプロパティを変更することができます。 詳細については、 [Windows のインターフェイス](window-interfaces-onenote.md)を参照してください。  <br/> |
|**COMAddIns** <br/> |OneNote の**COMAddIns**コレクションを取得します。 このコレクションには、OneNote で使用可能な COM アドインのすべてが含まれます。 **COMAddins**コレクションの**Count**プロパティは、使用可能な COM アドインの数を返します。詳細については、 [COMAddIns](http://msdn.microsoft.com/en-us/library/office/ff865489.aspx)オブジェクトを参照してください。  <br/> |
|**LanguageSettings** <br/> |OneNote の一般的な言語の設定を変更するのにはいくつかの Api にアクセスできます。  <br/> |
   
## <a name="events"></a>イベント
<a name="ON14DevRef_Application_Events"> </a>

このセクションでは、アプリケーションのインターフェイスのイベントについて説明します。
  
> [!CAUTION]
> イベントは、マネージ コードで現在追加ことはできません。 
  
### <a name="onnavigate-event"></a>OnNavigate イベント

|||
|:-----|:-----|
|**説明** <br/> |ユーザーは OneNote の UI が OneNote の現在の場所から移動したときに呼び出される関数を設定できます。  <br/> |
|**構文** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>OnHierarchyChange メソッド

|||
|:-----|:-----|
|**説明** <br/> |ユーザーが呼び出される関数を設定することができますいつでも、OneNote 階層の変更 (追加またはページを削除するなど、セクションを移動する)。 階層の変更はバッチ処理されるため、OneNote がイベントを 1 回発生させるとほぼ同時にある複数の変更が発生した場合。  <br/> |
|**構文** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**パラメーター** <br/> | _bstrActivePageID_&ndash; 、OneNote、作業中のページの ID を渡します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [OneNote の開発者用リファレンス](onenote-developer-reference.md)

