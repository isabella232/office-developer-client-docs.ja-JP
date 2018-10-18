---
<span data-ttu-id="845f5-101"><<<<<<< ヘッド タイトル: 属性プロパティ (ADO) TOCTitle: 属性プロパティ (ADO) === タイトル: 属性のプロパティ (ADO) TOCTitle: 属性のプロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="845f5-101"><<<<<<< HEAD title: Attributes Property (ADO) TOCTitle: Attributes Property (ADO) ======= title: Attributes property (ADO) TOCTitle: Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="845f5-102">マスターの ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 2015/09/18 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="845f5-102">master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="845f5-103">ado210.chm1231117 f1_categories。</span><span class="sxs-lookup"><span data-stu-id="845f5-103">ado210.chm1231117 f1_categories:</span></span>
- <span data-ttu-id="845f5-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="845f5-104">Office.Version=v15</span></span>
---

<span data-ttu-id="845f5-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="845f5-105"><<<<<<< HEAD</span></span>
# <a name="attributes-property-ado"></a><span data-ttu-id="845f5-106">Attributes プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="845f5-106">Attributes Property (ADO)</span></span>
=======
# <a name="attributes-property-ado"></a><span data-ttu-id="845f5-107">Attributes プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="845f5-107">Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="845f5-108">master</span><span class="sxs-lookup"><span data-stu-id="845f5-108">master</span></span>


<span data-ttu-id="845f5-109">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="845f5-109">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="845f5-110">Attributes プロパティ</span><span class="sxs-lookup"><span data-stu-id="845f5-110">Attributes Property</span></span>

<span data-ttu-id="845f5-111">オブジェクトの 1 つまたは複数の属性を示します。</span><span class="sxs-lookup"><span data-stu-id="845f5-111">Indicates one or more characteristics of an object.</span></span>

<span data-ttu-id="845f5-112"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="845f5-112"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="845f5-113">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="845f5-113">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="845f5-114">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="845f5-114">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="845f5-115">master</span><span class="sxs-lookup"><span data-stu-id="845f5-115">master</span></span>

<span data-ttu-id="845f5-116">長整数型 ( **Long** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="845f5-116">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="845f5-p101">[Connection](connection-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得および設定が可能で、その値は 1 つまたは複数の [XactAttributeEnum](xactattributeenum.md) 値の合計になります。既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="845f5-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="845f5-p102">[Parameter](parameter-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得および設定が可能で、その値は 1 つまたは複数の [ParameterAttributesEnum](parameterattributesenum.md) 値の合計になります。既定値は **adParamSigned** です。</span><span class="sxs-lookup"><span data-stu-id="845f5-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="845f5-p103">[Field](field-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは、1 つまたは複数の [FieldAttributeEnum](fieldattributeenum.md) 値の合計になります。通常は値の取得のみ可能ですが、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新しい [Field](record-object-ado.md) オブジェクトの場合は、 **Field** の [Value](value-property-ado.md) プロパティを指定し、 **Fields** コレクションの **Update** メソッドを呼び出すことによって新しい [Field](update-method-ado.md) がデータ プロバイダーによって正常に追加された直後にのみ、 **Attributes** の値の取得と設定の両方が可能になります。</span><span class="sxs-lookup"><span data-stu-id="845f5-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="845f5-123">[Property](property-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得のみ可能で、その値は 1 つまたは複数の [PropertyAttributesEnum](propertyattributesenum.md) 値の合計になります。</span><span class="sxs-lookup"><span data-stu-id="845f5-123">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="845f5-124">解説</span><span class="sxs-lookup"><span data-stu-id="845f5-124">Remarks</span></span>

<span data-ttu-id="845f5-125">**Attributes** プロパティを使用すると、 **Connection** オブジェクト、 **Parameter** オブジェクト、 [Field](field-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトの属性を設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="845f5-125">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="845f5-p104">複数の属性を設定する場合は、該当する定数の合計を使用できます。プロパティの値を、互換性のない定数を含む合計に設定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="845f5-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="845f5-128">**リモート データ サービスの使用法**このプロパティはクライアント側の**接続**オブジェクトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="845f5-128">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

