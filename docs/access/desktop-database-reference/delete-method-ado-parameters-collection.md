---
title: Delete メソッド (ADO Parameters コレクション)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294093"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete メソッド (ADO Parameters コレクション)

**適用先:** Access 2013、Office 2013

[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*パラメーター*。*インデックス*の削除

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Index* |削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。|

## <a name="remarks"></a>注釈

コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、[Command](command-object-ado.md) オブジェクトの **Parameters** コレクションでのみ使用できます。**Delete** メソッドを呼び出すときは、[Parameter](parameter-object-ado.md) オブジェクトの [Name](name-property-ado.md) プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。

