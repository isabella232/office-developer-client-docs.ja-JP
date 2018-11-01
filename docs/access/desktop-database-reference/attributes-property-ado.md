---
title: Attributes プロパティ (ADO)
TOCTitle: Attributes property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ea253515a673f0f941032e2920d84c7ebf68f1bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874819"
---
# <a name="attributes-property-ado"></a><span data-ttu-id="4e7e4-102">Attributes プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="4e7e4-102">Attributes property (ADO)</span></span>


<span data-ttu-id="4e7e4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="4e7e4-104">Attributes プロパティ</span><span class="sxs-lookup"><span data-stu-id="4e7e4-104">Attributes Property</span></span>

<span data-ttu-id="4e7e4-105">オブジェクトの 1 つまたは複数の属性を示します。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-105">Indicates one or more characteristics of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4e7e4-106">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="4e7e4-106">Settings and return values</span></span>

<span data-ttu-id="4e7e4-107">長整数型 ( **Long** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-107">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="4e7e4-p101">[Connection](connection-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得および設定が可能で、その値は 1 つまたは複数の [XactAttributeEnum](xactattributeenum.md) 値の合計になります。既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="4e7e4-p102">[Parameter](parameter-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得および設定が可能で、その値は 1 つまたは複数の [ParameterAttributesEnum](parameterattributesenum.md) 値の合計になります。既定値は **adParamSigned** です。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="4e7e4-p103">[Field](field-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは、1 つまたは複数の [FieldAttributeEnum](fieldattributeenum.md) 値の合計になります。通常は値の取得のみ可能ですが、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新しい [Field](record-object-ado.md) オブジェクトの場合は、 **Field** の [Value](value-property-ado.md) プロパティを指定し、 **Fields** コレクションの **Update** メソッドを呼び出すことによって新しい [Field](update-method-ado.md) がデータ プロバイダーによって正常に追加された直後にのみ、 **Attributes** の値の取得と設定の両方が可能になります。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="4e7e4-114">[Property](property-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得のみ可能で、その値は 1 つまたは複数の [PropertyAttributesEnum](propertyattributesenum.md) 値の合計になります。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-114">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7e4-115">解説</span><span class="sxs-lookup"><span data-stu-id="4e7e4-115">Remarks</span></span>

<span data-ttu-id="4e7e4-116">**Attributes** プロパティを使用すると、 **Connection** オブジェクト、 **Parameter** オブジェクト、 [Field](field-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトの属性を設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-116">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="4e7e4-p104">複数の属性を設定する場合は、該当する定数の合計を使用できます。プロパティの値を、互換性のない定数を含む合計に設定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="4e7e4-119">**リモート データ サービスの使用法**このプロパティはクライアント側の**接続**オブジェクトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="4e7e4-119">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

