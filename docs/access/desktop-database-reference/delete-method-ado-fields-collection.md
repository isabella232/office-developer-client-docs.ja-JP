---
title: Delete メソッド (ADO Fields Collection)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 463056a45ce3636d6b215c03fd65e8614f633bf3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577445"
---
# <a name="delete-method-ado-fields-collection"></a>Delete メソッド (ADO Fields Collection)

**適用先:** Access 2013、Office 2013


[Fields](fields-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*フィールド*。フィールドの *削除*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Field* |削除する **Field** オブジェクトを指定するバリアント型 ( [Variant](field-object-ado.md) ) の値です。このパラメーターには、 **Field** オブジェクトの名前または **Field** オブジェクト自体のインデックスを使用できます。|

## <a name="remarks"></a>注釈

**Fields.Delete** メソッドを開いている [Recordset](recordset-object-ado.md) に対して呼び出すと、実行時エラーが発生します。

