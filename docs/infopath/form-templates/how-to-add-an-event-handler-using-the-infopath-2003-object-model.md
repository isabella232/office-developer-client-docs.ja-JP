---
title: InfoPath オブジェクト モデルを使用してイベント ハンドラーを追加する
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- onafterimport event [infopath 2007],OnAfterChange event [InfoPath 2007],OnBeforeChange event [InfoPath 2007],OnSubmitRequest event [InfoPath 2007],OnVersionUpgrade event [InfoPath 2007],InfoPath 2003-compatible form templates, event handlers,OnLoad event [InfoPath 2007],event handlers [InfoPath 2007], adding using InfoPath 2003 object model,OnValidate event [InfoPath 2007],OnContextChange event [InfoPath 2007],OnSaveRequest event [InfoPath 2007],OnClick event [InfoPath 2007],OnSwitchView event [InfoPath 2007],OnSign event [InfoPath 2007],OnMergeRequest event [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: InfoPath 2003 オブジェクト モデルと互換性のあるフォーム テンプレート プロジェクトにイベント ハンドラー関数を追加するためのメニュー コマンドは、その他の種類のフォーム テンプレートと実質的に同一です。
ms.openlocfilehash: 8533b6bc11dccdad9d0f05de35406ad3cf68eacd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303669"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a><span data-ttu-id="e37a1-104">InfoPath オブジェクト モデルを使用してイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-104">Add an event handler using the InfoPath object model</span></span>

<span data-ttu-id="e37a1-p101">InfoPath 2003 オブジェクト モデルと互換性のあるフォーム テンプレート プロジェクトでイベント ハンドラー関数を追加するメニュー コマンドは、他の種類のフォーム テンプレートの場合と基本的に同じです。たとえば、 **OnLoad** イベント ハンドラーを追加するには、InfoPath のデザイン モードでフォーム テンプレートを開いているときに、[ **開発**] タブの [ **OnLoad イベント**] をクリックします。Visual Studio 2012 コード エディターの **OnLoad** イベント ハンドラーのフォーム コードに自動的にフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p101">The menu commands for adding event handler functions in a form template project that is compatible with the InfoPath 2003 object model are essentially the same as those for other types of form templates. For example, in order to add an **OnLoad** event handler, with the form template open in the InfoPath designer, click the **On Load Event** command on the **Developer** tab. The focus automatically switches to the form code for the **OnLoad** event handler in the Visual Studio 2012 code editor.</span></span> 
  
<span data-ttu-id="e37a1-107">InfoPath 2003 と互換性のあるマネージ コードのフォーム テンプレート プロジェクトでは、イベント ハンドラー関数を含むクラスとイベント ハンドラー自体が、コード モジュール内で InfoPath に固有の属性によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="e37a1-107">In managed-code form template projects compatible with InfoPath 2003, the class that contains event handler functions and the event handlers themselves are identified by attributes specific to InfoPath in the code module.</span></span>

## <a name="adding-event-handlers"></a><span data-ttu-id="e37a1-108">イベント ハンドラーの追加</span><span class="sxs-lookup"><span data-stu-id="e37a1-108">Adding event handlers</span></span>

<span data-ttu-id="e37a1-109">以下に示すすべての手順では、フォーム テンプレート プロジェクトが Visual Studio 2012 を使用した Microsoft InfoPath で開いていることを前提とします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-109">All of the following procedures assume that you have a form template project open in Microsoft InfoPath with Visual Studio 2012.</span></span>
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a><span data-ttu-id="e37a1-110">コマンド ボタンの OnClick イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-110">Add an event handler for the OnClick event of a command button</span></span>

1. <span data-ttu-id="e37a1-111">[ **コントロール**] ウィンドウで、[ **ボタン**] をクリックしてフォームにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="e37a1-111">In the **Controls** pane, click **Button** to add a button to the form.</span></span> 
    
2. <span data-ttu-id="e37a1-112">[ **プロパティ**] タブの [ **ユーザー設定コード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-112">On the **Properties** tab, click **Custom Code**.</span></span>
    
   <span data-ttu-id="e37a1-113">コード エディターの [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) イベントのいずれかに対するイベント ハンドラーのスタブにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-113">The focus switches to the stub for the event handler for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a><span data-ttu-id="e37a1-114">フィールドまたはグループの OnBeforeChange、OnValidate、または OnAfterChange イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-114">Add an event handler for the OnBeforeChange, OnValidate, or OnAfterChange event of a field or group</span></span>

1. <span data-ttu-id="e37a1-115">たとえば [ **テキスト ボックス**] コントロールなど、フィールドまたはグループにバインドされたデータ入力コントロールを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-115">Right-click a data-entry control bound to the field or group, such as a **Text Box** control.</span></span> 
    
2. <span data-ttu-id="e37a1-116">**[プログラミング]** をポイントし、いずれかのコマンド (**On Validate Event** など) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-116">Point to **Programming**, and then click one of the commands, such as **On Validate Event**.</span></span>
    
   <span data-ttu-id="e37a1-117">コード エディターの [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx)、[OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)、[OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) のいずれかのイベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-117">The focus switches to the stub for the event handler for one of the following events in the code editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx), or [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a><span data-ttu-id="e37a1-118">フォームの OnLoad、OnSwitchView、OnContextChange、または OnSign イベントのイベント ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="e37a1-118">Add an event handler for the OnLoad, OnSwitchView, OnContextChange, or OnSign event of a form</span></span>

- <span data-ttu-id="e37a1-119">**[ツール]** メニューの **[プログラミング]** をポイントし、イベント ハンドラーを作成するフォーム イベントをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-119">On the **Tools** menu, point to **Programming**, and then click the form event that you want to write an event handler for.</span></span>
    
    <span data-ttu-id="e37a1-120">コード エディターの [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx)、[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx)、[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)、[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) のいずれかに対するイベント ハンドラーのスタブにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-120">The focus switches to the stub for the event handler for one of the following in the code editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx), or [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a><span data-ttu-id="e37a1-121">フォームの OnSubmitRequest イベントのイベント ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="e37a1-121">Add an event handler for the OnSubmitRequest event of a form</span></span>

1. <span data-ttu-id="e37a1-122">[ **データ**] タブの [ **送信オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-122">On the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="e37a1-123">[ **ユーザーによるこのフォームの送信を許可する**] チェック ボックスをオンにして、[ **コードを使用してユーザー設定操作を実行する**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-123">Select the **Allow users to submit this form** check box, and then click **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="e37a1-124">[ **コードの編集**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-124">Click **Edit Code**, and then click **OK**.</span></span>
    
   <span data-ttu-id="e37a1-125">コード エディターの [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) イベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-125">The focus switches to the stub for the event handler for the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a><span data-ttu-id="e37a1-126">フォームの OnSaveRequest イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-126">Add an event handler for the OnSaveRequest event of a form</span></span>

1. <span data-ttu-id="e37a1-127">[ **ファイル**] タブをクリックし、[ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-127">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="e37a1-128">[ **保存**] カテゴリで、[ **ユーザー設定コードを使って保存**]、[ **編集**]、[ **OK**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-128">In the **Save** category, click **Save using custom code**, click **Edit**, and then click **OK**.</span></span>
    
   <span data-ttu-id="e37a1-129">コード エディターの [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) イベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-129">The focus switches to the stub for the event handler for the [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a><span data-ttu-id="e37a1-130">フォームの OnVersionUpgrade イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-130">Add an event handler for the OnVersionUpgrade event of a form</span></span>

1. <span data-ttu-id="e37a1-131">[ **ファイル**] タブをクリックし、[ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-131">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="e37a1-132">[ **バージョン管理**] カテゴリで、[ **既存のフォームの更新**] の一覧の [ **ユーザー設定イベントの使用**] をクリックし、[ **編集**] をクリックして、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-132">In the **Versioning** category, select **Use custom event** from the **Update existing forms** list, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="e37a1-133">コード エディターの [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) イベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-133">The focus switches to the stub for the event handler for the [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a><span data-ttu-id="e37a1-134">フォームの OnMergeRequest イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-134">Add an event handler for the OnMergeRequest event of a form</span></span>

1. <span data-ttu-id="e37a1-135">[ **ファイル**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-135">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="e37a1-136">[ **詳細設定**] カテゴリで、[ **フォームの結合を有効にする**] チェック ボックスと [ **ユーザー設定コードを使って結合する**] チェック ボックスをオンにして、[ **編集**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e37a1-136">In the **Advanced** category, select the **Enable Form merging** and the **Merge using custom code** check boxes, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="e37a1-137">コード エディターの [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) イベントのイベント ハンドラーのスタブにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-137">The focus switches to the stub for the event handler for the [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) event in the code editor.</span></span> 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a><span data-ttu-id="e37a1-138">OnAfterImport イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-138">Adding an event handler for the OnAfterImport event</span></span>

<span data-ttu-id="e37a1-p102">[OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) イベントのイベント ハンドラーを追加するには、マネージ コードのフォーム テンプレートのフォーム コードを開き、イベント ハンドラー関数を手動で追加する必要があります。このイベントのイベント ハンドラーを作成する方法については、 **OnAfterImport** イベントのリンクをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p102">To add event handlers for the [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) event, you must open the form code for your managed-code form template and add the event handler function manually. For information on how to write an event handler for this event, click the link for the **OnAfterImport** event.</span></span> 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a><span data-ttu-id="e37a1-141">セカンダリ データ ソースに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="e37a1-141">Adding an event handler for a secondary data source</span></span>

<span data-ttu-id="e37a1-p103">次の例では、セカンダリ データ ソースにイベント ハンドラーを追加する方法を示します。この例では、次のスキーマを持つ books.xml というリソース ファイルからのセカンダリ データ ソースを想定しています。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p103">The following example shows how to add an event handler for a secondary data source. The example assumes a secondary data source from a resource file named books.xml, which has the following schema:</span></span>
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema">
    <xsd:element name="catalog">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element ref="book" minOccurs="0" maxOccurs="unbounded"></xsd:element>
            </xsd:sequence>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="genre" type="xsd:string"></xsd:element>
    <xsd:element name="author" type="xsd:string"></xsd:element>
    <xsd:element name="book">
        <xsd:complexType>
            <xsd:all>
                <xsd:element ref="author" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="title" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="genre" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="price" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="publish_date" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="description" minOccurs="0" maxOccurs="1"></xsd:element>
            </xsd:all>
            <xsd:attribute ref="id"></xsd:attribute>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="price" type="xsd:string"></xsd:element>
    <xsd:element name="title" type="xsd:string"></xsd:element>
    <xsd:element name="publish_date" type="xsd:string"></xsd:element>
    <xsd:element name="description" type="xsd:string"></xsd:element>
    <xsd:attribute name="id" type="xsd:string"></xsd:attribute>
</xsd:schema>

```

<br/>

<span data-ttu-id="e37a1-p104">このデータ ソースからフォームのビューが作成されます。フォーム コードは著者と著者が書いた本の数に基づいてハッシュ テーブルを作成します。ビューに表示されるテーブルから項目を更新すると、 **OnAfterChange** イベント ハンドラーがハッシュ テーブルを更新します。 [InfoPathEventHandler](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) 属性 ( **InfoPathEventHandlerAttribute** クラスによって実装される) の [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) プロパティを使用してセカンダリ データ ソースが参照される点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p104">The form's view is built from this data source. The form code creates a hash table based on the authors and the number of books they have written. You can update an entry from the table shown in the view and the **OnAfterChange** event handler updates the hash table. Note that the [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) property of the **InfoPathEventHandler** attribute (which is implemented by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is used to reference the secondary data source.</span></span> 
  
```cs
namespace AuxDom
{
    // InfoPathNamespace attribute goes here.
    public class AuxDom
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        private Hashtable authors;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            authors = new Hashtable();
        }
        public void _Shutdown()
        {
            authors.Clear();
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
        public void OnLoad(DocReturnEvent e)
        {
            IXMLDOMDocument books = thisXDocument.GetDOM("books");
            DOMNodeList externalAuthors = books.selectNodes("/catalog/book/author");
            foreach (IXMLDOMNode authorNode in externalAuthors)
            {
                AddBookFromAuthor(authorNode.text);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="/catalog/book/author", EventType=InfoPathEventType.OnAfterChange, DataObject="books")]
        public void books__author_OnAfterChange(DataDOMEvent e)
        {
            if (e.IsUndoRedo)
            {
                // An undo or redo operation has occurred and the DOM 
                // is read-only.
                return;
            }
            
            if (e.Source.text != e.NewValue.ToString())
            {
                RemoveBookFromAuthor(e.OldValue.ToString());
                AddBookFromAuthor(e.NewValue.ToString());
            }
        }
        private void AddBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] + 1;
            }
            else
            {
                authors.Add(authorName, 1);
            }
        }
        private void RemoveBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] - 1;
            }
            if ((int)authors[authorName] == 0)
            {
                authors.Remove(authorName);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="ShowAuthors", EventType=InfoPathEventType.OnClick)]
        public void ShowAuthors_OnClick(DocActionEvent e)
        {
            // Write your code here.
            StringBuilder report = new StringBuilder();
            foreach (string authorName in authors.Keys)
            {
                report.Append(authorName + ",\t\t\t");
                report.Append(authors[authorName] + "\n");
            }
            thisXDocument.UI.Alert(report.ToString());
        }
    }
}

