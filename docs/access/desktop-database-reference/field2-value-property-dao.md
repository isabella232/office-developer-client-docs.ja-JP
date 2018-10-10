---
title: Field2.Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ae14ee13c0b94a477550b0f20cec2e1fc31fdd6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478102"
---
# <a name="field2value-property-dao"></a>Field2.Value プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( **Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。値

*式***Field2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。

通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。

**Value** プロパティは、 **Field2**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、プロパティを直接参照してこれらのオブジェクトいずれかの値を設定または取得できます。

正しくない状況で **Value** プロパティの設定または取得を行うと (たとえば、 **TableDef** オブジェクトの **Fields** コレクション内にある **Field2** オブジェクトの **Value** プロパティ)、トラップ可能なエラーが発生します。


> [!NOTE]
> <P>Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。</P>


