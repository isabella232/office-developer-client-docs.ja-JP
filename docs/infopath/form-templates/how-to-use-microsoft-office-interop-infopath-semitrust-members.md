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
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Microsoft を使用します。Office.Interop.InfoPath.SemiTrust メンバーは InfoPath と互換性がありません

Microsoft Office InfoPath 2003 Toolkit で作成されたフォーム テンプレートにコードを追加するか、InfoPath 2003 互換オブジェクト モデルで動作する新しいフォーム テンプレートを作成する場合[(「InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用してフォーム テンプレートを作成する」の説明に従って)、既定で、 Microsoft InfoPath は、InfoPath 2003 で使用されるオブジェクトとメンバーのサブセットを[使用します。Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供されます。 これは、InfoPath 2003 との互換性を維持するための措置です。 ただし[、Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供されるオブジェクト モデルには、Office InfoPath 2007 および InfoPath に追加された新しい機能を提供する追加のオブジェクトとメンバーが含まれています。 
  
たとえば [、PermissionObject インターフェイスと](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) インターフェイスは、InfoPath 2003 では使用できない新しい情報権限管理機能を提供します。 この新機能や、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間に追加されたその他の新しいオブジェクトは、InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートを開いたり作成したりした場合に既定では使用できません。 
  
同様に[、_XDocument2インターフェイス](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx)は InfoPath 2003 と同じ機能を提供します。[_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx)インターフェイスは、Office InfoPath 2007 で追加された追加のプロパティとメソッドを含むバージョン管理を行い[、_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx)は InfoPath に追加された追加のプロパティとメソッドを含むバージョン管理されています。 
  
**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを使用して作成されたフォーム テンプレート プロジェクトで Office InfoPath 2007 または InfoPath で追加されたオブジェクトとメンバーを使用する場合は、使用できますが、これらのメンバーを使用するコードは InfoPath 2003 と互換性がありません。 
  
> [!NOTE]
> **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを使用して作成されたビジネス ロジックを持つすべてのフォーム テンプレートは、InfoPath と互換性のあるオブジェクトとメンバーを使用するかどうかに関係無く、InfoPath Forms Services で Microsoft SharePoint Server 2010 に展開されたブラウザー対応フォーム テンプレートではサポートされません。 ブラウザーが有効なフォーム テンプレートのビジネス ロジックでは、Microsoft.Office によって提供される新しい InfoPath マネージ コード オブジェクト モデル[を使用する必要があります。InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)名前空間。 
  
## <a name="example"></a>例

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>新しいオブジェクト モデルのメンバーにアクセスするための XDocument オブジェクト変数または Application オブジェクト変数を作成する

**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間で使用できる新しいオブジェクトとメンバーにアクセスするには、オブジェクト変数を宣言し、これらのメンバーを実装するインターフェイスの正しいバージョンにキャストする必要があります。 既定では、 `thisXDocument` 変数 `thisApplication` は InfoPath 2003[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx)互換のバージョンの対応するインターフェイスおよび _XDocument2インターフェイス_Application2します。 新しい機能へのアクセスを提供する **_XDocument3** インターフェイスと [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx)インターフェイスにアクセスするには **、_XDocument3** または **_Application3** 型のオブジェクト変数を宣言し、次の例に示すように、変数または変数によって返されるオブジェクトを同じ型にキャストする必要があります。 `thisXDocument` `thisApplication` 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a>XDocument オブジェクト変数または Application オブジェクト変数からアクセサー プロパティを使用して新しいオブジェクトにアクセスする

後のバージョン _ **XDocument3** または **_Application3** 型の変数を作成したら、それを使用して、新しい InfoPath 機能を提供するオブジェクトまたはメンバーにアクセスできます。 
  
次の例は、新しい **Permission** インターフェイスとその [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx)プロパティにアクセスするために [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx)アクセサー プロパティと一緒に型 _ **XDocument3** のオブジェクト変数を使用して、フォームに対してアクセス許可設定が有効になっているかどうかを判断する方法を示しています。 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a>バージョン付きのオブジェクトにアクセスしてバージョン付きの型にキャストする

InfoPath 2003 オブジェクト モデルに存在していたオブジェクトに新しいプロパティやメソッドが追加された場合、それらの新しいメンバーを実装するオブジェクトにはバージョン付きの名前が付きます。
  
たとえば [、ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) オブジェクトは、バージョン管理された [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) オブジェクトを使用する場合にのみ使用できる 2 つの新しいプロパティ [(Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) プロパティと [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) プロパティ) へのアクセスを提供します。 
  
これらのプロパティにアクセスするには、次の例に示すように **、ViewInfo2** 型のオブジェクト変数を宣言し、_ **XDocument3** オブジェクト変数の [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx)プロパティによって返されるオブジェクトを **ViewInfo2** 型にキャストする必要があります。 
  
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


