---
title: Delete メソッド (ADO Fields コレクション)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fc2e614916026effe6ee0a9766e0b23db200574
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886397"
---
# <a name="delete-method-ado-fields-collection"></a>Delete メソッド (ADO Fields コレクション)


**適用されます**Access 2013、Office 2013。



[Fields](fields-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*フィールド*です。*フィールド*を削除します。

## <a name="parameters"></a>パラメーター

  - *Field*

  - 削除する **Field** オブジェクトを指定するバリアント型 ( [Variant](field-object-ado.md) ) の値です。このパラメーターには、 **Field** オブジェクトの名前または **Field** オブジェクト自体のインデックスを使用できます。

## <a name="remarks"></a>解説

**Fields.Delete** メソッドを開いている [Recordset](recordset-object-ado.md) に対して呼び出すと、実行時エラーが発生します。

