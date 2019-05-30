---
title: InfoPath 2003 オブジェクト モデルを使用する初期化コードと後処理コード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, clean-up code,InfoPath 2003-compatible form templates, initialization code
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: 既定では、InfoPath 2003 と互換性のあるフォーム テンプレート プロジェクトについて作成される FormCode.cs または FormCode.vb ファイルには、フォームのプログラム ロジックに対するすべてのソース コードが含まれています。プロジェクトのテンプレートによって FormCode.cs または FormCode.vb ファイルに以下の例とよく似たクラスが生成され、このクラスには、フォーム イベントのハンドラーだけでなく、初期化コードと後処理コードも定義できます。FormCode.cs および FormCode.vb ファイルは、イベント ハンドラーが実装される唯一のクラスとしてこのクラスを識別する、アセンブリ レベルの System.ComponentModel.DescriptionAttribute 属性を使用します。InfoPathNamespace 属性 (InfoPathNamespaceAttribute 型が実装する) をクラスに適用して、クラス内で使用する XML DOM セレクション名前空間を識別します。InfoPathNamespace で参照される名前空間は、InfoPath プロジェクト システムによって管理されます。
ms.openlocfilehash: 659214a21dacf75b12f36cb6ad1e7f09c5af8800
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538369"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用する初期化コードと後処理コード

既定では、InfoPath 2003 と互換性のあるフォーム テンプレート プロジェクトについて作成される FormCode.cs または FormCode.vb ファイルには、フォームのプログラム ロジックに対するすべてのソース コードが含まれています。プロジェクトのテンプレートによって FormCode.cs または FormCode.vb ファイルに以下の例とよく似たクラスが生成され、このクラスには、フォーム イベントのハンドラーだけでなく、初期化コードと後処理コードも定義できます。FormCode.cs および FormCode.vb ファイルは、イベント ハンドラーが実装される唯一のクラスとしてこのクラスを識別する、アセンブリ レベルの **System.ComponentModel.DescriptionAttribute** 属性を使用します。 **InfoPathNamespace** 属性 ( [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) 型が実装する) をクラスに適用して、クラス内で使用する XML DOM セレクション名前空間を識別します。 **InfoPathNamespace** で参照される名前空間は、InfoPath プロジェクト システムによって管理されます。 
  
FormCode クラス自体が、フォームが開いている間に InfoPath の標準的な機能に加えて必要となるコンポーネントに対して、初期化ルーチンと後処理ルーチンを実行するために使用する  `_Startup` および  `_Shutdown` メソッドを提供します。 
  