```

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a><span data-ttu-id="e37a1-148">イベント ハンドラーを含むクラスの識別方法</span><span class="sxs-lookup"><span data-stu-id="e37a1-148">How the class that contains event handlers is identified</span></span>

<span data-ttu-id="e37a1-149">InfoPath 2003 のマネージ コード オブジェクト モデルと互換性のある新しい InfoPath フォーム テンプレート プロジェクトを作成すると、フォーム コード モジュール先頭のクラスにアセンブリ レベルの **System.ComponentModel.Description** 属性が適用され、これによってフォーム テンプレートのすべてのイベント ハンドラーを含むクラスが識別されます。</span><span class="sxs-lookup"><span data-stu-id="e37a1-149">When you create a new InfoPath form template project that is compatible with the InfoPath 2003 managed code object model, an assembly-level **System.ComponentModel.Description** attribute is applied to the class at the beginning of the form code module to identify the class that contains all event handlers for the form template.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e37a1-p105">このクラスの **System.ComponentModel.Description** 属性は変更しないでください。変更すると、イベント ハンドラーがどこにあるかをフォーム テンプレートは特定できず、イベント ハンドラーが実行されません。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p105">Do not modify the **System.ComponentModel.Description** attribute in this class. If you do so, your form template will not be able to identify where event handlers are located, and the event handlers will fail to run.</span></span> 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the // form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute(    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
' Office integration attribute. Identifies the startup class for the form. Do not modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
```

