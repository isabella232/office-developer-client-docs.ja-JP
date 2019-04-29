---
title: InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using msxml5,MSXML5 [InfoPath 2007],MSXML5 script [InfoPath 2007],InfoPath 2007, using MSXML5
localization_priority: Normal
ms.assetid: f7a0cac5-26f9-49ed-b52c-0240ef0c9d38
description: InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレート プロジェクトは、内部で Microsoft XML Core Services (MSXML) を使用して XML を操作します。マネージ コードでは、多くの場合, .NET Framework クラス ライブラリの System.Xml 名前空間によって提供される XML サポートを使用した方が簡単です。MSXML と System.Xml では、オブジェクトをネイティブで交換することはできません。したがって、InfoPath と他のマネージ コードとの間で XML データの受け渡しを行う際には、常に XML データの変換が必要になります。ここで説明する方法を使用すると、System.Xml オブジェクトの XML データを InfoPath フォーム コードと交換できます。
ms.openlocfilehash: c56939a0cf03b5de6466de37013e154529afd1ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437400"
---
# <a name="working-with-msxml-and-systemxml-using-the-infopath-2003-object-model"></a><span data-ttu-id="cb1ec-107">InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する</span><span class="sxs-lookup"><span data-stu-id="cb1ec-107">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="cb1ec-p102">InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレート プロジェクトは、内部で Microsoft XML Core Services (MSXML) を使用して XML を操作します。マネージ コードでは、多くの場合, .NET Framework クラス ライブラリの **System.Xml** 名前空間によって提供される XML サポートを使用した方が簡単です。MSXML と **System.Xml** では、オブジェクトをネイティブで交換することはできません。したがって、InfoPath と他のマネージ コードとの間で XML データの受け渡しを行う際には、常に XML データの変換が必要になります。ここで説明する方法を使用すると、 **System.Xml** オブジェクトの XML データを InfoPath フォーム コードと交換できます。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-p102">Form template projects that work with the InfoPath 2003 object model use Microsoft XML Core Services (MSXML) internally to work with XML. In managed code, it is often easier to use the XML support provided by the **System.Xml** namespace in the .NET Framework class library. MSXML and **System.Xml** cannot exchange objects natively, so whenever you need to pass XML data between InfoPath and other managed code, XML data needs to be converted. You can exchange XML data from **System.Xml** objects with InfoPath form code by using the techniques in this topic.</span></span> 
  
<span data-ttu-id="cb1ec-112">InfoPath 2003 オブジェクト モデルを使用するマネージ コード プロジェクトで **System.Xml** 名前空間のメンバーを使用するには、Visual Studio 2012 の [ **参照の追加**] ダイアログ ボックスの [ **.NET**] タブで、 **System.Xml** への参照を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-112">To use members of the **System.Xml** namespace in a managed code project that uses the InfoPath 2003 object model, you must add a reference to **System.Xml** on the **.NET** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> 
  
 <span data-ttu-id="cb1ec-113">**メモ**</span><span class="sxs-lookup"><span data-stu-id="cb1ec-113">**Notes**</span></span>
  
- <span data-ttu-id="cb1ec-114">MSXML に関するリファレンス情報については、MSXML SDK を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-114">To view reference information about MSXML, see the MSXML SDK.</span></span>
    
- <span data-ttu-id="cb1ec-115">[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によってラップされた MSXML オブジェクト モデルのメンバーをマネージ コード フォーム テンプレートのフォーム コードのデリゲートに割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-115">Members of the MSXML object model that are wrapped by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace cannot be assigned to delegates in the form code of managed-code form templates.</span></span> 
    
- <span data-ttu-id="cb1ec-p103">[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーによって提供されるオブジェクト モデルを使用するようにフォーム テンプレートのコードを更新すると、 **System.Xml** がネイティブで使用されます。ただし、その場合は、すべてのコードを新しいオブジェクト モデルを使用するように手動で変換する必要があります。フォーム テンプレートを新しいオブジェクト モデルを使用するように変換するには、[ **フォームのオプション**] ダイアログ ボックスの [ **プログラミング**] カテゴリで [ **オブジェクト モデルのアップグレード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-p103">If you update the code of your form template to use the object model provided by members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace, **System.Xml** is used natively. However, when doing so, you must manually convert all of your code to use the new object model. To convert your form template to use the new object model, in the **Programming** category of the **Form Options** dialog box, click **Upgrade OM**.</span></span>
    
## <a name="loading-an-entire-xml-document-object-model-dom-from-systemxml"></a><span data-ttu-id="cb1ec-119">System.Xml から XML Document Object Model (DOM) 全体を読み込む</span><span class="sxs-lookup"><span data-stu-id="cb1ec-119">Loading an Entire XML Document Object Model (DOM) from System.Xml</span></span>

<span data-ttu-id="cb1ec-120">次のコード例は、InfoPath の **CreateDOM** メソッドと、 [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) 名前空間のメンバーによってラップされた Microsoft XML Core Services のメンバーを使用して、 [System.Xml](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) のコードから XML DOM 全体を読み込む方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-120">The following code sample demonstrates how to load an entire XML DOM from **System.Xml** code using the InfoPath [CreateDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.CreateDOM.aspx) method and the members of Microsoft XML Core Services that are wrapped by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
<span data-ttu-id="cb1ec-p104">この例では、フォーム コード モジュールの宣言セクションに **System.Xml** の **using** ディレクティブまたは **Imports** ディレクティブが必要です。また、 **XmlDocument** クラスの **Load** メソッドには **System.Security.Permissions.FileIOPermission** が必要なため、[ **フォームのオプション**] ダイアログ ボックスの [ **セキュリティと信頼**] カテゴリを使用して、フォーム テンプレートのセキュリティ レベルを [ **完全信頼**] として構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-p104">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module. Additionally, because the **Load** method of the **XmlDocument** class requires **System.Security.Permissions.FileIOPermission**, you must configure the security level of the form template as **Full Trust** using the **Security and Trust** category of the **Form Options** dialog box.</span></span> 
  
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

## <a name="loading-a-single-node-from-systemxml"></a><span data-ttu-id="cb1ec-123">System.Xml から 1 つのノードを読み込む</span><span class="sxs-lookup"><span data-stu-id="cb1ec-123">Loading a Single Node from System.Xml</span></span>

<span data-ttu-id="cb1ec-p105">次のコード例の関数は、ラップされた MSXML **createNode** メソッドを使用して **System.Xml**. **XmlElement** の 1 つのノードを複製する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-p105">The following code sample shows a function that demonstrates how to clone a single node from a **System.Xml**. **XmlElement** using the wrapped MSXML **createNode** method.</span></span> 
  
<span data-ttu-id="cb1ec-126">この例では、フォーム コード モジュールの宣言セクションに **System.Xml** の **using** ディレクティブまたは **Imports** ディレクティブが必要です。</span><span class="sxs-lookup"><span data-stu-id="cb1ec-126">The following examples require a **using** or **Imports** directive for **System.Xml** in the declarations section of the form code module.</span></span> 
  
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


