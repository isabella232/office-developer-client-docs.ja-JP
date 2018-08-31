---
title: InfoPath で XML スキーマを使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Microsoft InfoPath で作成するフォーム テンプレートでは、InfoPath フォームで入力、編集、出力される XML の構造とデータの検証が XML スキーマ (XSD) を使用して実行されます。InfoPath のフォーム デザイン ウィンドウで作成したすべてのフォーム テンプレートには、実行時の検証に使用される XSD スキーマ ファイル (.xsd) が少なくとも 1 つ含まれています。
ms.openlocfilehash: 6921a2206c098992a0a24e85c263992a0e2c98b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799238"
---
# <a name="working-with-xml-schemas-in-infopath"></a><span data-ttu-id="cf09b-104">InfoPath で XML スキーマを使用する</span><span class="sxs-lookup"><span data-stu-id="cf09b-104">Working with XML Schemas in InfoPath</span></span>

<span data-ttu-id="cf09b-p102">Microsoft InfoPath で作成するフォーム テンプレートでは、InfoPath フォームで入力、編集、出力される XML の構造とデータの検証が XML スキーマ (XSD) を使用して実行されます。InfoPath のフォーム デザイン ウィンドウで作成したすべてのフォーム テンプレートには、実行時の検証に使用される XSD スキーマ ファイル (.xsd) が少なくとも 1 つ含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p102">A form template that you create with Microsoft InfoPath uses an XML Schema (XSD) to perform structural and data validation on the XML that is input, edited, and output from an InfoPath form. Every form template created in the InfoPath form designer contains at least one XSD schema file (.xsd) that is used for validation at run time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf09b-p103">このトピックで説明する内容は、InfoPath エディターでの使用を目的としてフォーム テンプレートをデザインする場合に適用されます。ブラウザー互換のフォーム テンプレートの場合は、XSD スキーマの要件がより厳しくなります。詳細については、ブラウザー互換フォーム テンプレートの XML スキーマに関する MSDN のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p103">The information contained in this topic applies to form templates designed for use in the InfoPath editor. Browser-compatible form templates have stricter XSD Schema requirements. For more information, see the documentation about XML Schemas in browser-compatible form templates available on MSDN.</span></span> 
  
## <a name="using-externally-authored-xml-schemas"></a><span data-ttu-id="cf09b-110">外部で作成された XML スキーマを使用する</span><span class="sxs-lookup"><span data-stu-id="cf09b-110">Using Externally-authored XML Schemas</span></span>

<span data-ttu-id="cf09b-111">InfoPath の外部で作成された XSD スキーマ ファイルを読み込むには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-111">To load an XSD schema file that was authored outside of InfoPath, follow these steps.</span></span>
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a><span data-ttu-id="cf09b-112">外部スキーマに基づいてフォーム テンプレートを作成するには</span><span class="sxs-lookup"><span data-stu-id="cf09b-112">To create a form template based on an external schema</span></span>

