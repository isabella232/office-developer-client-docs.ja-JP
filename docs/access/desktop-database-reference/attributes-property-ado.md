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
ms.localizationpriority: medium
ms.openlocfilehash: 0edebe425b025e3b3497640a7e436b5996493dae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558885"
---
# <a name="attributes-property-ado"></a>Attributes プロパティ (ADO)


**適用先:** Access 2013、Office 2013


## <a name="attributes-property"></a>Attributes プロパティ

オブジェクトの 1 つまたは複数の属性を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

長整数型 ( **Long** ) の値を設定または取得します。

[Connection](connection-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得および設定が可能で、その値は 1 つまたは複数の [XactAttributeEnum](xactattributeenum.md) 値の合計になります。既定値は 0 です。

[Parameter](parameter-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得および設定が可能で、その値は 1 つまたは複数の [ParameterAttributesEnum](parameterattributesenum.md) 値の合計になります。既定値は **adParamSigned** です。

[Field](field-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは、1 つまたは複数の [FieldAttributeEnum](fieldattributeenum.md) 値の合計になります。通常は値の取得のみ可能ですが、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新しい [Field](record-object-ado.md) オブジェクトの場合は、 **Field** の [Value](value-property-ado.md) プロパティを指定し、 **Fields** コレクションの **Update** メソッドを呼び出すことによって新しい [Field](update-method-ado.md) がデータ プロバイダーによって正常に追加された直後にのみ、 **Attributes** の値の取得と設定の両方が可能になります。

[Property](property-object-ado.md) オブジェクトの場合、 **Attributes** プロパティは値の取得のみ可能で、その値は 1 つまたは複数の [PropertyAttributesEnum](propertyattributesenum.md) 値の合計になります。

## <a name="remarks"></a>注釈

**Attributes** プロパティを使用すると、**Connection** オブジェクト、**Parameter** オブジェクト、[Field](field-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトの属性を設定または取得できます。

複数の属性を設定する場合は、該当する定数の合計を使用できます。プロパティの値を、互換性のない定数を含む合計に設定すると、エラーが発生します。

**リモート データ サービスの使用状況** このプロパティは、クライアント側の Connection オブジェクト **では使用** できません。

