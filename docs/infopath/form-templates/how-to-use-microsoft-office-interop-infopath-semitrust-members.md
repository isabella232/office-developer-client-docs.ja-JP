---
title: Microsoft.Office.Interop.InfoPath.SemiTrust メンバーは InfoPath と互換性がありませんを使用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using infopath 2007 features
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間によって提供されるオブジェクト モデルには、オブジェクトと、Office InfoPath 2007 と InfoPath に追加された新しい機能を提供するメンバーが含まれています。
ms.openlocfilehash: 3d0e9b450dab6a821af1f698d9859b21e85abf81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799123"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Microsoft.Office.Interop.InfoPath.SemiTrust メンバーは InfoPath と互換性がありませんを使用します。

Microsoft Office InfoPath 2003 Toolkit を使用して作成されたフォーム テンプレートにコードを追加または、InfoPath 2003 と互換性のあるオブジェクト モデル (InfoPath 2003 オブジェクト[を使用してフォーム テンプレートの作成で説明したように動作する新しいフォーム テンプレートを作成するとモデル](how-to-create-a-form-template-using-the-infopath-2003-object-model.md))、既定では、Microsoft InfoPath は、オブジェクトのサブセットを使用し、メンバーと同じものに使用されている InfoPath 2003 で[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供されます。 これは、InfoPath 2003 との互換性を維持するための措置です。 しかし、 [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によって提供されるオブジェクト モデルには、Office InfoPath 2007 および InfoPath で追加された新機能を提供する追加のオブジェクトやメンバーも含まれています。 
  
たとえば、[PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) インターフェイスと [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) インターフェイスによって提供される新機能である Information Rights Management は、InfoPath 2003 では使用できません。この新機能や、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間に追加されたその他の新しいオブジェクトは、InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートを開いたり作成したりした場合に既定では使用できません。 
  
同様に、[_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) インターフェイスが InfoPath 2003 と同じ機能を提供するのに対し、 [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) インターフェイスは、Office InfoPath 2007 で追加されたプロパティやメソッドを含むようにバージョンアップされ、 [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) は、InfoPath で追加されたプロパティやメソッドを含むようにバージョンアップされています。 
  
**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを使用して作成したフォーム テンプレート プロジェクトで、Office InfoPath 2007 または InfoPath で追加されたオブジェクトやメンバーを使用することもできますが、それらのメンバーを使用するコードでは、InfoPath 2003 との互換性が失われます。 
  
> [!NOTE]
> [!メモ] **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供されるオブジェクト モデルを使用して作成したビジネス ロジックを含むすべてのフォーム テンプレートは、InfoPath と互換性のあるオブジェクトやメンバーを使用しているかどうかに関係なく、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 に展開されたブラウザー対応のフォーム テンプレートではサポートされません。ブラウザー対応フォーム テンプレートのビジネス ロジックでは、 [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される新しい InfoPath マネージ コード オブジェクト モデルを使用する必要があります。 
  
## <a name="example"></a>例

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>新しいオブジェクト モデルのメンバーにアクセスするための XDocument オブジェクト変数または Application オブジェクト変数を作成する

**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間で使用できる新しいオブジェクトやメンバーにアクセスするには、オブジェクト変数を宣言して、それらのメンバーを実装する正しいバージョンのインターフェイスにキャストする必要があります。既定では、  `thisXDocument` 変数と  `thisApplication` 変数は、対応する **_XDocument2** インターフェイスと [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) インターフェイスの InfoPath 2003 互換バージョンにアクセスします。新機能へのアクセスを提供する **_XDocument3** インターフェイスと [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) インターフェイスにアクセスするには、 **_XDocument3** 型または **_Application3** 型のオブジェクト変数を宣言し、  `thisXDocument` 変数または  `thisApplication` 変数によって返されるオブジェクトを同じ型にキャストする必要があります。以下に例を示します。 
  
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

新しいバージョンの _ **XDocument3** 型または **_Application3** 型の変数を作成したら、それを使用して、InfoPath の新機能を提供するオブジェクトやメンバーにアクセスできます。 
  
次の例は、_ **XDocument3** 型のオブジェクト変数を [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) アクセサー プロパティと共に使用して、新しい **Permission** インターフェイスとその [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) プロパティにアクセスする方法を示しています。これにより、フォームでアクセス許可の設定が有効になっているかどうかを確認できます。 
  
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
  
たとえば、[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) オブジェクトでは、バージョン付きの [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) オブジェクトを使用しないと利用できない 2 つの新しいプロパティ [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) および [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) にはアクセスできません。 
  
これらのプロパティにアクセスするには、 **ViewInfo2** 型のオブジェクト変数を宣言し、_ [XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) オブジェクト変数の **ViewInfos** プロパティによって返されるオブジェクトを **ViewInfo2** 型にキャストする必要があります。以下に例を示します。 
  
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


