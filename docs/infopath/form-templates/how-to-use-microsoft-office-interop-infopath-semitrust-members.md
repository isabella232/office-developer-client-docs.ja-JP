---
title: infopath と互換性のない SemiTrust メンバーを使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003 互換フォームテンプレート、infopath 2007 機能を使用
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: SemiTrust 名前空間によって提供されるオブジェクトモデルには、Office InfoPath 2007 および infopath に追加された新しい機能を提供するオブジェクトとメンバーが含まれています。
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300085"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>infopath と互換性のない SemiTrust メンバーを使用する

Microsoft Office InfoPath 2003 Toolkit を使用して作成されたフォームテンプレートにコードを追加するか、または infopath 2003 互換オブジェクトモデルで動作する新しいフォームテンプレートを作成する場合 (「 [infopath 2003 オブジェクトを使用してフォームテンプレートを作成する」を参照してください)Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md))、既定では、microsoft infopath では、infopath 2003 で使用されるものと同じである、 [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供されるオブジェクトとメンバーのサブセットが使用されます。 これは、InfoPath 2003 との互換性を維持するための措置です。 ただし、 [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供されるオブジェクトモデルには、Office InfoPath 2007 および infopath に追加された新しい機能を提供する追加のオブジェクトとメンバーが含まれています。 
  
たとえば、 [permissionobject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx)および[Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx)インターフェイスは、InfoPath 2003 では使用できない新しい information rights management 機能を提供します。 この新機能や、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間に追加されたその他の新しいオブジェクトは、InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートを開いたり作成したりした場合に既定では使用できません。 
  
同様に、 [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx)インターフェイスは InfoPath 2003 と同じ機能を提供します。[_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx)インターフェイスは、Office InfoPath 2007 で追加されたプロパティとメソッドが追加され、infopath で追加されたプロパティとメソッドを追加するために[_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx)がバージョン管理されています。. 
  
**SemiTrust**名前空間によって提供されるオブジェクトモデルを使用して作成されたフォームテンプレートプロジェクトで、Office InfoPath 2007 または infopath で追加されたオブジェクトとメンバーを使用する場合は、次のコードを使用します。これらのメンバーは、InfoPath 2003 と互換性がありません。 
  
> [!NOTE]
> **SemiTrust**名前空間によって提供されるオブジェクトモデルを使用して作成されたビジネスロジックを持つすべてのフォームテンプレートは、オブジェクトと InfoPath と互換性のあるメンバーを使用しているかどうかにかかわらず、InfoPath Forms Services を使用して Microsoft SharePoint Server 2010 に展開されたブラウザー対応のフォームテンプレート。 ブラウザー対応のフォームテンプレートのビジネスロジックでは、 [Microsoft Office infopath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)名前空間で提供される新しい infopath マネージコードオブジェクトモデルを使用する必要があります。 
  
## <a name="example"></a>例

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>新しいオブジェクト モデルのメンバーにアクセスするための XDocument オブジェクト変数または Application オブジェクト変数を作成する

**SemiTrust**名前空間で使用可能な新しいオブジェクトおよびメンバーにアクセスするには、これらのメンバーを実装するインターフェイスの正しいバージョンにオブジェクト変数を宣言し、キャストする必要があります。 既定では、 `thisXDocument`および`thisApplication`変数は、対応する **_XDocument2**および[アプリケーション 2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx)インターフェイスの InfoPath 2003 互換バージョンにアクセスします。 新しい機能へのアクセスを提供する **_XDocument3**および[application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx)のインターフェイスにアクセスするには、 **_XDocument3**または**アプリケーション**の種類のオブジェクト変数を宣言してから、次のようにして`thisXDocument`また`thisApplication`は、次の例に示すように、同じ型に変数を使用します。 
  
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

後のバージョンの**XDocument3**または**application3**タイプの変数を作成した後、それを使用して、新しい InfoPath 機能を提供するオブジェクトまたはメンバーにアクセスできます。 
  
次の例は、permission アクセサープロパティを指定して、_ **XDocument3**型[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx)のオブジェクト変数を使用して、アクセス許可の設定が新しい**アクセス許可**インターフェイスおよび[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx)プロパティにアクセスする方法を示しています。フォームに対して有効になります。 
  
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
  
たとえば、次のように、バージョン付きの[ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx)オブジェクトを使用している場合にのみ使用可能な2つの新しいプロパティ ( [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx)および[hidename](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx)プロパティ) へのアクセスは、 [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx)オブジェクトでは提供されません。 
  
これらのプロパティにアクセスするには、 **ViewInfo2**型のオブジェクト変数を宣言し、次に示すように、_ **XDocument3**オブジェクト変数の[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx)プロパティによって返されるオブジェクトを**ViewInfo2**型にキャストする必要があります。例. 
  
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


