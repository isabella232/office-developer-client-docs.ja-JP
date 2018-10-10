---
title: Precision プロパティ (ADO)
TOCTitle: Precision Property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9e98227e98b4f731cd4d361ff6a2c5394058e86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479630"
---
# <a name="precision-property-ado"></a>Precision プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

[Parameter](parameter-object-ado.md) オブジェクト内の数値または数値型の [Field](field-object-ado.md) オブジェクトの精度を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

値を表すために使用する最大桁数を示すバイト型 ( **Byte** ) の値を設定または取得します。

## <a name="remarks"></a>解説

数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値を表すために使用する最大桁数を調べるには、 **Precision** プロパティを使用します。

**Parameter** オブジェクトでは、値の設定および取得が可能です。

**Field** オブジェクトの場合は、 **Precision** は通常、値の取得のみ可能です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Precision** の値の設定および取得が可能になります。

