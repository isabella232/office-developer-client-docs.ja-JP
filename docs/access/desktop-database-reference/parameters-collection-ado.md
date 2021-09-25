---
title: Parameters コレクション (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 63af27d7856a737361def622e8547560aef8f1fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568741"
---
# <a name="parameters-collection-ado"></a>Parameters コレクション (ADO)


**適用先:** Access 2013、Office 2013

[Command](command-object-ado.md) オブジェクトのすべての [Parameter](parameter-object-ado.md) オブジェクトを格納します。

## <a name="remarks"></a>注釈

**Command** オブジェクトには、 **Parameter** オブジェクトから構成される **Parameters** コレクションがあります。

[Command](refresh-method-ado.md) オブジェクトの **Parameters** コレクションで **Refresh** メソッドを使用すると、 **Command** オブジェクトで指定されたストアド プロシージャまたはパラメーター化されたクエリに関するプロバイダー側のパラメーター情報が取得されます。プロバイダーの中には、ストアド プロシージャの呼び出しまたはパラメーター化されたクエリをサポートしないものもあります。このようなプロバイダーを使用する場合、 **Parameters** コレクションの **Refresh** メソッドを呼び出すと、エラーが発生します。

独自の **Parameter** オブジェクトを定義せず、 **Refresh** メソッドを呼び出す前に **Parameters** コレクションにアクセスすると、自動的にメソッドが呼び出され、コレクションが更新されます。

呼び出すストアド プロシージャまたはパラメーター化されたクエリに関連するパラメーターのプロパティを把握していると、プロバイダーの呼び出しを最小限に抑えて、パフォーマンスを向上させることができます。[CreateParameter](createparameter-method-ado.md) メソッドを使用して適切なプロパティ設定を備えた **Parameter** オブジェクトを作成し、 [Append](append-method-ado.md) メソッドを使用してそれらのオブジェクトを **Parameters** コレクションに追加します。これにより、プロバイダーを呼び出してパラメーター情報を取得しなくても、パラメーターの値を設定したり返したりすることができます。パラメーター情報を提供しないプロバイダーに書き込む場合にパラメーターを使用するには、このメソッドを使用して手動で **Parameters** コレクションを設定する必要があります。 [Delete](delete-method-ado-parameters-collection.md) メソッドを使用すると、必要に応じて **Parameters** コレクションから **Parameter** オブジェクトを削除できます。

**Recordset** の **Parameters** コレクションのオブジェクトは、 **Recordset** が閉じているときには範囲外になり、使用できなくなります。

