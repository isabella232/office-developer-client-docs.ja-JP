---
title: Delete メソッド (ADO Fields コレクション)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294107"
---
# <a name="delete-method-ado-fields-collection"></a>Delete メソッド (ADO Fields コレクション)

**適用先:** Access 2013、Office 2013


[Fields](fields-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*フィールド*。*フィールド*の削除

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Field* |削除する **Field** オブジェクトを指定するバリアント型 ( [Variant](field-object-ado.md) ) の値です。このパラメーターには、 **Field** オブジェクトの名前または **Field** オブジェクト自体のインデックスを使用できます。|

## <a name="remarks"></a>注釈

**Fields.Delete** メソッドを開いている [Recordset](recordset-object-ado.md) に対して呼び出すと、実行時エラーが発生します。

