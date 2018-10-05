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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386706"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>InfoPath オブジェクト モデルを使用してイベント ハンドラーを追加する

InfoPath 2003 オブジェクト モデルと互換性のあるフォーム テンプレート プロジェクトでイベント ハンドラー関数を追加するメニュー コマンドは、他の種類のフォーム テンプレートの場合と基本的に同じです。たとえば、 **OnLoad** イベント ハンドラーを追加するには、InfoPath のデザイン モードでフォーム テンプレートを開いているときに、[ **開発**] タブの [ **OnLoad イベント**] をクリックします。Visual Studio 2012 コード エディターの **OnLoad** イベント ハンドラーのフォーム コードに自動的にフォーカスが切り替わります。 
  
InfoPath 2003 と互換性のあるマネージ コードのフォーム テンプレート プロジェクトでは、イベント ハンドラー関数を含むクラスとイベント ハンドラー自体が、コード モジュール内で InfoPath に固有の属性によって識別されます。

## <a name="adding-event-handlers"></a>イベント ハンドラーの追加

以下に示すすべての手順では、フォーム テンプレート プロジェクトが Visual Studio 2012 を使用した Microsoft InfoPath で開いていることを前提とします。
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>コマンド ボタンの OnClick イベントに対するイベント ハンドラーを追加する

1. [ **コントロール**] ウィンドウで、[ **ボタン**] をクリックしてフォームにボタンを追加します。 
    
2. [ **プロパティ**] タブの [ **ユーザー設定コード**] をクリックします。
    
   コード エディターの [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) イベントのいずれかに対するイベント ハンドラーのスタブにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>フィールドまたはグループの OnBeforeChange、OnValidate、または OnAfterChange イベントに対するイベント ハンドラーを追加する

1. たとえば [ **テキスト ボックス**] コントロールなど、フィールドまたはグループにバインドされたデータ入力コントロールを右クリックします。 
    
2. **[プログラミング]** をポイントし、いずれかのコマンド (**On Validate Event** など) をクリックします。
    
   コード エディターの [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx)、[OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)、[OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) のいずれかのイベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>フォームの OnLoad、OnSwitchView、OnContextChange、または OnSign イベントのイベント ハンドラーを追加します。

- **[ツール]** メニューの **[プログラミング]** をポイントし、イベント ハンドラーを作成するフォーム イベントをクリックします。
    
    コード エディターの [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx)、[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx)、[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)、[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) のいずれかに対するイベント ハンドラーのスタブにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>フォームの OnSubmitRequest イベントのイベント ハンドラーを追加します。

1. [ **データ**] タブの [ **送信オプション**] をクリックします。
    
2. [ **ユーザーによるこのフォームの送信を許可する**] チェック ボックスをオンにして、[ **コードを使用してユーザー設定操作を実行する**] をクリックします。
    
3. [ **コードの編集**] をクリックし、[ **OK**] をクリックします。
    
   コード エディターの [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) イベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>フォームの OnSaveRequest イベントに対するイベント ハンドラーを追加する

1. [ **ファイル**] タブをクリックし、[ **フォームのオプション**] をクリックします。
    
2. [ **保存**] カテゴリで、[ **ユーザー設定コードを使って保存**]、[ **編集**]、[ **OK**] の順にクリックします。
    
   コード エディターの [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) イベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>フォームの OnVersionUpgrade イベントに対するイベント ハンドラーを追加する

1. [ **ファイル**] タブをクリックし、[ **フォームのオプション**] をクリックします。
    
2. [ **バージョン管理**] カテゴリで、[ **既存のフォームの更新**] の一覧の [ **ユーザー設定イベントの使用**] をクリックし、[ **編集**] をクリックして、[ **OK**] をクリックします。
    
    コード エディターの [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) イベントに対するイベント ハンドラーのスタブにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>フォームの OnMergeRequest イベントに対するイベント ハンドラーを追加する

1. [ **ファイル**] タブの [ **フォームのオプション**] をクリックします。
    
2. [ **詳細設定**] カテゴリで、[ **フォームの結合を有効にする**] チェック ボックスと [ **ユーザー設定コードを使って結合する**] チェック ボックスをオンにして、[ **編集**] をクリックし、[ **OK**] をクリックします。
    
    コード エディターの [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) イベントのイベント ハンドラーのスタブにフォーカスが切り替わります。 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>OnAfterImport イベントに対するイベント ハンドラーを追加する

[OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) イベントのイベント ハンドラーを追加するには、マネージ コードのフォーム テンプレートのフォーム コードを開き、イベント ハンドラー関数を手動で追加する必要があります。このイベントのイベント ハンドラーを作成する方法については、 **OnAfterImport** イベントのリンクをクリックしてください。 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>セカンダリ データ ソースに対するイベント ハンドラーを追加する

次の例では、セカンダリ データ ソースにイベント ハンドラーを追加する方法を示します。この例では、次のスキーマを持つ books.xml というリソース ファイルからのセカンダリ データ ソースを想定しています。
  
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

このデータ ソースからフォームのビューが作成されます。フォーム コードは著者と著者が書いた本の数に基づいてハッシュ テーブルを作成します。ビューに表示されるテーブルから項目を更新すると、 **OnAfterChange** イベント ハンドラーがハッシュ テーブルを更新します。 [InfoPathEventHandler](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) 属性 ( **InfoPathEventHandlerAttribute** クラスによって実装される) の [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) プロパティを使用してセカンダリ データ ソースが参照される点に注意してください。 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>イベント ハンドラーを含むクラスの識別方法

InfoPath 2003 のマネージ コード オブジェクト モデルと互換性のある新しい InfoPath フォーム テンプレート プロジェクトを作成すると、フォーム コード モジュール先頭のクラスにアセンブリ レベルの **System.ComponentModel.Description** 属性が適用され、これによってフォーム テンプレートのすべてのイベント ハンドラーを含むクラスが識別されます。 
  
> [!IMPORTANT]
> このクラスの **System.ComponentModel.Description** 属性は変更しないでください。変更すると、イベント ハンドラーがどこにあるかをフォーム テンプレートは特定できず、イベント ハンドラーが実行されません。 
  
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

## <a name="how-event-handlers-are-identified"></a>イベント ハンドラーの識別方法

InfoPath のデザイン モード ユーザー インターフェイスのメニュー コマンドまたはボタンを使用して新しいイベント ハンドラーを追加すると、イベント ハンドラー関数のスタブがフォームに書き込まれます。次の例では、total というフィールドの [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) を追加したときに作成されるスタブ イベント ハンドラーを示します。 
  
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

用意されたスタブに、 `thisXDocument` 変数または  `thisApplication` 変数のキャッシュされるプライベート メンバーを使用したり、イベント ハンドラーが受け取る  `e` **EventArgs** オブジェクトからアクセスするメンバーを使用したりして、InfoPath オブジェクト モデルのメンバーを起動するコードを追加できます。 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

**InfoPathEventHandler** 属性 ( [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) クラスで定義される) は、イベント ハンドラーとして使用する関数のカスタム属性です。 
  
イベントに必要な場合、 **MatchPath** パラメーター ( [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) クラスの **MatchPath** プロパティで定義される) はイベント ソースを識別する XPath 式を示しています。 **EventType** パラメーター ( [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) クラスの **EventType** プロパティで定義される) はイベントの種類を示しています。これらのパラメーターの値は変更しないでください。これらのパラメーターの値を変更すると、イベント ハンドラーが正しくコンパイルされないことや、イベント通知が予定どおりに発生しないことがあります。 
  
## <a name="obfuscating-code-in-event-handlers"></a>イベント ハンドラーのコードを隠ぺいする

マネージ コードのフォーム テンプレートをコンパイルしたときに生成されるアセンブリ ( *projectname*  .dll) に隠ぺいユーティリティを実行すると、ユーザーがフォームを開いたときに InfoPath がアセンブリを読み込めません。イベント ハンドラーやその他のコードを隠ぺいする必要がある場合は、隠ぺいするコードを別のアセンブリに置き、プロジェクトでそのアセンブリを参照し、参照先アセンブリのメンバーを FormCode.cs または FormCode.vb から呼び出してください。隠ぺいユーティリティは参照するアセンブリだけに実行することが重要です。 
  
## <a name="see-also"></a>関連項目

- [InfoPath 2003 オブジェクト モデルを使用してフォーム イベントに応答する](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

