---
title: Property オブジェクト (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a3fa2aad6506645db276d55d13257e8d2e2eafe5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565108"
---
# <a name="property-object-ado"></a>Property オブジェクト (ADO)


**適用先:** Access 2013、Office 2013

プロバイダーで定義される ADO オブジェクトの動的特性を表します。

## <a name="remarks"></a>注釈

ADO オブジェクトには、組み込みのプロパティと動的プロパティという 2 種類のプロパティがあります。

組み込みプロパティは、ADO に実装され、構文を使用して新しいオブジェクトですぐに使用できるプロパティです。 これらのプロパティは、オブジェクトの **Properties** コレクション内の [Property](properties-collection-ado.md) オブジェクトとして格納されないため、値の変更はできますが、特性を変更することはできません。

動的プロパティは、基になるデータ プロバイダーによって定義され、該当する ADO オブジェクトの **Properties** コレクションに含まれます。 たとえば、プロバイダー固有のプロパティには、 [Recordset](recordset-object-ado.md) オブジェクトがトランザクションや更新をサポートしているかどうかを示すものがあります。 これらの追加のプロパティは、その **Recordset** オブジェクトの **Properties** コレクションに、 **Property** オブジェクトとして格納されます。 動的プロパティは、MyObject.Properties(0) 構文または MyObject.Properties("Name") 構文を使用して、コレクションを通じてのみ参照できます。

どちらの種類のプロパティも削除できません。

動的プロパティである **Property** オブジェクトには、それ自体に次の 4 つの組み込みのプロパティがあります。

  - [Name](name-property-ado.md) プロパティは、プロパティを識別する文字列です。

  - [Type](type-property-ado.md) プロパティは、プロパティのデータ型を指定する整数です。

  - [Value](value-property-ado.md) プロパティは、プロパティの設定を格納する変数です。 **Value** は、 **Property** オブジェクトの既定のプロパティです。

  - [Attributes](attributes-property-ado.md) プロパティは、プロバイダー固有のプロパティの特性を示す長整数型 (Long) の値です。

