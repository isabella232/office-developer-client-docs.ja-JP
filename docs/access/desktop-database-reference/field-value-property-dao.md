---
title: Field.Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7ed259b1af80f4bd5c51b833462318b6e4696ae
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936190"
---
# <a name="fieldvalue-property-dao"></a>Field.Value プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( **Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。値

*式***Field**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。

通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。

**Value** プロパティは、 **Field**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、プロパティを直接参照してこれらのオブジェクトいずれかの値を設定または取得できます。

不適切なコンテキスト (たとえば、 **TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクトの **Value** プロパティ) で **Value** プロパティを設定または取得しようとすると、トラップ可能なエラーが発生します。


> [!NOTE]
> Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。


