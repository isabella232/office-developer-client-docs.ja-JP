---
title: Type プロパティ (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 646284877722baf9aec6bb591b071667fdf9cc1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867728"
---
# <a name="type-property-ado"></a>Type プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Parameter](parameter-object-ado.md) オブジェクト、 [Field](field-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトの操作の種類またはデータ型を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

[DataTypeEnum](datatypeenum.md) 値を設定または取得します。

## <a name="remarks"></a>解説

**Parameter** オブジェクトの場合、 **Type** プロパティは値の取得および設定が可能です。 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Type** の値の設定および取得が可能になります。

その他のすべてのオブジェクトでは、 **Type** プロパティは値の取得のみ可能です。

