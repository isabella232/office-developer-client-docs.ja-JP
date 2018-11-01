---
title: Property オブジェクト (ADO)
TOCTitle: Property Object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fe6ac64417c5758d25872a7b67be7cb9f12ac6d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874510"
---
# <a name="property-object-ado"></a>Property オブジェクト (ADO)


**適用されます**Access 2013、Office 2013。

プロバイダーで定義される ADO オブジェクトの動的特性を表します。

## <a name="remarks"></a>備考

ADO オブジェクトには、組み込みのプロパティと動的プロパティという 2 種類のプロパティがあります。

組み込みのプロパティは、これらのプロパティは、ADO に実装されていると、構文を使用して、すべての新しいオブジェクトにすぐに利用可能です。 これらのプロパティは、オブジェクトの **Properties** コレクション内の [Property](properties-collection-ado.md) オブジェクトとして格納されないため、値の変更はできますが、特性を変更することはできません。

動的プロパティは、基になるデータ プロバイダーによって定義され、該当する ADO オブジェクトの **Properties** コレクションに含まれます。 たとえば、プロバイダー固有のプロパティには、 [Recordset](recordset-object-ado.md) オブジェクトがトランザクションや更新をサポートしているかどうかを示すものがあります。 これらの追加のプロパティは、その **Recordset** オブジェクトの **Properties** コレクションに、 **Property** オブジェクトとして格納されます。 動的プロパティは、MyObject.Properties(0) を使用して、このコレクションを通じてのみ参照できるか、または MyObject.Properties("Name") の構文です。

どちらの種類のプロパティも削除できません。

動的プロパティである **Property** オブジェクトには、それ自体に次の 4 つの組み込みのプロパティがあります。

  - [Name](name-property-ado.md) プロパティは、プロパティを識別する文字列です。

  - [Type](type-property-ado.md) プロパティは、プロパティのデータ型を指定する整数です。

  - [Value](value-property-ado.md) プロパティは、プロパティの設定を格納する変数です。 **Value** は、 **Property** オブジェクトの既定のプロパティです。

  - [Attributes](attributes-property-ado.md) プロパティは、プロバイダー固有のプロパティの特性を示す長整数型 (Long) の値です。

