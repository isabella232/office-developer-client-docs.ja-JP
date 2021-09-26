---
title: Field.Type プロパティ (DAO)
TOCTitle: Type Property
description: Type プロパティ
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 082f6b34965ae90c99efd8d8cf3ac34d2cfc5dfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581295"
---
# <a name="fieldtype-property-dao"></a>Field.Type プロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 (**Integer**) の値を使用します。

## <a name="syntax"></a>構文

*expression* .Type

*expression*: **Field** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

設定値または戻り値は、操作の種類またはデータ型を示す定数です。 **Field** オブジェクトの場合、このプロパティは、オブジェクトがコレクションまたは他のオブジェクトに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。

次の表は、 **Field** オブジェクトで使用可能な設定値および戻り値を示しています。

|**定数**|**値**|**説明**|
|:----------|:----------|:----------|
|**dbBigInt**|16|多倍長整数型 (Big Integer)|
|**dbBinary**|9|Binary|
|**dbBoolean**|1|Boolean|
|**dbByte**|2|バイト型 (Byte)|
|**dbChar**|18|Char|
|**dbCurrency**|5|通貨|
|**dbDate**|8|日付/時刻|
|**dbDecimal**|20|Decimal|
|**dbDouble**|7|2 行分|
|**dbFloat**|21|浮動小数点数|
|**dbGUID**|15|GUID|
|**dbInteger**|3|整数|
|**dbLong**|4|Long|
|**dbLongBinary**|11|ロング バイナリ型 (Long Binary) - OLE オブジェクト型 (OLE Object)|
|**dbMemo**|12|メモ|
|**dbNumeric**|19|数値|
|**dbSingle**|6|1 行|
|**dbText**|10|テキスト|
|**dbTime**|22|Time|
|**dbTimeStamp**|23|タイム スタンプ|
|**dbVarBinary**|17|VarBinary|

新しい **Field** オブジェクト、 **Parameter** オブジェクト、または **Property** オブジェクトを **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **Recordset** オブジェクト、または **TableDef** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。
