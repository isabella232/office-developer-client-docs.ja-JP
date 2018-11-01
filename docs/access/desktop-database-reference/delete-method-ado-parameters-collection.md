---
title: Delete メソッド (ADO Parameters コレクション)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e519d40a081b132cd09030e9ba97de9e8987af99
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881959"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete メソッド (ADO Parameters コレクション)


**適用されます**Access 2013、Office 2013。


[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*パラメーター*です。*インデックス*を削除します。

## <a name="parameters"></a>パラメーター

  - *Index*

  - 削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。

## <a name="remarks"></a>解説

コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、 **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションでのみ使用できます。 [Delete](parameter-object-ado.md) メソッドを呼び出すときは、 [Parameter](name-property-ado.md) オブジェクトの **Name** プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。

