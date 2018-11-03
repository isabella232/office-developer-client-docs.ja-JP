---
title: メソッド (ADO Parameters コレクション) を削除します。
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b18a09d6a0c9d6a6ad8e9f579068c4f6d7162d1f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944873"
---
# <a name="delete-method-ado-parameters-collection"></a>メソッド (ADO Parameters コレクション) を削除します。


**適用されます**Access 2013、Office 2013。


[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*パラメーター*です。*インデックス*を削除します。

## <a name="parameters"></a>パラメーター

- *Index*

  - 削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。

## <a name="remarks"></a>解説

コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、 **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションでのみ使用できます。 [Delete](parameter-object-ado.md) メソッドを呼び出すときは、 [Parameter](name-property-ado.md) オブジェクトの **Name** プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。