## <a name="how-event-handlers-are-identified"></a><span data-ttu-id="e37a1-152">イベント ハンドラーの識別方法</span><span class="sxs-lookup"><span data-stu-id="e37a1-152">How event handlers are identified</span></span>

<span data-ttu-id="e37a1-p106">InfoPath のデザイン モード ユーザー インターフェイスのメニュー コマンドまたはボタンを使用して新しいイベント ハンドラーを追加すると、イベント ハンドラー関数のスタブがフォームに書き込まれます。次の例では、total というフィールドの [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) を追加したときに作成されるスタブ イベント ハンドラーを示します。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p106">When you add a new event handler using menu commands or buttons in the InfoPath design mode user interface, the stub for the event handler function is written into the form. The following example shows the stub event handler created for an [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) added for a field named 'total'.</span></span> 
  
```cs
[InfoPathEventHandler(MatchPath="/invoice/total", EventType=InfoPathEventType.OnValidate)]
public void total_OnValidate(DataDOMEvent e)
{
    // Write your code here.
}

```

```vb
<InfoPathEventHandler(MatchPath:="/invoice/total",EventType:= OnValidate)> Public Sub total_OnValidate(ByVal e As EventArgs)
    ' Write your code here.
End Sub

```

<span data-ttu-id="e37a1-155">用意されたスタブに、 `thisXDocument` 変数または  `thisApplication` 変数のキャッシュされるプライベート メンバーを使用したり、イベント ハンドラーが受け取る  `e` **EventArgs** オブジェクトからアクセスするメンバーを使用したりして、InfoPath オブジェクト モデルのメンバーを起動するコードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e37a1-155">You can then add code that invokes members of the InfoPath object model using the private cached members of the  `thisXDocument` or  `thisApplication` variables, or by using the members accessed from the  `e` **EventArgs** object received by the event handler:</span></span> 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

