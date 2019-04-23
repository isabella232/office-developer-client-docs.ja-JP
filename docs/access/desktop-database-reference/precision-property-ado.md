---
title: Precision プロパティ (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287476"
---
# <a name="precision-property-ado"></a>Precision プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Parameter](parameter-object-ado.md) オブジェクト内の数値または数値型の [Field](field-object-ado.md) オブジェクトの精度を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

値を表すために使用する最大桁数を示すバイト型 (**Byte**) の値を設定または取得します。

## <a name="remarks"></a>注釈

数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値を表すために使用する最大桁数を調べるには、**Precision** プロパティを使用します。

**Parameter** オブジェクトでは、値の設定および取得が可能です。

**Field** オブジェクトの場合は、 **Precision** は通常、値の取得のみ可能です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Precision** の値の設定および取得が可能になります。

