---
title: Precision プロパティ (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db2000c2db48215df42b5cd81fb35be0f0c4be9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869961"
---
# <a name="precision-property-ado"></a>Precision プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Parameter](parameter-object-ado.md) オブジェクト内の数値または数値型の [Field](field-object-ado.md) オブジェクトの精度を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

値を表すために使用する最大桁数を示すバイト型 ( **Byte** ) の値を設定または取得します。

## <a name="remarks"></a>解説

数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値を表すために使用する最大桁数を調べるには、 **Precision** プロパティを使用します。

**Parameter** オブジェクトでは、値の設定および取得が可能です。

**Field** オブジェクトの場合は、 **Precision** は通常、値の取得のみ可能です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Precision** の値の設定および取得が可能になります。

