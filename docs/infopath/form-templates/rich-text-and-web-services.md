---
title: リッチ テキストと Web サービス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: Microsoft InfoPath では、フォーム内のリッチ テキスト ボックス コントロールを、Web サービスから受け取った XML 要素にバインドし、リッチ テキスト ボックス コントロールのデータを Web サービスを通じて XML 要素に送信することができます。要素は XHTML (Extensible HyperText Markup Language) 形式に従っている必要があります。たとえば、リッチ テキストが含まれている MyRichTextElement という名前の要素のスキーマであれば、XML スキーマ定義は次のようになります。
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299847"
---
# <a name="rich-text-and-web-services"></a><span data-ttu-id="17bfd-105">リッチ テキストと Web サービス</span><span class="sxs-lookup"><span data-stu-id="17bfd-105">Rich Text and Web Services</span></span>

<span data-ttu-id="17bfd-p102">Microsoft InfoPath では、フォーム内の **リッチ テキスト ボックス** コントロールを、Web サービスから受け取った XML 要素にバインドし、リッチ テキスト ボックス コントロールのデータを Web サービスを通じて XML 要素に送信することができます。要素は XHTML (Extensible HyperText Markup Language) 形式に従っている必要があります。たとえば、リッチ テキストが含まれている  `MyRichTextElement` という名前の要素のスキーマであれば、XML スキーマ定義は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p102">Microsoft InfoPath supports binding a **Rich Text Box** control in a form to an XML element that is received from a Web service, and submitting data from a rich text box control to an XML element through a Web service. The element must adhere to the Extensible HyperText Markup Language (XHTML) format. For example, the schema for an element named  `MyRichTextElement` that contains rich text would have the following XML schema definition:</span></span> 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

<span data-ttu-id="17bfd-p103">**リッチ テキスト ボックス** コントロールを XHTML 要素にバインドできるようにするには、あらかじめラッパー ノードを使用して要素をラップしておく必要があります。このラッパー ノードは任意の名前空間に属することができます。ラッパー ノードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p103">Before a **Rich Text Box** control can be bound with the XHTML element, the element should be wrapped with a wrapper node; this wrapper node can belong to any arbitrary namespace. The wrapper node can look like this:</span></span> 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

<span data-ttu-id="17bfd-p104">このトピックでは、XHTML を送受信できる Web サービスを作成する手順と、InfoPath を使用して Web サービス パラメーターにバインドする方法について、その概要を説明します。ここでは、こうした Web サービスを作成するための詳細な手順は説明しません。Web サービスの操作に関する一定の知識を前提としています。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p104">This topic outlines the process of creating a Web service that can send and receive XHTML, and how to use InfoPath to bind to the Web service parameters. This topic does not provide detailed instructions on how to create such a Web service. It is assumed that you already have some familiarity with working with Web services.</span></span>
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a><span data-ttu-id="17bfd-114">XHTML を送受信するように Web サービスを設計する方法</span><span class="sxs-lookup"><span data-stu-id="17bfd-114">How to Design a Web Service to Receive and Send XHTML</span></span>

<span data-ttu-id="17bfd-p105">XHTML データを格納し、サーバー上の XML ファイルで送受信する Web サービスの例を示します。このファイルは out.xml という名前で、XHTML データを格納するデータ ソースとして機能します。 `getXhtml` および  `setXhtml` という 2 つの Web メソッドがあり、クライアント アプリケーションが XHTML データ ソースとのインターフェイスに使用できるように公開されます。  `getXhtml` Web サービス メソッドは **XmlNode** を返します。これには XHTML が格納されており、InfoPath のリッチ テキスト ボックス コントロールにバインドできます。  `setXhtml` Web サービス メソッドは **XmlNode** をデータとして受け取り、out.xml ファイルに格納します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p105">The example Web service stores the XHTML data that it sends and receives in an XML file on the server. This file that is named out.xml, acts as a data source that stores the XHTML data. There are two Web methods that will be exposed to allow a client application to interface with the XHTML data source:  `getXhtml` and  `setXhtml`. The  `getXhtml` Web Service method returns an **XmlNode** that contains the XHTML that can be bound to an InfoPath rich text box control. The  `setXhtml` Web Service method accepts an **XmlNode** as the data to store in the out.xml file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="17bfd-120">[!メモ] これらの Web メソッドでは、 **System.IO** および **System.Xml** 名前空間を参照する **using** ステートメントが必要です。</span><span class="sxs-lookup"><span data-stu-id="17bfd-120">These Web methods require **using** statements that reference the **System.IO** and **System.Xml** namespaces.</span></span> 
  
