---
title: Refresh メソッド (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4bbc44dbb9cdfeaac0904ed5296db206016211d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922763"
---
# <a name="refresh-method-ado"></a>Refresh メソッド (ADO)


**適用されます**Access 2013、Office 2013。

コレクションのオブジェクトを更新し、プロバイダーから使用可能な、プロバイダーに固有のオブジェクトを反映します。

## <a name="syntax"></a>構文

*コレクション*です。更新

## <a name="remarks"></a>解説

**Refresh** メソッドは、どのコレクションから呼び出すかによって異なる操作を実行します。

## <a name="parameters"></a>パラメーター

**Command** オブジェクトの [Parameters](command-object-ado.md) コレクションで [Refresh](parameters-collection-ado.md) メソッドを使用すると、 **Command** オブジェクトで指定されたストアド プロシージャまたはパラメーター化されたクエリに関するプロバイダー側のパラメーター情報が取得されます。プロバイダーがストアド プロシージャの呼び出しまたはパラメーター化されたクエリをサポートしない場合には、コレクションは空になります。

[Refresh](activeconnection-property-ado.md) メソッドを呼び出す前に、 **Command** オブジェクトの [ActiveConnection](connection-object-ado.md) プロパティを有効な [Connection](commandtext-property-ado.md) オブジェクトに、 [CommandText](commandtype-property-ado.md) プロパティを有効なコマンドに、 **CommandType** プロパティを **adCmdStoredProc** に、それぞれ設定する必要があります。

**Refresh** メソッドを呼び出す前に **Parameters** コレクションにアクセスすると、自動的にメソッドが呼び出され、コレクションが更新されます。


> [!NOTE]
> <P>[!メモ] <STRONG>Refresh</STRONG> メソッドを使用してプロバイダーからパラメーター情報を取得し、1 つまたは複数の可変長データ型の <A href="parameter-object-ado.md">Parameter</A> オブジェクトが返される場合、ADO はパラメーターの最大可能サイズに基づいてメモリを割り当てるため、実行時にエラーが発生します。エラーを避けるには、 <A href="size-property-ado.md">Execute</A> メソッドを呼び出す前に、これらのパラメーターの <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Size</A> プロパティを明示的に設定する必要があります。</P>



**Fields**

**Fields** コレクションに対して **Refresh** メソッドを使用しても、目に見える効果はありません。基になっているデータベース構造から変更を取得するには、 [Requery](requery-method-ado.md) メソッドを使用するか、または [Recordset](recordset-object-ado.md) オブジェクトがブックマークをサポートしない場合は [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) メソッドを使用する必要があります。

**Properties**

一部のオブジェクトの **Properties** コレクションに対して **Refresh** メソッドを使用すると、プロバイダーが公開するダイナミック プロパティでコレクションが作成されます。このようなプロパティは、ADO がサポートする組み込みプロパティにはない、プロバイダーに固有の機能に関する情報を提供します。

