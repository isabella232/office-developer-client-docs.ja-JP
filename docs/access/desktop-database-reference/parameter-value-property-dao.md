---
title: パラメーター Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4e7f3976b934c407a038f321953259fd63a6f60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287992"
---
# <a name="parametervalue-property-dao"></a>パラメーター Value プロパティ (DAO)

**適用先:** Access 2013、Office 2013

オブジェクトの値を設定または取得します。 値の取得と設定が可能なバリアント型 (**Variant**) の値です。

## <a name="syntax"></a>構文

*式*。金額

*式***Parameter**オブジェクトを表す変数を指定します。

## <a name="remarks"></a>注釈

設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。

通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。

**Value** プロパティは、 **Field**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、これらのオブジェクトいずれかを直接参照してその値を設定または取得できます。

正しくない状況で **Value** プロパティの設定または取得を行うと (たとえば、 **TableDef** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **Value** プロパティ)、トラップ可能なエラーが発生します。

> [!NOTE]
> Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。


