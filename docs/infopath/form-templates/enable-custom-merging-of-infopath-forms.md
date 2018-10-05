---
title: InfoPath フォームのカスタム結合の有効化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: Microsoft InfoPath エディターのフォームの結合機能を使用すると、複数のフォームのデータを 1 つのフォームに結合することができます。
ms.openlocfilehash: 598c44bfe63a31237bf82ceb2212b001fbe7cc1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386916"
---
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="c7f7a-103">InfoPath フォームのカスタム結合を有効にする</span><span class="sxs-lookup"><span data-stu-id="c7f7a-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="c7f7a-104">Microsoft InfoPath エディターの**フォームの結合**機能を使用すると、複数のフォームのデータを 1 つのフォームに結合することができます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-104">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.</span></span> <span data-ttu-id="c7f7a-105">これは、データの集計とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-105">This is also known as data aggregation.</span></span> <span data-ttu-id="c7f7a-106">フォームの結合が有効になっている場合、**[ファイル]** タブ、**[保存と送信]&amp;**、**[インポートとリンク]&amp;** の **[フォームの結合]**、**[フォームの結合]** ボタンの順にクリックし、1 つ以上のフォームを選択して、現在開かれているフォームに結合することができます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-106">If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form.</span></span> <span data-ttu-id="c7f7a-107">現在開かれているフォームをターゲット フォームと呼び、**[フォームの結合]** ダイアログ ボックスで選択したフォームをソース フォームと呼びます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-107">The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="c7f7a-p102">フォームの結合によって集計されたデータには、ソース フォームとターゲット フォームのすべてのデータが含まれる場合と、元データの一部のみが含まれる場合があります。既定の動作は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p102">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data. The default operations are the following.</span></span>
  
- <span data-ttu-id="c7f7a-p103">繰り返し要素の場合、データはターゲット ドキュメントの対応する場所に挿入されます。これは、ターゲット要素の **MaxOccurs** 属性が 2 以上の場合です。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p103">For repeating elements, data is inserted at a matching location in the target document. This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="c7f7a-112">繰り返さない要素 (つまり、 **MaxOccurs** 属性が "1" の要素) の場合、ソース要素の属性がターゲット要素の既存の属性に追加されます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="c7f7a-113">カスタム変換の作成</span><span class="sxs-lookup"><span data-stu-id="c7f7a-113">Creating a Custom Transform</span></span>

<span data-ttu-id="c7f7a-p104">結合対象のフォームが同じ XML スキーマに基づいている場合は、既定の動作で問題なく結合できます。しかし、スキーマが異なるフォームどうしを結合したり、スキーマが同じ場合の既定の動作を上書きするときもあります。このような場合には、結合の集計指示を記載した XSL 変換 (XSLT) を作成します。XSL 変換は、結合時に適用されます。その結果、インポート対象の情報が記載された DOM ドキュメントと、この情報をターゲット ドキュメントにどのように組み込むかを指定した注釈が作成されます。この注釈は、 `https://schemas.microsoft.com/office/InfoPath/2003/aggregation` 名前空間の XML 属性です。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p104">The default operation when merging forms works well for forms that are based on the same XML schema. In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema. For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation. The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document. These annotations are XML attributes in the namespace  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="c7f7a-p105">XML 属性とそれぞれの値は、各ノードをターゲットの XML ドキュメントにどのように結合するかを明記した集計指示として機能します。次の節では、各属性について説明します。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p105">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document. These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="c7f7a-121">select</span><span class="sxs-lookup"><span data-stu-id="c7f7a-121">select</span></span>

<span data-ttu-id="c7f7a-122">**agg:select** 属性には、ターゲット要素を特定する絶対 XPath 式を指定します。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="c7f7a-123">insert</span><span class="sxs-lookup"><span data-stu-id="c7f7a-123">insert</span></span>

<span data-ttu-id="c7f7a-p106">**agg:action** 属性の値 "insert" は、 **agg:select** 属性に指定されたターゲット要素の子としてソース要素を挿入するように InfoPath に指示するものです。ソース要素の子も挿入対象に含められます。 **selectChild** 属性を使用すると、ノード挿入操作の場所を選択できます。 **order** 属性は、ソース要素を既存のターゲット要素の前に挿入するのか、後に挿入するのかを指定します。 **order** 属性を省略した場合は、"after" が既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p106">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute. The children of the source element are included in the insert operation. The **selectChild** attribute lets you select a certain location for the insert node operation. The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after. The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="c7f7a-129">replace</span><span class="sxs-lookup"><span data-stu-id="c7f7a-129">replace</span></span>

