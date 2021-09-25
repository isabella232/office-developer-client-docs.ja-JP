---
title: InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using msxml5,MSXML5 [InfoPath 2007],MSXML5 script [InfoPath 2007],InfoPath 2007, using MSXML5
ms.localizationpriority: medium
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレート プロジェクトは、内部で Microsoft XML Core Services (MSXML) を使用して XML を操作します。マネージ コードでは、多くの場合, .NET Framework クラス ライブラリの System.Xml 名前空間によって提供される XML サポートを使用した方が簡単です。MSXML と System.Xml では、オブジェクトをネイティブで交換することはできません。したがって、InfoPath と他のマネージ コードとの間で XML データの受け渡しを行う際には、常に XML データの変換が必要になります。ここで説明する方法を使用すると、System.Xml オブジェクトの XML データを InfoPath フォーム コードと交換できます。
ms.openlocfilehash: 7fa559974a542aeb3472f6ef51ac6869a94cf6d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588372"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する

InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレート プロジェクトは、内部で Microsoft XML Core Services (MSXML) を使用して XML を操作します。マネージ コードでは、多くの場合, .NET Framework クラス ライブラリの **System.Xml** 名前空間によって提供される XML サポートを使用した方が簡単です。MSXML と **System.Xml** では、オブジェクトをネイティブで交換することはできません。したがって、InfoPath と他のマネージ コードとの間で XML データの受け渡しを行う際には、常に XML データの変換が必要になります。ここで説明する方法を使用すると、 **System.Xml** オブジェクトの XML データを InfoPath フォーム コードと交換できます。 
  
InfoPath 2003 オブジェクト モデルを使用するマネージ コード プロジェクトで **System.Xml** 名前空間のメンバーを使用するには、Visual Studio 2012 の [ **参照の追加**] ダイアログ ボックスの [ **.NET**] タブで、 **System.Xml** への参照を追加する必要があります。 
  
 **メモ**
  
- MSXML に関するリファレンス情報については、MSXML SDK を参照してください。
    
- [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によってラップされた MSXML オブジェクト モデルのメンバーをマネージ コード フォーム テンプレートのフォーム コードのデリゲートに割り当てることはできません。 
    
- [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーによって提供されるオブジェクト モデルを使用するようにフォーム テンプレートのコードを更新すると、 **System.Xml** がネイティブで使用されます。ただし、その場合は、すべてのコードを新しいオブジェクト モデルを使用するように手動で変換する必要があります。フォーム テンプレートを新しいオブジェクト モデルを使用するように変換するには、[ **フォームのオプション**] ダイアログ ボックスの [ **プログラミング**] カテゴリで [ **オブジェクト モデルのアップグレード**] をクリックします。
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a>System.Xml から XML Document Object Model (DOM) 全体を読み込む

次のコード例は、InfoPath の **CreateDOM** メソッドと、 [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) 名前空間のメンバーによってラップされた Microsoft XML Core Services のメンバーを使用して、 [System.Xml](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) のコードから XML DOM 全体を読み込む方法を示しています。 
  
この例では、フォーム コード モジュールの宣言セクションに **System.Xml** の **using** ディレクティブまたは **Imports** ディレクティブが必要です。また、 **XmlDocument** クラスの **Load** メソッドには **System.Security.Permissions.FileIOPermission** が必要なため、[ **フォームのオプション**] ダイアログ ボックスの [ **セキュリティと信頼**] カテゴリを使用して、フォーム テンプレートのセキュリティ レベルを [ **完全信頼**] として構成する必要があります。 
  
```cs
// Create a System.Xml XmlDocument and load an XML file.
XmlDocument doc = new XmlDocument();
doc.Load("c:\\temp\\MyFile.xml");
// Create an MSXML DOM object.
IXMLDOMDocument newDoc = thisXDocument.CreateDOM();
// Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml);
```

```vb
' Create a System.Xml XmlDocument and load an XML file.
Dim doc As XmlDocument = New XmlDocument()
doc.Load("c:\temp\MyFile.xml");
' Create an MSXML DOM object.
Dim newDoc As IXMLDOMDocument = thisXDocument.CreateDOM()
' Load the DOM with the XML from the System.XML object.
newDoc.loadXML(doc.DocumentElement.OuterXml)
```

## <a name="loading-a-single-node-from-systemxml"></a>System.Xml から 1 つのノードを読み込む

次のコード例の関数は、ラップされた MSXML **createNode** メソッドを使用して **System.Xml**. **XmlElement** の 1 つのノードを複製する方法を示しています。 
  
この例では、フォーム コード モジュールの宣言セクションに **System.Xml** の **using** ディレクティブまたは **Imports** ディレクティブが必要です。 
  
```cs
// This function takes a System.Xml XmlElement object and 
// an MSXML IXMLDOMDocument object, and returns an MSXML 
// IXMLDOMNode object that is a copy of the XmlElement object.
public IXMLDOMNode CloneSystemXmlElementToMsxml(
   XmlElement systemXmlElement, IXMLDOMDocument msxmlDocument)
{
   IXMLDOMNode msxmlResultNode;
   // Create a new element from the MSXML DOM using the same 
   // namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(
      DOMNodeType.NODE_ELEMENT, 
      systemXmlElement.Name, 
      systemXmlElement.NamespaceURI);
   // Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString();
   return msxmlResultNode;
}
```

```vb
' This function takes a System.Xml XmlElement object and 
' an MSXML IXMLDOMDocument object, and returns an MSXML 
' IXMLDOMNode object that is a copy of the XmlElement object.
Public Function CloneSystemXmlElementToMsxml(_
   XmlElement systemXmlElement, _
   IXMLDOMDocument msxmlDocument) As IXMLDOMNode
   Dim msxmlResultNode As IXMLDOMNode
   ' Create a new element from the MSXML DOM using the same 
   ' namespace as the XmlElement.
   msxmlResultNode = msxmlDocument.createNode(_
      DOMNodeType.NODE_ELEMENT, _
      systemXmlElement.Name, _
      systemXmlElement.NamespaceURI)
   ' Set the element's value.
   msxmlResultNode.text = systemXmlElement.Value.ToString()
   Return msxmlResultNode
End Function
```