1. <span data-ttu-id="cf09b-113">Backstage で [ **新規作成**] をクリックし、[ **フォーム テンプレート (高度)**] の [ **XML またはスキーマ**] をクリックして、[ **フォームのデザイン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf09b-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span></span>
    
2. <span data-ttu-id="cf09b-114">**データ ソース ウィザード**で、使用する XSD スキーマ ファイルを指定して [ **次へ**] をクリックし、ウィザードの残りのページの処理を行います。</span><span class="sxs-lookup"><span data-stu-id="cf09b-114">In the **Data Source Wizard**, specify the XSD schema file you want to use, and then click **Next** and complete the remaining pages of the wizard.</span></span> 
    
## <a name="unsupported-xsd-constructs"></a><span data-ttu-id="cf09b-115">サポートされていない XSD コンストラクト</span><span class="sxs-lookup"><span data-stu-id="cf09b-115">Unsupported XSD Constructs</span></span>

<span data-ttu-id="cf09b-p104">ここでは、InfoPath で実行時に処理できない XSD コンストラクトについて説明します。InfoPath のフォーム デザイン ウィンドウでフォーム テンプレートを作成する際は、これらのコンストラクトを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p104">The following sections describe XSD constructs that InfoPath cannot handle at run time. Avoid these constructs when creating a form template in the InfoPath form designer.</span></span>
  
## <a name="entity-and-entities-types"></a><span data-ttu-id="cf09b-118">ENTITY 型と ENTITIES 型</span><span class="sxs-lookup"><span data-stu-id="cf09b-118">ENTITY and ENTITIES Types</span></span>

<span data-ttu-id="cf09b-p105">**ENTITY** 型と **ENTITIES** 型は、検証にドキュメント型定義 (DTD) が必要ですが、InfoPath は DTD をサポートしていません。InfoPath では、このようなスキーマに基づくフォーム テンプレートはデザインできないため、 **ENTITY** 型の派生元である **NCName** 型を **ENTITY** の代わりに使用することを勧めるエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p105">The **ENTITY** and **ENTITIES** types require a document type definition (DTD) for validation, which InfoPath does not support. InfoPath does not allow you to design a form template against such a schema and displays an error message that recommends changing the **ENTITY** type to the **NCName** type from which **ENTITY** derives.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="cf09b-121">InfoPath のデザイン モード以外の場所でフォーム テンプレートを手動で作成し、このテンプレートで **ENTITY** 型と **ENTITIES** 型を含む XSD を使用する場合、これらの型に必要な DTD が Template.xml ファイルに記述されていれば、フォーム テンプレートが実行時に機能します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-121">If you manually author an InfoPath form template outside of design mode, and it uses an XSD that includes **ENTITY** and **ENTITIES** types, the form template may work at run time if the Template.xml file contains the required DTD for these types.</span></span> 
  
## <a name="required-xsdany-element"></a><span data-ttu-id="cf09b-122">必須の xsd:any 要素</span><span class="sxs-lookup"><span data-stu-id="cf09b-122">Required xsd:any Element</span></span>

<span data-ttu-id="cf09b-p106">**xsd:any** ワイルドカード要素が出現する場合、つまり、 **xsd:any** 要素の **minOccurs** 属性の値がゼロより大きい場合 ("必須の any 要素")、InfoPath でこのスキーマ フラグメントに対する有効なインスタンスを判定して作成することができません。InfoPath では、このようなスキーマ フラグメントを使用するフォームの生成時に、有効なインスタンスを作成できなくてはなりません。スキーマで **xsd:any** 要素が必須となっている場合は、 **データ ソース ウィザード**の実行時に、必須の **xsd:any** 要素の代わりに使用するスキーマ要素を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p106">An occurrence of an **xsd:any** wildcard element, that is, an occurrence of an **xsd:any** element with a **minOccurs** attribute value greater than zero ("required any"), prevents InfoPath from deterministically creating a valid instance for this schema fragment. InfoPath must be able to create a valid instance when generating a form that uses this schema fragment. As part of running the **Data Source Wizard**, schemas with required **xsd:any** elements require you to choose which schema element you want to use in place of the required **xsd:any** element.</span></span> 
  
## <a name="elements-with-an-abstract-complex-type"></a><span data-ttu-id="cf09b-126">抽象複合型の要素</span><span class="sxs-lookup"><span data-stu-id="cf09b-126">Elements with an Abstract Complex Type</span></span>

<span data-ttu-id="cf09b-p107">InfoPath のデザイン モードでは、抽象複合型を使用するスキーマに基づいてフォーム テンプレートをデザインできます。たとえば、 `shippingAddress` という要素の型が  `address` という名前の抽象複合型であり、この抽象複合型に  `USAddress` と  `CanadianAddress` という 2 つの派生型がある場合、InfoPath では、  `shippingAddress` のすべてのインスタンスが、  `shippingAddress` 型の  `USAddress` と  `shippingAddress` 型の  `CanadianAddress` の二者択一として扱われます。この例では、提供されたスキーマに address から派生する型がない場合、InfoPath はこの要件を満たす追加のスキーマを必要とします。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p107">InfoPath design mode supports designing a form template against schemas that use abstract complex types. For example, if an element named  `shippingAddress` has an abstract complex type named  `address` that has two derivations,  `USAddress` and  `CanadianAddress`, InfoPath treats any instance of  `shippingAddress` as a choice between  `shippingAddress` with type  `USAddress` and  `shippingAddress` with type  `CanadianAddress` . In this example, if the provided schemas contain no types that derive from address, then InfoPath requests an additional schema that fulfills this requirement.</span></span> 
  
## <a name="xsd-constructs-with-reduced-functionality"></a><span data-ttu-id="cf09b-130">機能が制限される XSD コンストラクト</span><span class="sxs-lookup"><span data-stu-id="cf09b-130">XSD Constructs with Reduced Functionality</span></span>

<span data-ttu-id="cf09b-131">ここでは、InfoPath のフォーム デザイン ウィンドウでフォーム テンプレートを作成する際、使用すると機能が制限される XSD コンストラクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-131">The following sections describe XSD constructs that have reduced functionality when used to create a form template in the InfoPath form designer.</span></span>
  
## <a name="substitution-groups"></a><span data-ttu-id="cf09b-132">代替グループ</span><span class="sxs-lookup"><span data-stu-id="cf09b-132">Substitution Groups</span></span>

<span data-ttu-id="cf09b-p108">代替グループのメンバーはすべて [ **フィールド**] 作業ウィンドウに表示されます。InfoPath では、代替候補がすべての代替グループからの複数択一として表現されます (定義元の要素も抽象要素でない場合は対象となります)。抽象要素の代替グループがない場合は、代替グループである要素を少なくとも 1 つ含むスキーマを提供するように求められます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p108">All members of the substitution group appear in the **Fields** task pane. InfoPath represents the substitution possibilities as a choice of all the substitution groups (including the defining element, if it is not abstract). If there are no substitution groups for an abstract element, InfoPath prompts you to provide a schema that contains at least one element that is a substitution group.</span></span> 
  
## <a name="unbounded-choice-elements"></a><span data-ttu-id="cf09b-136">unbounded の choice 要素</span><span class="sxs-lookup"><span data-stu-id="cf09b-136">Unbounded Choice Elements</span></span>

<span data-ttu-id="cf09b-137">次のスキーマ フラグメントは、unbounded の choice 要素を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf09b-137">The following schema fragment shows an unbounded choice element:</span></span>
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

<span data-ttu-id="cf09b-p109">InfoPath では、繰り返し出現する選択肢要素は、[ **フィールド**] 作業ウィンドウに繰り返し選択肢として表示されます。[ **繰り返し選択肢グループ**] というコントロールを使用して、XSD で繰り返し回数が無制限の choice 要素によって定義される、異種混在情報の一覧を表現できます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p109">InfoPath displays repeating choice elements as repeating choices in the **Fields** task pane. There is a **Repeating Choice Group** control that you can use to represent the heterogeneous list defined by the repeating choice element in the XSD.</span></span> 
  
## <a name="repeating-sequence"></a><span data-ttu-id="cf09b-140">繰り返し回数が無制限の sequence 要素</span><span class="sxs-lookup"><span data-stu-id="cf09b-140">Repeating Sequence</span></span>

<span data-ttu-id="cf09b-141">次のスキーマ フラグメントは、繰り返し回数が無制限の sequence 要素を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf09b-141">The following schema fragment shows a repeating sequence:</span></span>
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

<span data-ttu-id="cf09b-142">繰り返し回数が無制限の sequence 要素に必要な子要素が含まれていれば、その XSD を無変更で InfoPath に読み込み、繰り返し出現の sequence 要素に繰り返しセクション コントロールをバインドできます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-142">As long as the repeating sequence contains a required element, InfoPath loads the XSD without modifying it and allows you to bind repeating section controls to the repeating sequence.</span></span>
  
## <a name="choice-of-model-groups"></a><span data-ttu-id="cf09b-143">モデル グループの選択</span><span class="sxs-lookup"><span data-stu-id="cf09b-143">Choice of Model Groups</span></span>

<span data-ttu-id="cf09b-144">次のスキーマ フラグメントは、複数のモデル グループを含む choice 要素を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf09b-144">The following schema fragment shows the choice element containing several model groups:</span></span>
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

<span data-ttu-id="cf09b-p110">InfoPath のデザイン モードでは、このような XSD コンストラクトがそのままサポートされ、フォーム デザイン ウィンドウで変更を加える必要はありません。InfoPath でスキーマの意味が変更されることはありませんが、[ **フィールド**] 作業ウィンドウでは上記の choice 構造体が同等の 1 つの選択肢グループとして簡易表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p110">InfoPath design mode supports such XSD constructs without requiring any modification by the form designer. While InfoPath does not modify the meaning of the schema, it simplifies the choice construct above into an equivalent collapsed single choice in the **Fields** task pane.</span></span> 
  
## <a name="optional-sibling-with-same-qualified-name"></a><span data-ttu-id="cf09b-147">修飾名が同じ省略可能な兄弟要素</span><span class="sxs-lookup"><span data-stu-id="cf09b-147">Optional Sibling with Same Qualified Name</span></span>

<span data-ttu-id="cf09b-148">次のスキーマ フラグメントは、修飾名 (`QName`) が同じ省略可能な兄弟要素を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf09b-148">The following schema fragment shows an optional sibling with same qualified name (QName`QName`):</span></span>
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

<span data-ttu-id="cf09b-p111">これらのノードを取得するための **XPath** 式は、InfoPath のフォーム デザイン ウィンドウで XML インスタンスの候補をすべて考慮する必要があるため、複雑になる場合があります。InfoPath では、正しい **XPath** バインディングを作成できない可能性があるスキーマ部分は公開されません。無視されるスキーマ部分については、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p111">**XPath** expressions for these nodes can be complex because every potential XML instance must be accounted for in the InfoPath form designer. InfoPath does not expose parts of the schema for which it may have difficulty creating correct **XPath** bindings. Warnings appear regarding the portions of the schema that are ignored.</span></span> 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a><span data-ttu-id="cf09b-152">InfoPath で特別な意味を持つ XSD コンストラクト</span><span class="sxs-lookup"><span data-stu-id="cf09b-152">XSD Constructs with Special Meaning in InfoPath</span></span>

<span data-ttu-id="cf09b-p112">ここでは、デザイン モードでフォーム テンプレートを作成する際、使用すると特別な意味が発生する XSD コンストラクトについて説明します。これらのコンストラクトをスキーマで使用して、特定の動作を有効にする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p112">The following sections describe XSD constructs that have special meaning when used in creating a form template in design mode. These sections describe how you can use the constructs in your schema to enable certain behaviors.</span></span>
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a><span data-ttu-id="cf09b-155">[フィールド] 作業ウィンドウで新しい要素フィールドとグループを追加する</span><span class="sxs-lookup"><span data-stu-id="cf09b-155">Adding New Element Fields and Groups with the Fields Task Pane</span></span>

<span data-ttu-id="cf09b-p113">デザイン時に [ **フィールド**] 作業ウィンドウを使用して新しい要素フィールドやグループを追加できる構造を、スキーマに含めておくことができます。そのようにするには、省略可能な unbounded の **xsd:any** 要素を使用してスキーマで要素宣言をし、xsd:any 要素の namespace 属性に **##any** ワイルドカードを指定します。これにより、デザイン時に [ **フィールド**] 作業ウィンドウを使用して、その要素に新しい要素フィールドやグループを追加できるようになります。たとえば、次の要素には新しいコンテンツを追加できます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p113">You can construct your schema so that you can use the **Fields** task pane to add new element fields and groups to an element at design time. To do so, you declare an element in your schema with an optional, unbounded **xsd:any** element that specifies the namespace attribute with the **##any** wildcard. Then, in design mode, you can use the **Fields** task pane to add new element fields and groups to that element. For example, you could add new content to the following element:</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a><span data-ttu-id="cf09b-160">[フィールド] 作業ウィンドウで新しい属性フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="cf09b-160">Adding New Attribute Fields with the Fields Task Pane</span></span>

<span data-ttu-id="cf09b-p114">要素の場合と同様に、namespace 属性に **##any** ワイルドカードを指定した **anyAttribute** 要素を使用して属性を宣言します。デザイン時に、[ **フィールド**] 作業ウィンドウを使用して、このスキーマ属性に新しいコンテンツを追加できます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p114">Similarly to the element case, you can declare an attribute with an **anyAttribute** element that has the namespace attribute specified as the **##any** wildcard. At design time, you can use the **Fields** task pane to add new content to that schema attribute.</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a><span data-ttu-id="cf09b-163">データ ソースに XML 署名を格納する</span><span class="sxs-lookup"><span data-stu-id="cf09b-163">Storing XML Signatures in the Data Source</span></span>

<span data-ttu-id="cf09b-p115">実行時にユーザーのデジタル署名をフォームに入力できるようにするには、ユーザーがフォームに署名したときに作成される XML 署名 (デジタル署名) 情報の格納用として、signature という名前の要素をデータ ソースのスキーマで宣言する必要があります。この宣言は、 **xsd:any** 要素を使用して行い、その namespace 属性にはワイルドカード文字を使用して XML 署名の名前空間を指定します (例: "http://www.w3c.org/2000/09/xmldsig#")。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p115">To enable users to digitally sign a form at run time, the schema of the data source must declare an element named signature for storing the XML Signatures (digital signature) information that is created when a user signs the form. You make this declaration by using the **xsd:any** element with the namespace attribute specified as the XML Signatures namespace with a wildcard character, as follows: "http://www.w3c.org/2000/09/xmldsig#"</span></span> 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a><span data-ttu-id="cf09b-166">リッチ テキスト ボックス コントロールにフィールドをバインドする</span><span class="sxs-lookup"><span data-stu-id="cf09b-166">Binding a Field to a Rich Text Box Control</span></span>

 <span data-ttu-id="cf09b-p116">InfoPath の **リッチ テキスト ボックス** コントロールは、汎用的な XHTML を生成します。したがって、フォーム インスタンスの XML では任意の数のテキスト ノードと XHTML ノードが有効であることが、スキーマで指定されている必要があります。そのように指定するには、次の XSD コンストラクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p116">**Rich Text Box** controls in InfoPath generate generic XHTML; consequently, your schema must specify that any number of text and XHTML nodes is valid in the XML of the form instance. You can achieve this specification with the following XSD construct:</span></span> 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="http://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> <span data-ttu-id="cf09b-p117">InfoPath では、スキーマ ファイル (.xsd) の内容が変更されることはありませんが、論理的にスキーマ ファイルがデザイン用のサブセットとして扱われることはあります。スキーマ ファイルは、デザイン時も実行時もフォーム テンプレート内では必ず無変更のまま維持されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p117">InfoPath never modifies the content of the schema file (.xsd), but it may logically infer a subset of it for design purposes. The schema file is always untouched within the form template at both design time and run time.</span></span> 
  
## <a name="debugging-common-xsd-errors"></a><span data-ttu-id="cf09b-171">一般的な XSD エラーをデバッグする</span><span class="sxs-lookup"><span data-stu-id="cf09b-171">Debugging Common XSD Errors</span></span>

<span data-ttu-id="cf09b-p118">外部で作成された XSD ファイルを読み込んで、InfoPath フォーム デザイン ウィンドウでフォーム テンプレートを作成する場合、MSXML エラー メッセージと InfoPath エラー メッセージの 2 種類のエラー メッセージのどちらかが表示されることがあります。MSXML のエラー メッセージは、InfoPath のエラー メッセージ ダイアログ ボックスの [ **詳細**] セクションに表示され、冒頭には必ず、エラーの原因となっているスキーマ ファイルの名前またはパスに関する情報が示されます。InfoPath では、XSD スキーマの有効なコンストラクトの一部がサポートされていません。これらのコンストラクトについては、「サポートされていない XSD コンストラクト」で前述しています。ここでは、スキーマを InfoPath に正常に読み込めない結果を招く一般的なエラーの一部について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p118">If you load externally authored XSD files to create form templates in the InfoPath form designer, you may receive either of two types of error messages: MSXML error messages or InfoPath error messages. MSXML error messages appear in the **Details** section of an InfoPath error message dialog box, and they always begin with a reference to the name or path of the schema file that is raising the error. Some valid XSD schema constructs are not supported by InfoPath; these are discussed in the Unsupported XSD Constructs section. The following sections describe some common errors that can cause schemas to fail to load successfully in InfoPath.</span></span> 
  
## <a name="the-xsd-namespace-declaration"></a><span data-ttu-id="cf09b-176">XSD 名前空間の宣言</span><span class="sxs-lookup"><span data-stu-id="cf09b-176">The XSD Namespace Declaration</span></span>

<span data-ttu-id="cf09b-p119">すべての W3C 標準と同様に、XML スキーマ (XSD) も長期にわたる検討プロセスを経て勧告となるに至っています。多数の草案が出され、絶えず変化する草案段階の各標準に基づいて数々の XSD ファイルが記述されました。この勧告プロセスの間に、Microsoft は XML-Data Reduced (XDR) と呼ばれる独自のスキーマ言語を開発し、MSXML 3.0 に組み込みました。MSXML 4.0 のリリース以降は、Microsoft XML Core Services で XSD の勧告をサポートしています。スキーマ作成用の多数のプログラムが、XSD の勧告を待たずに開発されました。これらの古いバージョンのプログラムでは、InfoPath が依存する MSXML 5.0 インフラストラクチャでサポートされていない旧式の XSD ファイルが作成される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p119">Similar to all W3C standards, XML Schemas (XSD) went through a lengthy review process on its way to becoming a recommendation. There were many working drafts, and consequently, many XSD files were written based on these evolving standards. During this process, Microsoft created a proprietary schema language called XML-Data Reduced (XDR) that was included with MSXML 3.0. Starting with the release of MSXML 4.0, Microsoft XML Core Services supports the full recommendation of XSD. Many programs for creating schemas did not wait for XSD to become a full recommendation. Older versions of these programs may produce outdated XSD files that the MSXML 5.0 infrastructure, on which InfoPath depends, does not support.</span></span>
  
<span data-ttu-id="cf09b-183">XSD ファイルが XSD 勧告を確実にサポートするようにするには、次の XML 名前空間宣言を \<schema\> タグに含めます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-183">To ensure that an XSD file supports the full XSD recommendation, it should contain the following XML namespace declaration in the \<schema\> tag:</span></span>
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

<span data-ttu-id="cf09b-p120">すべての XML 名前空間宣言と同様、XML プレフィックス (この場合は 'xsd') には、有効なプレフィックス文字列を任意に指定できます。実際に使用される一般的なプレフィックスとしては、'xsd'、'xs'、'' (プレフィックスなし) などが挙げられます。MSXML では、通常、この名前空間宣言がない場合、ルートが正しく定義されていないという内容のエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p120">Similar to all XML namespace declarations, the XML prefix (in this case 'xsd') can be any valid prefix string. Some common prefixes you may see in practice are 'xsd', 'xs', and '' (no prefix). MSXML usually reports an error about the root not being properly defined if this namespace declaration is missing.</span></span>
  
## <a name="importing-and-including-schemas"></a><span data-ttu-id="cf09b-187">スキーマをインポートおよびインクルードする</span><span class="sxs-lookup"><span data-stu-id="cf09b-187">Importing and Including Schemas</span></span>

<span data-ttu-id="cf09b-p121">XSD スキーマは拡張が可能で、他のスキーマをインポートおよびインクルードできます。一般に、 **targetNamespace** 属性で指定されているスキーマが現在のスキーマと異なる場合は、スキーマをインポートします。 **targetNamespace** 属性に指定されているスキーマが現在のスキーマと同じ場合は、スキーマをインクルードします。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p121">XSD schemas are extensible and can import and include other schemas. Generally, you should import a schema if the schema specified in the **targetNamespace** attribute differs from the current schema. You should include it if the schema specified in the **targetNamespace** attribute is the same as the current schema.</span></span> 
  
<span data-ttu-id="cf09b-191">スキーマのインポートとインクルードのセマンティクスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cf09b-191">The semantics for importing and including schemas are as follows:</span></span>
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

<span data-ttu-id="cf09b-p122">**schemaLocation** 属性がない場合 (一部のコンバーターで起こることがあります)、MSXML でスキーマ ファイルが見つからないためエラーが報告されます。このエラーが表示された場合は、schemaLocation 属性に指定されているリソースまたは場所に、フォーム テンプレートのユーザーがアクセス可能かどうかも確認してください。 **schemaLocation** 属性で参照されているサーバーまたはディレクトリが停止しているか存在しない場合、またはユーザーにアクセス許可が割り当てられていない場合は、当然のことながらエラーが発生します。また、インポートまたはインクルードされるスキーマがすべて有効なスキーマであることも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p122">If the **schemaLocation** attribute is missing (as happens with some converters), then MSXML raises an error because it cannot find the file. If you get this error, also check to make sure that the resource or location specified in the schemaLocation attribute is accessible by users of the form template. Obviously, errors occur if the **schemaLocation** attribute references a server or directory that is down or nonexistent or if users do not have access permissions. Also, be sure to examine all imported and included schemas to make sure they are valid.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cf09b-p123">**schemaLocation** 属性に起因するエラーが問題となるのは、InfoPath でスキーマを最初にインポートするとき、つまり、既存のスキーマに基づいて初めてフォームのデザインを開始するときに限られます。それ以降は、InfoPath では、フォーム テンプレートに格納されているスキーマ ファイルのキャッシュ済みバージョンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p123">Errors caused by problems with the **schemaLocation** attribute are an issue only when InfoPath first imports the schemas; that is, when you first start designing a form based on an existing schema. After that, InfoPath works with cached versions of the schema files that are stored in the form template.</span></span> 
  
<span data-ttu-id="cf09b-p124">スキーマをインポートする場合は、そのスキーマで **targetNamespace** 属性が指定されていなければ、namespace 属性を空にすることができます。一般に、インポート時の名前空間は、インポートするスキーマに指定されている **targetNamespace** に一致しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p124">An empty namespace attribute is allowed when importing a schema, if that schema does not specify a **targetNamespace** attribute. In general, the namespace on the import must match the **targetNamespace** specified in the schema that you import.</span></span> 
  
## <a name="nondeterministic-schemas"></a><span data-ttu-id="cf09b-200">非決定論的スキーマ</span><span class="sxs-lookup"><span data-stu-id="cf09b-200">Nondeterministic Schemas</span></span>

<span data-ttu-id="cf09b-p125">InfoPath が依存する MSXML 5.0 インフラストラクチャは、非決定論的なスキーマを確実に検出し、このようなスキーマについて警告エラーを報告しますが、このときのエラー メッセージには、エラーの原因となっているスキーマ部分を示す行番号は表示されません。ここでは、XSD スキーマ ファイルが決定論的であることが重要である理由と、非決定論的とはどういう意味かを説明します。また、一般に陥りやすいエラーについても説明します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p125">The MSXML 5.0 infrastructure that InfoPath depends upon can reliably detect and raise errors to alert you to nondeterministic schemas, but the resultant error message does not provide a line number to tell you which part of the schema is raising the error. This section discusses why it is important for XSD schema files to be deterministic and what it means to be nondeterministic. It also shows some common errors to avoid.</span></span>
  
<span data-ttu-id="cf09b-p126">XSD スキーマの存在意義は、XML のデータ構造と型のセマンティクスを検証することにあります。この目的を果たすために、検証システム (この場合は MSXML 5.0) では XML ノードを XSD 宣言に対応付ける必要があります。この対応付けを行わないと、検証システムで検証を遂行することができません。この対応付けを確実に行える場合、そのスキーマは決定論的であると見なされます。対応付けを不可能にする XML インスタンスが 1 つでもある場合、スキーマは非決定論的ということになります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p126">XSD schemas exist for the purpose of validating XML data structure and type semantics. To accomplish this task, the validating system (in this case, MSXML 5.0) must map XML nodes to XSD declarations. Without this mapping, the validating system cannot accomplish its task. If a mapping can be guaranteed, then the schema is deterministic. If there is a single XML instance that makes this mapping impossible, then the schema is nondeterministic.</span></span>
  
<span data-ttu-id="cf09b-209">次に、非決定論的なスキーマの例を示します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-209">The following example schema is nondeterministic:</span></span>
  
```XML
<xsd:element name="file_Information"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element name="file_name"/> 
            <xsd:choice> 
                <xsd:element name="file_path"/> 
                <xsd:sequence> 
                    <xsd:element name="file_path" minOccurs="0"/> 
                    <xsd:element name="URI"/> 
                </xsd:sequence> 
            </xsd:choice> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="cf09b-210">この XSD セグメントが非決定論的である理由を説明するために、次の XML フラグメントをこのスキーマで検証する場合を想定します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-210">To illustrate why this XSD segment is nondeterministic, assume you have the following XML fragment that you want to validate with this schema:</span></span>
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

<span data-ttu-id="cf09b-211">この XML フラグメントでは、*\<file_path\>* 要素が、choice 要素宣言の最初の部分を出所とする必須ノードなのか、choice 要素宣言の 2 番目の部分を出所とする省略可能なノードなのかが判然としません。</span><span class="sxs-lookup"><span data-stu-id="cf09b-211">In this XML fragment, it is not clear whether the <file_path> element is the required node from the first part of the choice declaration or the optional one from the second part of the choice declaration. This distinction is important for the following reasons:</span></span> <span data-ttu-id="cf09b-212">この区別は、次の理由で重要になってきます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-212">This distinction is important for the following reasons:</span></span> 
  
1. <span data-ttu-id="cf09b-213">この XML フラグメントが choice 要素宣言の最初の部分に照らして検証される場合、XML はスキーマに対して有効と判断されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-213">If the XML fragment is validated against the first part of the choice declaration, then the XML is valid against the schema.</span></span>
    
2. <span data-ttu-id="cf09b-214">XML フラグメントが choice 要素宣言の第 2 の部分に照らして検証される場合、必須の \<URI\> ノードがないため、スキーマは有効ではないと判断されます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-214">If the XML fragment is validated against the second part of the choice declaration, then the schema is not valid, because the required \<URI\> node is missing.</span></span> 
    
<span data-ttu-id="cf09b-p128">XSD 検証システムによっては、有効なパスが存在することから、このスキーマに照らした検証で誤った判断が下される場合がありますが、MSXML はより厳密であり、スキーマが非決定論的であるというエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p128">Some XSD validation systems err toward validating against this schema because there is a valid path. MSXML is stricter and raises an error stating that the schema is nondeterministic.</span></span>
  
<span data-ttu-id="cf09b-p129">以降では、非決定論的なスキーマの例をさらにいくつか説明します。まず、省略可能な要素について説明します。このようなケースは、XDR と XSD の 2 つのスキーマ言語で既定の基数が異なることから、XDR から XSD へのコンバーターに起因してよく生じます。最初に検討すべきケースは、 **xsd:choice** 要素と **xsd:sequence** 要素を使用して宣言される省略可能な要素です。 **xsd:sequence** 要素内で宣言される省略可能な要素は、通常は適切に検証されますが、次の例に示すように、同じ名前の複数の要素が間に省略可能な要素のみを挟んで出現する場合は例外となります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p129">What follows are a few more examples of nondeterministic schemas. The first deals with optional elements. These cases often arise from XDR to XSD converters because of differences in the default cardinalities in the two schema languages. The first case to consider is optional elements declared with **xsd:choice** and **xsd:sequence** elements. Optional elements declared in an **xsd:sequence** element usually validate properly, as long as you do not have elements with the same name more than once, with only optional elements in between. For example:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:element ref="aNode" /> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="cf09b-223">このスキーマ フラグメントが非決定論的である理由を説明するために、次の有効な XML フラグメントについて考えることにします。</span><span class="sxs-lookup"><span data-stu-id="cf09b-223">To understand why this schema segment is nondeterministic, assume you have the following invalid XML fragment:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

<span data-ttu-id="cf09b-224">`<aNode>` 要素の前に、1 回しか出現してはならない  `<anotherNode>` 要素が 2 回出現しているため、このフラグメントは明らかに無効です。</span><span class="sxs-lookup"><span data-stu-id="cf09b-224">Looking at this fragment, you can see why it is invalid: there are two  `<aNode>` elements before the  `<anotherNode>` element, when only one is allowed.</span></span> 
  
<span data-ttu-id="cf09b-225">ここで、次の XML インスタンスを検証する場合を考えます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-225">Now assume that you have the following XML instance to validate:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

<span data-ttu-id="cf09b-p130">この場合の課題は、このインスタンスが有効かどうかをどのように判定するかです。1 回しか出現してはならない  `<aNode>` 要素が 2 回出現しているのか、それとも、それぞれ許容される  `<aNode>` 要素が 1 回ずつ出現しているのか、これだけでは判断できません。十分な判断材料がないため、このスキーマは非決定論的ということになります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p130">The challenge is to determine whether this instance is valid. Do you have two  `<aNode>` elements where only one is allowed, or do you have an  `<aNode>` element where it is allowed and another where it is allowed? The schema is nondeterministic because there is no way to know.</span></span> 
  
<span data-ttu-id="cf09b-p131">同様に、 **xsd:choice** 要素内で宣言される省略可能要素も、通常は問題になります。次の簡単な例では、choice が 1 回出現しているが省略可能要素が存在しないのか、それとも一度も出現していないのか判断できません。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p131">Similarly, optional elements declared in an **xsd:choice** element are usually problematic. In the following simplified example, there is no way to determine whether the choice occurred once with the optional element not being there or whether it never occurred at all.</span></span> 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

<span data-ttu-id="cf09b-p132">問題となる例として最後に説明するのは、 **xsd:sequence** 要素の後に、  `<xsd:any namespace="##other"/>` のように、名前空間が定義されていない **xsd:any** 要素を使用する場合です。このコンストラクトが省略可能な要素の後に続く場合は特に注意が必要です。前述の例をここでも使用し、次に示すように最後のノードのみを **xsd:any** 要素に置き換えて考えると、非決定論的かどうかに関する前述の説明がすべてここでも当てはまることがわかります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p132">The final questionable practice is using an **xsd:any** element without a namespace definition, as in  `<xsd:any namespace="##other"/>` , after an **xsd:sequence** element. This construct is especially troublesome when it follows an optional element. If you revisit the previous example and change just the last node to an **xsd:any** element, you can see that all the previous arguments about nondeterminism still apply, as follows:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:any />     
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="illegal-enumeration-values"></a><span data-ttu-id="cf09b-234">無効な列挙値</span><span class="sxs-lookup"><span data-stu-id="cf09b-234">Illegal Enumeration Values</span></span>

<span data-ttu-id="cf09b-p133">XSD スキーマは、通常、実際のインスタンス ドキュメントが検証されるまでは、どのような型検証も実行しません。ただし、スキーマに列挙体が含まれる場合は例外です。この場合は、列挙値が適切なノード値かどうかが列挙型に照らして検証されます。次に、2 つの例を紹介します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p133">XSD schemas typically do not perform any type validation until you validate an actual instance document. An exception to this is when you have an enumeration in your schema. In this case, the schema validates the enumeration values against the enumeration types to ensure they are proper node values. Here are two examples:</span></span>
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="cf09b-239">このスキーマは、"eleven o'clock" が **xsd:time** 型の要素に対して有効な値ではないため無効です。</span><span class="sxs-lookup"><span data-stu-id="cf09b-239">This schema is invalid because "eleven o'clock" is not a valid value for an element of type **xsd:time**.</span></span>
  
<span data-ttu-id="cf09b-240">これよりも複雑な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-240">The following is a more complex example:</span></span>
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="cf09b-p134">この例が正しくないことを理解するには、 **xsd:NMTOKEN** 型がどのように定義されているかを理解する必要があります。W3C によるデータ型仕様では、 **NMTOKEN** 型は「An NMTOKEN (name token) is any mixture of name characters (NMTOKEN (名前トークン) は名前文字の任意の組み合わせとする)」と定義されています。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p134">To understand why this example is invalid, you must understand how the type **xsd:NMTOKEN** is defined. The W3C data types specification defines the **NMTOKEN** type as follows: "An NMTOKEN (name token) is any mixture of name characters."</span></span> 
  
<span data-ttu-id="cf09b-243">さらに掘り下げて調べると、'&' が有効な名前文字ではないため、"M&Ms" は **NMTOKEN** 型として有効ではないことがわかります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-243">If you investigate further, you find that '' is not a valid name character, and therefore "MMs" does not validate as an NMTOKEN type.</span></span> 
  
## <a name="empty-sequence-or-choice-elements"></a><span data-ttu-id="cf09b-244">空のシーケンスまたは選択要素</span><span class="sxs-lookup"><span data-stu-id="cf09b-244">Empty Sequence or Choice Elements</span></span>

<span data-ttu-id="cf09b-245">MSXML では、次の例に示すような、空の **xsd:choice** 要素または **xsd:sequence** 要素を含むスキーマ宣言について、エラーが報告される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-245">MSXML sometimes raises errors about schema declarations that contain empty **xsd:choice** or **xsd:sequence** elements, as shown in the following example.</span></span> 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="cf09b-246">この問題は、空の  `<xsd:choice />` タグを削除することで解決します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-246">Removing the empty  `<xsd:choice />` tag should resolve this problem.</span></span> 
  
## <a name="regular-expressions"></a><span data-ttu-id="cf09b-247">正規表現</span><span class="sxs-lookup"><span data-stu-id="cf09b-247">Regular Expressions</span></span>

<span data-ttu-id="cf09b-p135">MSXML 5.0 では、読み込み時に正規表現パターンの検証で問題が生じる場合があります。正規表現は複雑になる場合があるため、慎重に使用する必要があります。XSD パーサーはどれも皆、柔軟な正規表現言語を採用しているように見えますが、それは、公式の XSD 正規表現言語に加えて、他の正規表現言語の要素も実装しているからです。InfoPath のフォーム デザイン ウィンドウで正規表現の解析に問題が生じる場合は、InfoPath で生成されるサンプル データが無効であるか、まったく生成されていないことが考えられます。これはデザイン時には、サンプル データが書式設定にしか使用されないため問題にはなりません。ただし、MSXML がサポートしていない正規表現を使用する場合は、ユーザーがフォームに記入する際に、InfoPath でその正規表現に照らして値を検証できません。「[XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)」では、XSD 正規表現のサポート内容について説明しています。XSD 正規表現と Unicode レベル 1 の正規表現の詳細については、「[Unicode Regular Expressions (英語)](http://www.unicode.org/reports/tr18/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p135">MSXML 5.0 can have problems validating regular expression patterns on load. Regular expressions can be complicated, and you should be careful when you are using them. Every XSD parser seems to have flexible regular expression languages; that is, they implement the official XSD regular expression language plus elements from other regular expression languages. If InfoPath form designer has problems parsing a regular expression, then the sample data InfoPath generates might be invalid or might not be generated at all. This is acceptable at design time, because InfoPath uses only sample data for formatting. However, if you use a regular expression that MSXML does not support, then InfoPath cannot validate a value against it when a user is filling out a form. [XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions. For more information about XSD regular expressions and Unicode level 1 regular expressions, see [Unicode Regular Expressions](http://www.unicode.org/reports/tr18/) .</span></span> 
  
## <a name="targetnamespace-attribute-issues"></a><span data-ttu-id="cf09b-256">targetNamespace 属性に関する問題</span><span class="sxs-lookup"><span data-stu-id="cf09b-256">targetNamespace Attribute Issues</span></span>

<span data-ttu-id="cf09b-p136">XSD の興味深い点として、 **targetNamespace** 属性では既定で最上位の宣言のみ参照されるが、  `attributeFormDefault=qualified` および  `elementFormDefault=qualified` を設定すると既定の動作を上書き変更できることが挙げられます。例として、次の XSD を想定します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p136">XSD is interesting in that, by default, the **targetNamespace** attribute refers to only the top-level declarations, although you can set  `attributeFormDefault=qualified` and  `elementFormDefault=qualified` to override this default behavior. As an example, assume that you have the following XSD.</span></span> 
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

<span data-ttu-id="cf09b-259">また、XML インスタンス ドキュメントは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-259">And that, your XML instance document resembles the following example.</span></span>
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

<span data-ttu-id="cf09b-p137">ローカル定義では、名前空間による修飾は既定で無効なため、ターゲットの名前空間の指定は不要です。ただし、ローカル定義をグローバルに変更する場合は、参照先 (ref) を名前空間プレフィックスで修飾する必要があります。たとえば、次のスキーマは正しくありません。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p137">Local definitions do not require the target namespace because qualification is turned off by default. However, if you change your local definition to be global, then your reference must be qualified with the namespace prefix. For example, the following schema is invalid.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="cf09b-p138">"global" は名前空間 "http://ns" 内にあるため、このスキーマは正しくありません。既定の名前空間は "http://ns" ではないため、単純に ref="global" と指定しただけでは正しく認識されません。この問題を解決するには、ターゲットの名前空間のプレフィックスを追加し、すべてのグローバル参照と型の使用時にこのプレフィックスを使用する必要があります。修正後のスキーマは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p138">This schema is invalid because "global" is in the namespace "http://ns". The simple ref="global" is not recognized because the default namespace is not "http://ns". To fix this, you must add a prefix for the target namespace and use that for all global references and type uses. The corrected schema looks like the following.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"  
    xmlns:ns="http://ns" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="ns:global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="cf09b-267">スキーマで **targetNamespace** 属性が指定されている場合は、すべてのグローバル参照を適切な名前空間プレフィックスで修飾してください。</span><span class="sxs-lookup"><span data-stu-id="cf09b-267">If your schema has the **targetNamespace** attribute specified, ensure that all global references are qualified with the correct namespace prefix.</span></span> 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a><span data-ttu-id="cf09b-268">XML 処理命令でのエンコーディング (Unicode または ANSII) の指定</span><span class="sxs-lookup"><span data-stu-id="cf09b-268">XML Processing Instruction Encoding (Unicode vs. ANSII)</span></span>

<span data-ttu-id="cf09b-p139">XML は、Unicode 文字セットのみをサポートしています。したがって、ANSII 文字を使用するファイルを保存すると情報が失われる可能性があります。ただし、この特定の用途では、ファイルを UTF-16 形式で保存する必要はありません。XML リーダーの実装コストを削減するために、XML 作成者は使用するエンコーディングを最上位の処理命令タグで指定する必要があります。たとえば、次のような処理命令を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p139">XML supports only Unicode character sets. Therefore, you may lose information if you save files that use ANSII characters. However, saving files as UTF-16 may be excessive for your particular use. To reduce the implementation cost of an XML reader, the XML author must state which encoding they are using in the top-level XML processing instruction. You may recognize the following processing instruction.</span></span>
  
```XML
xml version="1.0" encoding="UTF-8"
```

<span data-ttu-id="cf09b-p140">この処理命令タグでは、ファイルのエンコーディングとして UTF-8 が指定されています。ファイル内のエンコーディングは、処理命令タグで指定したエンコーディングと同一にする必要があります。ファイルのエンコーディングは、ファイル内のバイトを調べて Unicode のバイト オーダー マークを探すことにより確認できます。ただし、それよりも簡単な方法があります。XSD スキーマを開く際に問題が生じる場合は、エンコーディングとして "UTF-8" を指定し、スキーマをメモ帳などのテキスト エディターで開いてから、UTF-8 エンコーディングでファイルを保存します (メモ帳には、[ **名前を付けて保存**] ダイアログ ボックスに [ **エンコード**] ドロップダウン リストがあります)。それでもファイルを開く際に問題がある場合、原因はエンコーディングではありません。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p140">This processing instruction tag specifies that the encoding of the file is UTF-8. You must ensure that the file encoding is the same as the encoding stated in the processing instruction tag. You can determine the encoding by looking at the bytes of the file and looking for the Unicode byte order marks. But there is an easier way. If you have problems opening an XSD schema, specify the encoding as "UTF-8", open it in a text editor such as Notepad, and then save the file by using UTF-8 encoding (Notepad provides the **Encoding** drop-down list in the **Save As** dialog box). If you still have problems opening the file, it is not an encoding issue.</span></span> 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a><span data-ttu-id="cf09b-280">xsd:all 要素内の maxOccurs 属性</span><span class="sxs-lookup"><span data-stu-id="cf09b-280">maxOccurs Attribute Inside the xsd:all Element</span></span>

<span data-ttu-id="cf09b-p141">XML Schema 勧告における非決定論の定義に基づくと、 **xsd:all** 要素内の **xsd:element** 要素の **maxOccurs** 属性に対して有効な値は 1 のみになります。たとえば、次は正しい例です。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p141">Due to the way nondeterminism is defined in the XML Schema recommendation, the only valid value for the **maxOccurs** attribute of an **xsd:element** element inside an **xsd:all** element is 1. For example, the following is valid.</span></span> 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

<span data-ttu-id="cf09b-283">しかし、次の例は正しくありません。</span><span class="sxs-lookup"><span data-stu-id="cf09b-283">However, this example is not valid.</span></span>
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

<span data-ttu-id="cf09b-p142">この例が正しくない理由は、 `<x/>` が 2 回出現する場合に、この例の単一の宣言に対応しているのか、この宣言とは別の無効な定義に対応しているのかを検証システムで判断できないためです。同様に、  `<xsd:all>` タグ内に同じ名前の要素を 2 つ含めることもできません。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p142">This example is invalid because the validation system cannot determine whether two occurrences of  `<x/>` map to the single declaration or to the declaration and another invalid definition. Along the same lines, you cannot have two elements of the same name in an  `<xsd:all>` tag.</span></span> 
  
<span data-ttu-id="cf09b-p143">これは、任意の数の  `<x/>` ノードと  `<docs/>` ノードを任意の順序で親要素内に含められるという点で興味深い例です。このままでは無効ですが、別の方法で記述すれば正しい構造になります。次の例に示すように **xsd:choice** 要素を使用すると、意図した結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p143">This example is also interesting because it allows you to have any number of  `<x/>` and  `<docs/>` nodes inside a containing element in any order. Although this construct is invalid, there is a workaround. By using the **xsd:choice** element, you can achieve the same result, as demonstrated in the following example.</span></span> 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a><span data-ttu-id="cf09b-289">InfoPath 用に XSD を編集または作成する方法</span><span class="sxs-lookup"><span data-stu-id="cf09b-289">How to Edit or Author an XSD for InfoPath</span></span>

<span data-ttu-id="cf09b-290">ここでは 2 つの例を使用して、InfoPath で特定の結果を得られるようにスキーマを編集または作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cf09b-290">The two examples in the following sections show how to edit or author a schema to produce specific results in InfoPath.</span></span>
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a><span data-ttu-id="cf09b-291">[フィールド] 作業ウィンドウにユーザー定義の要素を挿入できるようにする</span><span class="sxs-lookup"><span data-stu-id="cf09b-291">Allowing User-defined Elements to Be Inserted in the Fields Task Pane</span></span>

<span data-ttu-id="cf09b-p144">[ **フィールド**] 作業ウィンドウで親要素の下にユーザー定義の要素を表示できるようにする場合は、該当する親要素の下に **xsd:any** 要素を挿入する必要があります。  `<your_node_name>` 内にユーザー定義の要素を挿入できるようにする場合は、次のような XSD 宣言が必要です。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p144">To allow user-defined elements to appear under a parent element in the **Fields** task pane, you must insert an **xsd:any** element under the parent element. To allow user-defined elements to be inserted inside  `<your_node_name>` , the XSD declaration should resemble the following.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="##any | ##other"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="cf09b-294">ユーザー定義の属性を使用できるようにする場合は、要素宣言に  `<xsd:anyAttribute namespace="##any | ##other"/>` を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-294">If you also want to allow user-defined attributes, then you must add  `<xsd:anyAttribute namespace="##any | ##other"/>` to the element declaration.</span></span> 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a><span data-ttu-id="cf09b-295">InfoPath のデザイン モードと編集モードでリッチ テキスト要素をバインドできるようにする</span><span class="sxs-lookup"><span data-stu-id="cf09b-295">Allowing Rich Text Elements to be Bound in InfoPath Design and Edit Modes</span></span>

<span data-ttu-id="cf09b-296">**Rich Text Box** コントロールにバインドできるように要素を宣言する場合は、次の例に示すように、namespace 属性を "****" に設定した http://www.w3.org/1999/xhtml 要素を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf09b-296">If you want to declare an element that can be bound to a **Rich Text Box** control, then it should have the following form, which includes the **xsd:any** element that has a namespace attribute set to "http://www.w3.org/1999/xhtml" as shown in the following example.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a><span data-ttu-id="cf09b-297">終わりに</span><span class="sxs-lookup"><span data-stu-id="cf09b-297">Conclusion</span></span>

<span data-ttu-id="cf09b-p145">外部で作成された XML スキーマ (.xsd) ファイルに基づく XML フォーム ソリューションのデザインに関する InfoPath のサポートを有効活用することで、業界標準のスキーマまたは所属する会社や組織で作成したカスタム スキーマと連携するフォーム テンプレートを作成できます。この記事で解説した内容を参考にして、InfoPath と互換性のあるカスタムの XSD スキーマ ファイルを作成し、外部で作成された XSD ファイルを InfoPath のデザイン環境に読み込む際によく発生する問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="cf09b-p145">By taking advantage of InfoPath support for designing XML form solutions that are based on externally authored XML Schema (.xsd) files, you can create a form template that works with an industry-standard schema or custom schema created by your company or organization. By using the information in this article, you can create custom XSD schema files that are compatible with InfoPath, and you can troubleshoot common issues that you may encounter when you load externally authored XSD files into the InfoPath design environment.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf09b-300">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf09b-300">See also</span></span>

- [<span data-ttu-id="cf09b-301">W3C XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="cf09b-301">W3C XML Schema</span></span>](http://www.w3.org/XML/Schema)
- [<span data-ttu-id="cf09b-302">W3C XML Schema Primer</span><span class="sxs-lookup"><span data-stu-id="cf09b-302">W3C XML Schema Primer</span></span>](http://www.w3.org/TR/xmlschema-0/)
- [<span data-ttu-id="cf09b-303">W3C XML Schema Structures Reference (英語)</span><span class="sxs-lookup"><span data-stu-id="cf09b-303">W3C XML Schema Structures Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [<span data-ttu-id="cf09b-304">W3C XML Schema Datatypes Reference (英語)</span><span class="sxs-lookup"><span data-stu-id="cf09b-304">W3C XML Schema Datatypes Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [<span data-ttu-id="cf09b-305">XML Schema Tutorial (英語)</span><span class="sxs-lookup"><span data-stu-id="cf09b-305">XML Schema Tutorial</span></span>](http://www.w3schools.com/schema/default.asp)
- [<span data-ttu-id="cf09b-306">データ プラットフォーム デベロッパー センター (英語)</span><span class="sxs-lookup"><span data-stu-id="cf09b-306">XML Developer Center</span></span>](http://msdn.microsoft.com/ja-JP/xml/default.aspx)

