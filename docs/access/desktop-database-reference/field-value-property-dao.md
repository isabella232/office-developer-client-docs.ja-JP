---
title: Field.Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 305b94655d46dcbd089f1bfde5b2b0482fdde23f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597304"
---
# <a name="fieldvalue-property-dao"></a>Field.Value プロパティ (DAO)


**適用先**: Access 2013、Office 2013

オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( **Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式* .値

*expression*: **Field** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。

通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。

**Value** プロパティは、 **Field**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、これらのオブジェクトいずれかを直接参照してその値を設定または取得できます。

正しくない状況で **Value** プロパティの設定または取得を行うと (たとえば、 **TableDef** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **Value** プロパティ)、トラップ可能なエラーが発生します。


> [!NOTE]
> Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。