<span data-ttu-id="17bfd-121">`getXhtml` Web サービス メソッドは、ドライブ C の Data フォルダーにある out.xml ファイルから返される XML データの読み込みを試みます。ファイルが見つからないか有効な XML が格納されていないために読み込みに失敗した場合は、XHTML 名前空間を参照する空の **DIV** HTML 要素を返します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-121">The  `getXhtml` Web Service method attempts to load the XML data to be returned from the out.xml file in the Data folder on drive C. If it fails, because the file is not found, or does not contain valid XML, the method will return an empty **DIV** HTML element that references the XHTML namespace.</span></span> 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "https://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "https://someNameSpace"); 
 
            // Temporary XmlDocument 
            XmlDocument tempDocument = new XmlDocument(); 
            try 
            { 
                // Read the saved rich text data from the local machine 
                tempDocument.Load(@"c:\Data\out.xml"); 
            } 
            catch (XmlException) 
            { 
                // If the file does not exist or content is not valid XML 
                tempDocument.LoadXml("<div xmlns=\"https://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

<span data-ttu-id="17bfd-p106">`setXhtml` Web サービス メソッドは、InfoPath フォーム上の **リッチ テキスト ボックス** コントロールから XHTML を受け取ります。Web サービスはノード リストには対応していないので、複数の行を含むリッチ テキスト フィールドが Web サービスに送られた場合、Web サービスは 1 行目のみを受け取り、残りは無視します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p106">The  `setXhtml` Web Service method accepts XHTML from a **Rich Text Box** control on an InfoPath form. Because Web services do not support a node list, when a rich text field that contains multiple lines is sent to a Web service, the Web service only accepts the first line and ignores the rest.</span></span> 
  
<span data-ttu-id="17bfd-p107">サンプルの  `setXhtml` メソッドは、最上位の XML ノードを受信することを前提としています。通常、最上位の XML ノードは **DIV** 要素にラップされます。 **リッチ テキスト ボックス** コントロール内のテキストの書式が設定されていないなどの理由で、受信した XML にラップ要素が含まれていない場合、このメソッドは、渡された XML がテキスト ノードであることが **NodeType** プロパティで示されているかどうかをチェックすることで、そのことを確かめます。XML がテキスト ノードの場合は、 **DIV** 要素を作成し、テキスト ノードの内容を **DIV** にコピーして、Web サービスから送られたテキストを持つ子のテキスト ノードが **DIV** に格納されるようにします。このメソッドが受信した XML はドライブ C の Data フォルダーにある out.xml ファイルに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p107">The sample  `setXhtml` method assumes that it will receive a top-level XML node, which in most cases will be wrapped in a **DIV** element. If the XML received does not contain a wrapping element, for example when text within the **Rich Text Box** control has no formatting, this method will detect this by checking whether the **NodeType** property indicates that the XML passed in is a text node. If the XML is a text node, the method creates a **DIV** element and copies the text node contents to the **DIV** so that the **DIV** contains a text node child with the text that was sent to the Web service. The XML received by this method is written to the out.xml file in the Data folder on the drive C.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="17bfd-p108">[!メモ] サンプルの  `setXhtml` メソッドは任意のサイズの XHTML データを受け取るように記述されていますが、実用上は、送信されるデータの大きさを必ず確かめ、送信できるデータの上限を設定してください。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p108">The sample  `setXhtml` method was written to accept XHTML data of any size. In actual practice, you should always check to see how much data is being submitted and set an upper limit for how much data that can be submitted.</span></span> 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the text to the DIV. 
                div.AppendChild(document.ImportNode(xn, true)); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            else 
            { 
                // Copy the node to our own XmlDocument 
                document.AppendChild(document.ImportNode(xn, true)); 
            } 
 
            // Save the file to the local machine 
            document.Save(@"c:\Data\out.xml"); 
}  

```

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a><span data-ttu-id="17bfd-130">サンプルの Web サービスとデータを交換する InfoPath フォームの作成方法</span><span class="sxs-lookup"><span data-stu-id="17bfd-130">How to Create an InfoPath Form That Exchanges Data with the Sample Web Service</span></span>

<span data-ttu-id="17bfd-131">サンプルの Web サービスをテストするフォームを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-131">Perform the following steps to create a form to test the sample Web service.</span></span>
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a><span data-ttu-id="17bfd-132">サンプルの Web サービスに接続するフォームを作成するには</span><span class="sxs-lookup"><span data-stu-id="17bfd-132">To create a form that connects to the sample Web service</span></span>

1. <span data-ttu-id="17bfd-133">InfoPath フォーム デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="17bfd-133">Open the InfoPath form designer.</span></span>
    
2. <span data-ttu-id="17bfd-134">[ **新規作成**] タブの [ **フォーム テンプレート (高度)**] で [ **Web サービス**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-134">On the **New** tab, double-click **Web Service** under **Advanced Form Templates**.</span></span>
    
3. <span data-ttu-id="17bfd-135">[ **データ接続ウィザード**] ダイアログ ボックスで、[ **データの受信**] を選択し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-135">In the **Data Connection Wizard** dialog box, select **Receive data**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="17bfd-136">サンプルの Web サービス メソッドのある Web サービスのアドレスを入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-136">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span> 
    
5. <span data-ttu-id="17bfd-137">受信メソッドの場合、操作として [ **getXhtml**] を選択し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-137">For the receive method, select **getXhtml** as the operation, and then click **Next**.</span></span>
    
6. <span data-ttu-id="17bfd-138">**getXHTML** Web サービス メソッドはパラメーターを受け取らないので、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-138">The **getXHTML** Web service method takes no parameters, so click **Next**.</span></span>
    
7. <span data-ttu-id="17bfd-139">**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-139">Click **Finish**.</span></span>
    
8. <span data-ttu-id="17bfd-140">[ **データ**] タブの [ **送信処理**] グループで [ **その他の場所へ**] をクリックし、[ **Web サービス**] をクリックして、同じ Web サービスを送信データに使用します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-140">On the **Data** tab, in the **Submit Actions** group click **To Other Locations**, and then click **Web Service** to use the same Web service to the submit data.</span></span> 
    
9. <span data-ttu-id="17bfd-141">サンプルの Web サービス メソッドのある Web サービスのアドレスを入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-141">Type the address of the Web service that contains the sample Web service methods, and then click **Next**.</span></span>
    
10. <span data-ttu-id="17bfd-142">送信メソッドの場合、操作として [ **setXhtml**] を選択し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-142">For the submit method, select **setXhtml** as the operation, and then click **Next**.</span></span>
    
11. <span data-ttu-id="17bfd-143">[ **変更**] をクリックし、[ **dataFields**] フォルダー、[ **s0:getXhtmlResponse**] フォルダー、[ **getXhtmlResult**] フォルダーの順に展開し、[ **MyRichTextElement**] 要素を選択して、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-143">Click **Modify**, expand the **dataFields** folder, expand the **s0:getXhtmlResponse** folder, expand the **getXhtmlResult** folder, select the **MyRichTextElement** element, and then click **Next**.</span></span>
    
12. <span data-ttu-id="17bfd-144">[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17bfd-144">Click **Finish**.</span></span>
    
13. <span data-ttu-id="17bfd-145">[ **フィールド**] 作業ウィンドウで、[ **dataFields**] フォルダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-145">In the **Fields** task pane, expand the **dataFields** folder.</span></span> 
    
14. <span data-ttu-id="17bfd-p109">[ **s0:getXhtmlResponse**] および [ **getXhtmlResult**] フォルダーを展開し、[ **MyRichTextElement**] 要素をフォーム上にドラッグします。InfoPath によって、 **MyRichTextElement** 要素が XHTML 要素であることが認識され、リッチ テキスト ボックス コントロールを使用してバインドされます。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p109">Expand the **s0:getXhtmlResponse** and **getXhtmlResult** folders, and then drag the **MyRichTextElement** element onto the form. InfoPath will recognize that the **MyRichTextElement** element is an XHTML element and will use a rich text box control to bind to it.</span></span> 
    
15. <span data-ttu-id="17bfd-148">フォームを保存または発行します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-148">Save or publish the form.</span></span>
    
<span data-ttu-id="17bfd-p110">フォームをテストするには、フォームを開き、画像、テーブル、書式設定されたテキストなどのリッチ テキストの内容を入力します。リボン上の [ **送信**] をクリックして、リッチ テキストの内容をサーバー上の out.xml ファイルに格納します。[ **表示**] タブの [ **クエリ**] をクリックし、フォーム上の [ **クエリの実行**] ボタンをクリックします。これにより、out.xml ファイルに格納されている XHTML の内容が **リッチ テキスト ボックス** コントロールに表示されます。リッチ テキスト フィールドに複数の行が含まれている場合、Web サービスは 1 行目のみを受け取り、残りは無視します。</span><span class="sxs-lookup"><span data-stu-id="17bfd-p110">To test the form, open the form, enter some rich text content such as pictures, tables, and formatted text. Click **Submit** on the ribbon to store the rich text content in the out.xml file on the server. Click **Query** on the **View** tab, and then click the **Run Query** button on the form. The **Rich Text Box** control should display the XHTML content from the out.xml file. If the rich text field contains multiple lines, the Web service will only accept the first line and ignore the rest.</span></span> 
  

