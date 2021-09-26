---
title: Delete メソッド (ADO Parameters Collection)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 30545ef12b5f794985b4925fe242e360ed1576f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622383"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete メソッド (ADO Parameters Collection)

**適用先**: Access 2013、Office 2013

[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*パラメーター*。インデックスの *削除*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Index* |削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。|

## <a name="remarks"></a>注釈

コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、[Command](command-object-ado.md) オブジェクトの **Parameters** コレクションでのみ使用できます。**Delete** メソッドを呼び出すときは、[Parameter](parameter-object-ado.md) オブジェクトの [Name](name-property-ado.md) プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。