<span data-ttu-id="c7f7a-130">**agg:action** 属性の値 "replace" は、 **select** 属性の参照する各ターゲット要素をソース要素に置き換えることを InfoPath に指示するものです。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="c7f7a-131">mergeAttributes</span><span class="sxs-lookup"><span data-stu-id="c7f7a-131">mergeAttributes</span></span>

<span data-ttu-id="c7f7a-132">**agg:action** 属性の値が "mergeAttributes" の場合は、 **select** 属性の参照する各ターゲット要素の属性とソース要素の属性が結合されます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="c7f7a-133">delete</span><span class="sxs-lookup"><span data-stu-id="c7f7a-133">delete</span></span>

<span data-ttu-id="c7f7a-134">**agg:action** 属性の値が "delete" の場合は、 **select** 属性の参照する各ターゲット要素がターゲット ドキュメントから削除されます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="c7f7a-p107">`https://schemas.microsoft.com/office/InfoPath/2003/aggregation` インターフェイスを実装する XSL オブジェクトを表すには、  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` 名前空間に指定されている属性のほか、  \*\*\*\* 名前空間も使用します。このインターフェイスのメンバーの中で特に有益なのが、 **get-documentElement** です。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p107">In conjunction with the attributes specified in the  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**. One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="c7f7a-137">get-documentElement</span><span class="sxs-lookup"><span data-stu-id="c7f7a-137">get-documentElement</span></span>

<span data-ttu-id="c7f7a-p108">**target:get-documentElement** 関数を使用すると、ターゲット ドキュメントのドキュメント オブジェクト モデルにアクセスできます。ターゲット ドキュメントの現在の内容に基づいて結合の操作を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p108">The **target:get-documentElement** function provides access to the Document Object Model of the destination document. It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="c7f7a-140">カスタム結合の作成手順</span><span class="sxs-lookup"><span data-stu-id="c7f7a-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="c7f7a-p109">データの結合元の XML ソース ドキュメントの種類を選択します。各種ソース ドキュメントの代表的なサンプルを集めてください。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p109">Select the kinds of XML source documents from which you want to merge data. Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="c7f7a-p110">既存の InfoPath フォームの各種 XML ソース ドキュメントに対応した XML スキーマを取り出します。この手順は簡単で、Backstage の [ **発行**] タブの [ **ソース ファイルのエクスポート**] コマンドを使用して XML スキーマをエクスポートするだけです。XML ドキュメントを InfoPath で作成しなかった場合、Microsoft Visual Studio などのツールを使ってサンプルの XML ドキュメントからスキーマを作成できます。または、InfoPath で XML ドキュメントからサンプル フォームを作成し、そのドキュメント構造から InfoPath が導き出したスキーマをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p110">Derive the XML schema for each kind of XML source document for an existing InfoPath form. This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage. For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="c7f7a-p111">各種 XML ソース ドキュメントから結合対象のデータを特定します。 この手順は、ソース フォームとターゲット フォームの両方の要件に大きく依存します。たとえば、ソース フォームからすべてのデータをコピーした方がよい場合があります。一方、フォームの基になる XML ドキュメントから 1 つか 2 つの要素だけをコピーした方がよい場合もあります。結合するデータを特定するときは、ソース ドキュメントとターゲット ドキュメントの内容を十分に把握し、ソース フォームとターゲット フォームの間で要素が論理的にマッピングされるように注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p111">Identify the data that you want to merge from each kind of XML source document. This step will depend almost entirely on the requirements of both your source and destination forms. For some forms, you may want to copy all of the data from the source form. For others, you may want only one or two elements from the form's underlying XML document. When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="c7f7a-p112">各種 XML ソース ドキュメントに対応した XSL 変換を作成します。 フォーム結合の構成で、この手順に最も時間がかかります。XSL 変換の役割は、ターゲット フォームと結合できる形式に XML ソース ドキュメントを変換することです。XSL 変換を設計するときに、XML ロケーション パスによる結合を使用するのか、InfoPath 集計指示による結合を使用するのかを決定してください。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p112">Create an XSL transform for each kind of XML source document. When configuring the merging of your forms, this step will take the most time. The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form. When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="c7f7a-p113">XSL 変換の作成には、Visual Studio が便利です。Visual Studio には、構文に色を付ける機能や、ドキュメントの概要を参照する機能があります。また、XSL 要素の終了タグを自動的に付与してくれるので、余分なタイピングが不要になり、入力ミスを抑えることができます。メモ帳などのテキスト エディターでも、XSL 変換を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p113">Visual Studio is a convenient tool for creating XSL transforms. Visual Studio provides syntax coloring and a document outline. It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors. You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="c7f7a-159">まず、恒等変換から始めます。これは、入力と同じ XML ファイルを出力する XSL 変換です。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="https://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="https://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="https://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    <span data-ttu-id="c7f7a-p114">次に、特殊な処理を追加する要素のテンプレート セクションを上書きします。たとえば、次のテンプレートでは  `<src:Task>` 要素を  `<my:field1>` 要素に変換し、 **agg:action** 属性の値に "replace" を設定しています。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p114">Then add overriding template sections for the elements you want to add special handling for. For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="c7f7a-p115">XSL 変換ファイルとスキーマ ファイルをフォーム テンプレートに追加します。 各種ソース ドキュメントに対応したスキーマを導き出し、また InfoPath がデータを結合できる形に各種ソース ドキュメントを変換する XSL 変換を作成したら、各スキーマと XSL 変換をフォームのリソースとして追加します。[ **データ**] タブの [ **リソース ファイル**] をクリックし、[ **リソース ファイル**] ダイアログ ボックスの [ **追加**] をクリックします。作成したスキーマ ファイルまたは XSL 変換ファイルを表示し、[ **OK**] をクリックします。作成したスキーマ ファイルおよび XSL 変換ファイルごとに、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p115">Add the XSL transform files and schema files in the form template. After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form. Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**. Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="c7f7a-p116">追加するスキーマの中で **targetNamespace** 属性を使用している場合には、プロパティ要素をフォームの .xsf ファイルに追加する必要があります。これにより、InfoPath がスキーマの名前空間を認識できるようになります。フォームの .xsf ファイルにアクセスするには、[ **ファイル**] タブの [ **発行**] をクリックし、[ **ソース ファイルのエクスポート**] をクリックします。スキーマ ファイルおよび XSL 変換ファイルの保存場所を選択し、[ **OK**] をクリックします。設計していた InfoPath フォーム テンプレートを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p116">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema. To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**. Select a location for the files, and then click **OK**. Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="c7f7a-p117">抽出したファイルの保存場所を開き、拡張子が .xsf のファイルを探します。通常は、manifest.xsf という名前が付けられています。このファイルをメモ帳で開き、スキーマに対応した  `<xsf:file>` タグを探し、"namespace" プロパティ要素を追加します。これは、次の例で示すように **targetNamespace** を指定するプロパティ要素です。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-p117">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension. Usually, this file is called manifest.xsf. Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="c7f7a-173">カスタム結合に対応するようにフォームを準備する最後の手順は、フォームに関連付けられている .xsf ファイルの **importParameters** 要素を更新することです。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="c7f7a-174">最初に、.xsf ファイルで `<xsf:importParameters>` タグを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="c7f7a-175">フォームに対して作成したスキーマ/ XSL 変換ペアごとに、**xsf:importSource** 要素を **xsf:importParameters** 要素に追加します。 `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="c7f7a-176">**xsf:importSource** 要素の **name** 属性には、ソース XML ドキュメントにあるフォーム テンプレートの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="c7f7a-177">通常、これは空白のままにできます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="c7f7a-178">**schema** 属性には、前の手順でフォーム テンプレートに追加したスキーマ ファイルの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="c7f7a-179">**transform** 属性には、スキーマに準拠するフォームを変換するために使用する XML 変換の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="c7f7a-180">カスタム変換は、[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントで使用するか、または単独で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="c7f7a-181">コードによるカスタム結合の作成</span><span class="sxs-lookup"><span data-stu-id="c7f7a-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="c7f7a-182">[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベント ハンドラーを使用することで、コードによってカスタム結合を作成できます。フォームに関連付けられている .xsf ファイルで、対応する **importParameters** 要素の **useScriptHandler** 属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="c7f7a-183">マネージ コードの場合は、**[ユーザー設定コードを使って結合する]** をオンにして、Backstage から利用できる **[詳細設定]** カテゴリの **[フォームのオプション]** ダイアログ ボックスで **[編集]** ボタンをクリックすることで、[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c7f7a-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

