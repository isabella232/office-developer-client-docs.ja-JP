---
title: numericscale プロパティ (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288554"
---
# <a name="numericscale-property-ado"></a>numericscale プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Parameter](parameter-object-ado.md) オブジェクトまたは [Field](field-object-ado.md) オブジェクトの数値の桁数を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

数値の小数点以下の桁数を示すバイト型 (**Byte**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**NumericScale** プロパティは、数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値の小数点以下の桁数を取得するために使用します。

**Parameter** オブジェクトでは、 **NumericScale** は読み取り/書き込み可能です。

**Field** オブジェクトの場合、 **NumericScale** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **NumericScale** は読み取り/書き込み可能になります。

