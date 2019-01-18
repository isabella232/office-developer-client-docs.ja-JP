---
title: Property.Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e7c79fe12b3b7bfe98e0c7547f4ed2d12b148ba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713381"
---
# <a name="propertyvalue-property-dao"></a>Property.Value プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( **Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。値

*式***Property**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。

通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。

**Value** プロパティは、 **Field**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、プロパティを直接参照してこれらのオブジェクトいずれかの値を設定または取得できます。

不適切なコンテキスト (たとえば、 **TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクトの **Value** プロパティ) で **Value** プロパティを設定または取得しようとすると、トラップ可能なエラーが発生します。

> [!NOTE]
> Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。


