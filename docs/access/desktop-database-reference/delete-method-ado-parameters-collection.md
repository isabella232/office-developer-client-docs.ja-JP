---
title: メソッド (ADO Parameters コレクション) を削除します。
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704575"
---
# <a name="delete-method-ado-parameters-collection"></a>メソッド (ADO Parameters コレクション) を削除します。

**適用されます**Access 2013、Office 2013。

[Parameters](parameters-collection-ado.md) コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*パラメーター*です。*インデックス*を削除します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Index* |削除するオブジェクトの名前、またはコレクション内でのオブジェクトの位置 (インデックス) を含む文字列型 ( **String** ) の値です。|

## <a name="remarks"></a>解説

コレクションで **Delete** メソッドを使用すると、コレクションからオブジェクトの 1 つを削除できます。このメソッドは、 **Command** オブジェクトの [Parameters](command-object-ado.md) コレクションでのみ使用できます。 [Delete](parameter-object-ado.md) メソッドを呼び出すときは、 [Parameter](name-property-ado.md) オブジェクトの **Name** プロパティまたはコレクションのインデックスを使用する必要があり、オブジェクト変数は有効な引数ではありません。

