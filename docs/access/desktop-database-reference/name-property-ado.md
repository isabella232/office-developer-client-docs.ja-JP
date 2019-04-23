---
title: Name プロパティ (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288666"
---
# <a name="name-property-ado"></a>Name プロパティ (ADO)


**適用先:** Access 2013、Office 2013

オブジェクトの名前を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

オブジェクトの名前を示す文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**Name** プロパティは、**Command** オブジェクト、**Property** オブジェクト、**Field** オブジェクト、または **Parameter**  オブジェクトの名前を設定または取得するために使用します。

値は、 **Command** オブジェクトでは読み取り/書き込み可能で、 **Property** オブジェクトでは読み取り専用になります。

**Field** オブジェクトの場合、 **Name** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **Name** は読み取り/書き込み可能になります。

**Parameters** コレクションに追加されていない [Parameter](parameters-collection-ado.md) オブジェクトでは、 **Name** プロパティは読み取り/書き込み可能です。追加された **Parameter** オブジェクトとその他のオブジェクトでは、 **Name** プロパティは読み取り専用です。名前はコレクション内で一意でなくてもかまいません。

オブジェクトの **Name** は、序数参照で取得でき、その後は、その名前で直接オブジェクトを参照できます。 たとえば、rstmain プロパティ (20) を使用します。Name は更新可能になり、後でこのプロパティを参照すると、更新の更新が可能になり、このプロパティを rstmain. プロパティ ("更新可能性") と呼ぶことができます。

