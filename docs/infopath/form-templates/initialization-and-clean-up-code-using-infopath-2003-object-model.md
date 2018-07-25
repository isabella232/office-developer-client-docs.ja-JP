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
ms.openlocfilehash: 7111a8525b092998e21d4c267b5884f50fdb9777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799135"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a><span data-ttu-id="50e92-108">InfoPath 2003 オブジェクト モデルを使用する初期化コードと後処理コード</span><span class="sxs-lookup"><span data-stu-id="50e92-108">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>

<span data-ttu-id="50e92-p102">既定では、InfoPath 2003 と互換性のあるフォーム テンプレート プロジェクトについて作成される FormCode.cs または FormCode.vb ファイルには、フォームのプログラム ロジックに対するすべてのソース コードが含まれています。プロジェクトのテンプレートによって FormCode.cs または FormCode.vb ファイルに以下の例とよく似たクラスが生成され、このクラスには、フォーム イベントのハンドラーだけでなく、初期化コードと後処理コードも定義できます。FormCode.cs および FormCode.vb ファイルは、イベント ハンドラーが実装される唯一のクラスとしてこのクラスを識別する、アセンブリ レベルの **System.ComponentModel.DescriptionAttribute** 属性を使用します。 **InfoPathNamespace** 属性 ( [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) 型が実装する) をクラスに適用して、クラス内で使用する XML DOM セレクション名前空間を識別します。 **InfoPathNamespace** で参照される名前空間は、InfoPath プロジェクト システムによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="50e92-p102">By default, the FormCode.cs or FormCode.vb file that is created for a form template project that is compatible with InfoPath 2003 contains all the source code for the programming logic of the form. The template for the project generates a class in the FormCode.cs or FormCode.vb file much like the classes in the following examples where you can define initialization and clean-up code, as well as handlers for form events. The FormCode.cs and FormCode.vb files apply an assembly-level **System.ComponentModel.DescriptionAttribute** attribute, which identifies the class as the only class where event handlers are implemented. The **InfoPathNamespace** attribute (which is implemented by the [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) type) is applied to a class to identify the XML DOM selection namespaces used within the class. The namespaces referenced in the **InfoPathNamespace** are maintained by the InfoPath project system.</span></span> 
  
<span data-ttu-id="50e92-114">FormCode クラス自体が、フォームが開いている間に InfoPath の標準的な機能に加えて必要となるコンポーネントに対して、初期化ルーチンと後処理ルーチンを実行するために使用する  `_Startup` および  `_Shutdown` メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="50e92-114">The FormCode class itself provides  `_Startup` and  `_Shutdown` methods that are used to perform initialization and clean-up routines for any components that are required in addition to standard InfoPath functionality while the form is open.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="50e92-p103">InfoPath オブジェクト モデルのメンバーは、 `_Startup` および  `_Shutdown` メソッド内から呼び出さないでください。これらのメソッドでは、外部コンポーネントのメンバーだけを初期化し、呼び出さなければなりません。</span><span class="sxs-lookup"><span data-stu-id="50e92-p103">Do not call members of the InfoPath object model from within the  `_Startup` and  `_Shutdown` methods. You should initialize and call only members of external components in these methods.</span></span> 
  
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

## <a name="the-startup-method"></a><span data-ttu-id="50e92-117">_Startup メソッド</span><span class="sxs-lookup"><span data-stu-id="50e92-117">The _Startup Method</span></span>

<span data-ttu-id="50e92-p104">追加コンポーネントの初期化コードを記述する場所を提供することに加え、 `_Startup` メソッドは、フォーム コードで InfoPath オブジェクト モデルの `thisXDocument` および `thisApplication` クラスのメンバーにアクセスするために使用できる  [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) および  [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) 変数を初期化します。この 2 つの変数を初期化するために必要なコードは、プロジェクト テンプレートによって自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="50e92-p104">In addition to providing a place to write initialization code for additional components, the  `_Startup` method initializes the  `thisXDocument` and  `thisApplication` variables that can be used in your form code to access the members of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) and [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes in the InfoPath object model. The code necessary to initialize the two variables is generated automatically by the project template.</span></span> 
  
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

<span data-ttu-id="50e92-120">次の例では、 `thisXDocument` 変数を使用して [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) 型の [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) メソッドにアクセスする、簡単なボタンのイベント ハンドラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="50e92-120">The following examples show a simple event handler for a button that uses the  `thisXDocument` variable to access the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) type.</span></span> 
  
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

<span data-ttu-id="50e92-121">イベント ハンドラーの作成方法については、「[InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加する方法](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50e92-121">For information on how to create an event handler, see [How to: Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="the-shutdown-method"></a><span data-ttu-id="50e92-122">_ShutDown メソッド</span><span class="sxs-lookup"><span data-stu-id="50e92-122">The _ShutDown Method</span></span>

<span data-ttu-id="50e92-p105">`_Shutdown` メソッドは、フォームを閉じるときに呼び出される最後のメソッドです。フォームで使用するコンポーネントの後処理に必要なコードは、このメソッドに記述できます。</span><span class="sxs-lookup"><span data-stu-id="50e92-p105">The  `_Shutdown` method is the last method called when a form is closed. You can write any code in this method that is needed to clean up or finalize components used in the form.</span></span> 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a><span data-ttu-id="50e92-125">初期化コードと後処理コードの例</span><span class="sxs-lookup"><span data-stu-id="50e92-125">Initialization and Clean-up Code Example</span></span>

<span data-ttu-id="50e92-p106">次の例では、 `_Startup` メソッドで Microsoft SQL Server データベースへの接続を初期化し、  `_Shutdown` メソッドでその接続を閉じる方法を示します。この例が正常に動作するには、最初に、[ **プロジェクト**] メニューの [ **参照の追加**] をクリックし、[ **.NET**] タブで System.Data.dll コンポーネントを選択して, .NET Framework の System.Data アセンブリへの参照を設定する必要があります。また、キーストロークを少なくするために、フォーム コード ファイルの先頭に  `using System.Data.SqlClient` (または  `Imports System.Data.SqlClient)`) ディレクティブが追加されたことにも注意してください。</span><span class="sxs-lookup"><span data-stu-id="50e92-p106">The following example shows how to initialize a connection to a Microsoft SQL Server database in the  `_Startup` method and close the connection in the  `_Shutdown` method. In order for this example to work correctly, you must first set a reference to the System.Data assembly of the .NET Framework by clicking **Add Reference** on the **Project** menu, and then selecting the System.Data.dll component on the **.NET** tab. Also note that the  `using System.Data.SqlClient` (or  `Imports System.Data.SqlClient)` directive was added at the top of the form code file to reduce keystrokes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="50e92-128">InfoPath フォームに SQL Server データベースに接続するフォーム コードが含まれている場合、フォームの展開方法およびセキュリティ ポリシーの定義方法によっては、ユーザーにセキュリティのアクセス許可が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="50e92-128">Users of an InfoPath form that contains form code that connects to a SQL Server database may require security permissions depending on how the form is deployed and security policy is defined.</span></span> <span data-ttu-id="50e92-129">セキュリティの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」および「[コードを含むフォーム テンプレートのセキュリティ設定を構成する方法](how-to-configure-security-settings-for-form-templates-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50e92-129">For more information on security see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md) and [How to: Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md).</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="50e92-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="50e92-130">See also</span></span>



[<span data-ttu-id="50e92-131">InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="50e92-131">How to: Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