> [!IMPORTANT]
> InfoPath オブジェクト モデルのメンバーは、 `_Startup` および  `_Shutdown` メソッド内から呼び出さないでください。これらのメソッドでは、外部コンポーネントのメンバーだけを初期化し、呼び出さなければなりません。 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
    public partial class FormCode
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // You can add additional initialization code here.
        }
        public void _Shutdown()
        {
        }
    }
}
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
    ' The namespace prefixes defined in this attribute must remain synchronized with
    ' those in the form definition file (.xsf).
    <InfoPathNamespace( _
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
    Public Class FormCode
        Private thisXDocument As XDocument
        Private thisApplication As Application
        Public Sub _Startup(app As Application, doc As XDocument)
            thisXDocument = doc
            thisApplication = app
            ' You can add additional initialization code here.
        End Sub
        Public Sub _Shutdown()
        End Sub
    End Class
End Namespace
```

## <a name="the-startup-method"></a>_Startup メソッド

追加コンポーネントの初期化コードを記述する場所を提供することに加え、 `_Startup` メソッドは、フォーム コードで InfoPath オブジェクト モデルの `thisXDocument` および `thisApplication` クラスのメンバーにアクセスするために使用できる  [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) および  [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) 変数を初期化します。この 2 つの変数を初期化するために必要なコードは、プロジェクト テンプレートによって自動的に生成されます。 
  
```cs
    private XDocument thisXDocument;
    private Application thisApplication;
    public void _Startup(Application app, XDocument doc)
    {
        thisXDocument = doc;
        thisApplication = app;
        // You can add additional initialization code here.
    }
```

```vb
    Private thisXDocument As XDocument
    Private thisApplication As Application
    Public Sub _Startup(app As Application, doc As XDocument)
        thisXDocument = doc
        thisApplication = app
        ' You can add additional initialization code here.
    End Sub

```

次の例では、 `thisXDocument` 変数を使用して [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) 型の [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) メソッドにアクセスする、簡単なボタンのイベント ハンドラーを示しています。 
  
```cs
[InfoPathEventHandler(MatchPath="CTRL1_5", EventType=InfoPathEventType.OnClick)]
public void CTRL1_5_OnClick(DocActionEvent e)
{
    // Write your code here.
    thisXDocument.UI.Alert("Hello!");
}
```

```vb
<InfoPathEventHandler(MatchPath:="CTRL1_5", EventType:=InfoPathEventType.OnClick)> _
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
    ' Write your code here.
    thisXDocument.UI.Alert("Hello!")
End Sub
```

イベント ハンドラーの作成方法については、「[InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加する方法](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)」を参照してください。
  
## <a name="the-shutdown-method"></a>_ShutDown メソッド

`_Shutdown` メソッドは、フォームを閉じるときに呼び出される最後のメソッドです。フォームで使用するコンポーネントの後処理に必要なコードは、このメソッドに記述できます。 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a>初期化コードと後処理コードの例

次の例では、 `_Startup` メソッドで Microsoft SQL Server データベースへの接続を初期化し、  `_Shutdown` メソッドでその接続を閉じる方法を示します。この例が正常に動作するには、最初に、[ **プロジェクト**] メニューの [ **参照の追加**] をクリックし、[ **.NET**] タブで System.Data.dll コンポーネントを選択して, .NET Framework の System.Data アセンブリへの参照を設定する必要があります。また、キーストロークを少なくするために、フォーム コード ファイルの先頭に  `using System.Data.SqlClient` (または  `Imports System.Data.SqlClient)`) ディレクティブが追加されたことにも注意してください。 
  
> [!NOTE]
> InfoPath フォームに SQL Server データベースに接続するフォーム コードが含まれている場合、フォームの展開方法およびセキュリティ ポリシーの定義方法によっては、ユーザーにセキュリティのアクセス許可が必要になることがあります。 セキュリティの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」および「[コードを含むフォーム テンプレートのセキュリティ設定を構成する方法](how-to-configure-security-settings-for-form-templates-with-code.md)」を参照してください。 
  
```cs
using System;
using System.Data.SqlClient;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
    public partial class Template1
    {
        private XDocument    thisXDocument;
        private Application    thisApplication;
        private SqlConnection sqlConnect;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // Initialize variable for SQL Server connection.
            sqlConnect= new SqlConnection("server=localhost;Trusted_Connection=yes;database=Northwind");
        }
        public void _Shutdown()
        {
            // Close SQL Server connection at shut down.
            sqlConnect.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Data.SqlClient
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
        ' The namespace prefixes defined in this attribute must remain synchronized with
        ' those in the form definition file (.xsf).
        <InfoPathNamespace( _
            "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
        Public Class Template1
            Private thisXDocument As XDocument
            Private thisApplication As Application
            Private sqlConnect As SqlConnection
            Public Sub _Startup(app As Application, doc As XDocument)
                thisXDocument = doc
                thisApplication = app
                ' Initialize variable for SQL Server connection.
                sqlConnect = New SqlConnection _("server=localhost;Trusted_Connection=yes;database=Northwind")
            End Sub
        Public Sub _Shutdown()
            ' Close SQL Server connection.
            sqlConnect.Close()
        End Sub
    End Class
End Namespace
```

## <a name="see-also"></a>関連項目



[InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加する](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

