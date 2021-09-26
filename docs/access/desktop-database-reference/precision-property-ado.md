---
title: Precision プロパティ (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f176bb08d757d94b11b9f407177fa27dacf76b70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622124"
---
# <a name="precision-property-ado"></a>Precision プロパティ (ADO)


**適用先**: Access 2013、Office 2013

[Parameter](parameter-object-ado.md) オブジェクト内の数値または数値型の [Field](field-object-ado.md) オブジェクトの精度を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

値を表すために使用する最大桁数を示すバイト型 (**Byte**) の値を設定または取得します。

## <a name="remarks"></a>注釈

数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値を表すために使用する最大桁数を調べるには、**Precision** プロパティを使用します。

**Parameter** オブジェクトでは、値の設定および取得が可能です。

**Field** オブジェクトの場合は、 **Precision** は通常、値の取得のみ可能です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Precision** の値の設定および取得が可能になります。

