---
title: Property オブジェクト (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302920"
---
# <a name="property-object-ado"></a>Property オブジェクト (ADO)


**適用先:** Access 2013、Office 2013

プロバイダーで定義される ADO オブジェクトの動的特性を表します。

## <a name="remarks"></a>注釈

ADO オブジェクトには、組み込みのプロパティと動的プロパティという 2 種類のプロパティがあります。

組み込みプロパティは、ADO で実装されているプロパティであり、構文を使用して、任意の新しいオブジェクトですぐに使用できます。 これらのプロパティは、オブジェクトの **Properties** コレクション内の [Property](properties-collection-ado.md) オブジェクトとして格納されないため、値の変更はできますが、特性を変更することはできません。

動的プロパティは、基になるデータ プロバイダーによって定義され、該当する ADO オブジェクトの **Properties** コレクションに含まれます。 たとえば、プロバイダー固有のプロパティには、 [Recordset](recordset-object-ado.md) オブジェクトがトランザクションや更新をサポートしているかどうかを示すものがあります。 これらの追加のプロパティは、その **Recordset** オブジェクトの **Properties** コレクションに、 **Property** オブジェクトとして格納されます。 動的プロパティは、MyObject プロパティ (0) または myobject プロパティ ("Name") の構文を使用して、コレクションを通じてのみ参照できます。

どちらの種類のプロパティも削除できません。

動的プロパティである **Property** オブジェクトには、それ自体に次の 4 つの組み込みのプロパティがあります。

  - [Name](name-property-ado.md) プロパティは、プロパティを識別する文字列です。

  - [Type](type-property-ado.md) プロパティは、プロパティのデータ型を指定する整数です。

  - [Value](value-property-ado.md) プロパティは、プロパティの設定を格納する変数です。 **Value** は、 **Property** オブジェクトの既定のプロパティです。

  - [Attributes](attributes-property-ado.md) プロパティは、プロバイダー固有のプロパティの特性を示す長整数型 (Long) の値です。