<span data-ttu-id="e37a1-156">**InfoPathEventHandler** 属性 ( [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) クラスで定義される) は、イベント ハンドラーとして使用する関数のカスタム属性です。</span><span class="sxs-lookup"><span data-stu-id="e37a1-156">The **InfoPathEventHandler** attribute (as defined by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is the custom attribute for functions that will be used as event handlers.</span></span> 
  
<span data-ttu-id="e37a1-p107">イベントに必要な場合、 **MatchPath** パラメーター ( [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) クラスの **MatchPath** プロパティで定義される) はイベント ソースを識別する XPath 式を示しています。 **EventType** パラメーター ( [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) クラスの **EventType** プロパティで定義される) はイベントの種類を示しています。これらのパラメーターの値は変更しないでください。これらのパラメーターの値を変更すると、イベント ハンドラーが正しくコンパイルされないことや、イベント通知が予定どおりに発生しないことがあります。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p107">When required by the event, the **MatchPath** parameter (as defined by the [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies an XPath expression that identifies the event source. The **EventType** parameter (as defined by the [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies the type of event. You should not change the values of these parameters. If the values of these parameters are changed, the event handler may not compile correctly, or event notification will not occur as expected.</span></span> 
  
## <a name="obfuscating-code-in-event-handlers"></a><span data-ttu-id="e37a1-161">イベント ハンドラーのコードを隠ぺいする</span><span class="sxs-lookup"><span data-stu-id="e37a1-161">Obfuscating code in event handlers</span></span>

<span data-ttu-id="e37a1-p108">マネージ コードのフォーム テンプレートをコンパイルしたときに生成されるアセンブリ ( *projectname*  .dll) に隠ぺいユーティリティを実行すると、ユーザーがフォームを開いたときに InfoPath がアセンブリを読み込めません。イベント ハンドラーやその他のコードを隠ぺいする必要がある場合は、隠ぺいするコードを別のアセンブリに置き、プロジェクトでそのアセンブリを参照し、参照先アセンブリのメンバーを FormCode.cs または FormCode.vb から呼び出してください。隠ぺいユーティリティは参照するアセンブリだけに実行することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e37a1-p108">If you run an obfuscator utility on the assembly that is generated when a managed-code form template is compiled ( *projectname*  .dll), InfoPath will not be able to load the assembly when a user opens the form. If you want to obfuscate the code for your event handlers or other form code, you must put the code that you want to obfuscate in a separate assembly, and reference that assembly in your project, and then call members of the referenced assembly from FormCode.cs or FormCode.vb. It is important that you run the obfuscator utility only on the referenced assembly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e37a1-165">関連項目</span><span class="sxs-lookup"><span data-stu-id="e37a1-165">See also</span></span>

- [<span data-ttu-id="e37a1-166">InfoPath 2003 オブジェクト モデルを使用してフォーム イベントに応答する</span><span class="sxs-lookup"><span data-stu-id="e37a1-166">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

