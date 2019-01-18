---
title: MoveFirst メソッド、MoveLast メソッド、MoveNext メソッド、MovePrevious メソッド (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716034"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>MoveFirst メソッド、MoveLast メソッド、MoveNext メソッド、MovePrevious メソッド (RDS)

**適用されます**Access 2013、Office 2013。

指定された [Recordset](recordset-object-ado.md) オブジェクトの最初、最後、次、または前のレコードに移動します。

## <a name="syntax"></a>構文

*DataControl*。レコード セットです。{ MoveFirst |MoveLast |MoveNext |MovePrevious}

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|

## <a name="remarks"></a>解説

Rds. の**に、 **Move**メソッドを使用します。DataControl** web ページ上のデータ バインド コントロール内のデータ レコード間を移動するオブジェクトです。 

たとえば、 **RDS.DataControl** オブジェクトにバインドしてグリッドに **Recordset** を表示しているとします。 [First]、[Last]、[Next]、および [Previous] ボタンを追加し、ユーザーが各ボタンをクリックすると、表示されている **Recordset** の最初、最後、次、または前のレコードに移動できるようにします。 これを行うには、[First]、[Last]、[Next]、および [Previous] の各ボタンの onClick プロシージャで、 **RDS.DataControl** オブジェクトの **MoveFirst** 、 **MoveLast** 、 **MoveNext** 、および **MovePrevious** の各メソッドを呼び出します。 「 [Address Book のナビゲーション ボタン](address-book-navigation-buttons.md)」でこの方法を説明しています。

