---
title: Microsoft を使用します。Office.Interop.InfoPath.SemiTrust メンバーは InfoPath と互換性がありません
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007 機能を使用した infopath 2003 互換フォーム テンプレート
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Microsoft によって提供されるオブジェクト モデル。Office.Interop.InfoPath.SemiTrust 名前空間には、Office InfoPath 2007 および InfoPath に追加された新しい機能を提供するオブジェクトとメンバーが含まれています。
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415342"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="c57a1-104">Microsoft を使用します。Office.Interop.InfoPath.SemiTrust メンバーは InfoPath と互換性がありません</span><span class="sxs-lookup"><span data-stu-id="c57a1-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="c57a1-105">Microsoft Office InfoPath 2003 Toolkit で作成されたフォーム テンプレートにコードを追加するか、InfoPath 2003 互換オブジェクト モデルで動作する新しいフォーム テンプレートを作成する場合[(「InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用してフォーム テンプレートを作成する」の説明に従って)、既定で、 Microsoft InfoPath は、InfoPath 2003 で使用されるオブジェクトとメンバーのサブセットを[使用します。Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="c57a1-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="c57a1-106">これは、InfoPath 2003 との互換性を維持するための措置です。</span><span class="sxs-lookup"><span data-stu-id="c57a1-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="c57a1-107">ただし[、Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供されるオブジェクト モデルには、Office InfoPath 2007 および InfoPath に追加された新しい機能を提供する追加のオブジェクトとメンバーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c57a1-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="c57a1-108">たとえば [、PermissionObject インターフェイスと](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) インターフェイスは、InfoPath 2003 では使用できない新しい情報権限管理機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="c57a1-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="c57a1-109">この新機能や、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間に追加されたその他の新しいオブジェクトは、InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートを開いたり作成したりした場合に既定では使用できません。</span><span class="sxs-lookup"><span data-stu-id="c57a1-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="c57a1-110">同様に[、_XDocument2インターフェイス](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx)は InfoPath 2003 と同じ機能を提供します。[_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx)インターフェイスは、Office InfoPath 2007 で追加された追加のプロパティとメソッドを含むバージョン管理を行い[、_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx)は InfoPath に追加された追加のプロパティとメソッドを含むバージョン管理されています。</span><span class="sxs-lookup"><span data-stu-id="c57a1-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="c57a1-111">**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを使用して作成されたフォーム テンプレート プロジェクトで Office InfoPath 2007 または InfoPath で追加されたオブジェクトとメンバーを使用する場合は、使用できますが、これらのメンバーを使用するコードは InfoPath 2003 と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="c57a1-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c57a1-112">**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを使用して作成されたビジネス ロジックを持つすべてのフォーム テンプレートは、InfoPath と互換性のあるオブジェクトとメンバーを使用するかどうかに関係無く、InfoPath Forms Services で Microsoft SharePoint Server 2010 に展開されたブラウザー対応フォーム テンプレートではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="c57a1-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="c57a1-113">ブラウザーが有効なフォーム テンプレートのビジネス ロジックでは、Microsoft.Office によって提供される新しい InfoPath マネージ コード オブジェクト モデル[を使用する必要があります。InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)名前空間。</span><span class="sxs-lookup"><span data-stu-id="c57a1-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c57a1-114">例</span><span class="sxs-lookup"><span data-stu-id="c57a1-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="c57a1-115">新しいオブジェクト モデルのメンバーにアクセスするための XDocument オブジェクト変数または Application オブジェクト変数を作成する</span><span class="sxs-lookup"><span data-stu-id="c57a1-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="c57a1-116">**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間で使用できる新しいオブジェクトとメンバーにアクセスするには、オブジェクト変数を宣言し、これらのメンバーを実装するインターフェイスの正しいバージョンにキャストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c57a1-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="c57a1-117">既定では、 `thisXDocument` 変数 `thisApplication` は InfoPath 2003[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx)互換のバージョンの対応するインターフェイスおよび _XDocument2インターフェイス_Application2します。</span><span class="sxs-lookup"><span data-stu-id="c57a1-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="c57a1-118">新しい機能へのアクセスを提供する **_XDocument3** インターフェイスと [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx)インターフェイスにアクセスするには **、_XDocument3** または **_Application3** 型のオブジェクト変数を宣言し、次の例に示すように、変数または変数によって返されるオブジェクトを同じ型にキャストする必要があります。 `thisXDocument` `thisApplication`</span><span class="sxs-lookup"><span data-stu-id="c57a1-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

```cs
// Declare an object variable of type _Application3 and
// cast the object returned by the thisApplication variable to
// the same type.
_Application3 thisApplication3 = (_Application3)thisXDocument;
```

```vb
' Declare an object variable of type _Application3 and
' cast the object returned by the thisXApplication variable to
' the same type.
Dim thisDocument As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="c57a1-119">XDocument オブジェクト変数または Application オブジェクト変数からアクセサー プロパティを使用して新しいオブジェクトにアクセスする</span><span class="sxs-lookup"><span data-stu-id="c57a1-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="c57a1-120">後のバージョン _ **XDocument3** または **_Application3** 型の変数を作成したら、それを使用して、新しい InfoPath 機能を提供するオブジェクトまたはメンバーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c57a1-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="c57a1-121">次の例は、新しい **Permission** インターフェイスとその [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx)プロパティにアクセスするために [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx)アクセサー プロパティと一緒に型 _ **XDocument3** のオブジェクト変数を使用して、フォームに対してアクセス許可設定が有効になっているかどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c57a1-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Use the object variable to access the later version object and
// property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Use the object variable to access the later version object and
' property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString())
```

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="c57a1-122">バージョン付きのオブジェクトにアクセスしてバージョン付きの型にキャストする</span><span class="sxs-lookup"><span data-stu-id="c57a1-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="c57a1-123">InfoPath 2003 オブジェクト モデルに存在していたオブジェクトに新しいプロパティやメソッドが追加された場合、それらの新しいメンバーを実装するオブジェクトにはバージョン付きの名前が付きます。</span><span class="sxs-lookup"><span data-stu-id="c57a1-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="c57a1-124">たとえば [、ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) オブジェクトは、バージョン管理された [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) オブジェクトを使用する場合にのみ使用できる 2 つの新しいプロパティ [(Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) プロパティと [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) プロパティ) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="c57a1-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="c57a1-125">これらのプロパティにアクセスするには、次の例に示すように **、ViewInfo2** 型のオブジェクト変数を宣言し、_ **XDocument3** オブジェクト変数の [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx)プロパティによって返されるオブジェクトを **ViewInfo2** 型にキャストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c57a1-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Declare an object variable of type ViewInfo2 and cast the object 
// returned by the ViewInfos property to that type.
ViewInfo2 thisView = (ViewInfo2)thisXDocument3.ViewInfos["View2"];
// Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Declare an object variable of type ViewInfo2 and cast the object 
' returned by the ViewInfos property to that type.
Dim thisView As ViewInfo2 = _
   DirectCast(thisXDocument3.ViewInfos("View2"), ViewInfo2)
' Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString())
```


