---
title: Name プロパティ (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 42b543481e023e10dd79cd42302a5f5f8c98bf93
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626275"
---
# <a name="name-property-ado"></a>Name プロパティ (ADO)


**適用先**: Access 2013、Office 2013

オブジェクトの名前を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

オブジェクトの名前を示す文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

**Name** プロパティは、**Command** オブジェクト、**Property** オブジェクト、**Field** オブジェクト、または **Parameter**  オブジェクトの名前を設定または取得するために使用します。

値は、 **Command** オブジェクトでは読み取り/書き込み可能で、 **Property** オブジェクトでは読み取り専用になります。

**Field** オブジェクトの場合、 **Name** は一般には読み取り専用です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されていて、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合に限り、 **Name** は読み取り/書き込み可能になります。

**Parameters** コレクションに追加されていない [Parameter](parameters-collection-ado.md) オブジェクトでは、 **Name** プロパティは読み取り/書き込み可能です。追加された **Parameter** オブジェクトとその他のオブジェクトでは、 **Name** プロパティは読み取り専用です。名前はコレクション内で一意でなくてもかまいません。

オブジェクトの **Name** は、序数参照で取得でき、その後は、その名前で直接オブジェクトを参照できます。 たとえば、rstMain.Properties(20) の場合です。Name yields Updatability , you can refer to this property as yields Updatability , you can refer to this property as rstMain.Properties("Updatability") .

