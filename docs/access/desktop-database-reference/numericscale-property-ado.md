---
title: NumericScale プロパティ (ADO)
TOCTitle: NumericScale Property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d70144ae886f60285ad22067e0c52b9193a0005
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479182"
---
# <a name="numericscale-property-ado"></a>NumericScale プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

[Parameter](parameter-object-ado.md) オブジェクトまたは [Field](field-object-ado.md) オブジェクトの数値の桁数を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

数値の小数点以下の桁数を示すバイト型 ( **Byte** ) の値を設定または取得します。

## <a name="remarks"></a>解説

**NumericScale** プロパティは、数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値の小数点以下の桁数を取得するために使用します。

**Parameter** オブジェクトでは、 **NumericScale** は読み取り/書き込み可能です。

**Field** オブジェクトの場合、 **NumericScale** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **NumericScale** は読み取り/書き込み可能になります。

