---
title: MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4671e57e3edb44bc1c927ca11f2cf79e70c2699
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478094"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (RDS)


**適用されます**Access 2013 |。Office 2013

指定された [Recordset](recordset-object-ado.md) オブジェクトの最初、最後、次、または前のレコードに移動します。

## <a name="syntax"></a>構文

*DataControl*。レコード セットです。{ MoveFirst |MoveLast |MoveNext |MovePrevious}

## <a name="parameters"></a>パラメーター

  - *DataControl*

  - [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。

## <a name="remarks"></a>解説

**RDS.DataControl** オブジェクトで **Move** メソッドを使用すると、Web ページ上のデータ連結コントロールのデータ レコード間を移動できます。たとえば、 **RDS.DataControl** オブジェクトにバインドしてグリッドに **Recordset** を表示しているとします。[First]、[Last]、[Next]、および [Previous] ボタンを追加し、ユーザーが各ボタンをクリックすると、表示されている **Recordset** の最初、最後、次、または前のレコードに移動できるようにします。これを行うには、[First]、[Last]、[Next]、および [Previous] の各ボタンの onClick プロシージャで、 **RDS.DataControl** オブジェクトの **MoveFirst** 、 **MoveLast** 、 **MoveNext** 、および **MovePrevious** の各メソッドを呼び出します。「 [Address Book のナビゲーション ボタン](address-book-navigation-buttons.md)」でこの方法を説明しています。

