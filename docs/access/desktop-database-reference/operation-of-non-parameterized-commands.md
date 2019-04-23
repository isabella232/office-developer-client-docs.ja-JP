---
title: 非パラメーター化コマンドの操作
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 720cbaf346b64d4d23b1e3314b06ba941e78b700
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288267"
---
# <a name="operation-of-non-parameterized-commands"></a>非パラメーター化コマンドの操作


**適用先:** Access 2013、Office 2013

非パラメーター化コマンドの場合、すべてのプロバイダー コマンドが実行され、コマンドの実行中に **Recordset** が作成されます。コマンドが同期的に実行される場合、すべての **Recordset** が完全に作成されます。非同期作成モードが選択された場合、 **Recordset** の作成状態は、作成モードと **Recordset** のサイズによって異なります。

たとえば、*parent-command* は、Customers テーブルからある会社の顧客の **Recordset** を返すことができ、*child-command* は、Orders テーブルからすべての顧客の受注の **Recordset** を返すことができます。

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

非パラメーター化親子関係の場合、親と子の **Recordset** オブジェクトには、それぞれを関連付ける共通の列が必要です。 列の名前は RELATE 句で、まず *parent-column* を、次に *child-column* を指定します。 列の名前は、 **Recordset** オブジェクトごとに異なってもかまいませんが、意味のある関係を指定するために、同じ情報を参照する必要があります。 たとえば、 **Customers** と **Orders** の両方の **Recordset** オブジェクトに customerID フィールドがある場合などです。 子 **Recordset** のメンバーシップはプロバイダー コマンドによって決定されるため、子 **Recordset** に孤立行を含めることができます。 これらの孤立行にアクセスするには、さらにリシェイプを実行する必要があります。

データ シェイプにより、チャプター列が親 **Recordset** に追加されます。チャプター列の値は、RELATE 句を満たす子 **Recordset** 内の行への参照です。つまり、特定の親行の *parent-column* と、チャプター子のすべての行の *child-column* が同じ値になります。同じ RELATE 句で複数の TO 句が使用される場合、暗黙的に AND 演算子を使用して結合されます。RELATE 句の親列が親 **Recordset** へのキーの構成要素でない場合、1 つの子行に複数の親行が存在する可能性があります。

チャプター列の参照にアクセスすると、その参照で表される **Recordset** が ADO によって自動的に取得されます。非パラメーター化コマンドの場合、子 **Recordset** 全体が取得されても、チャプターは行のサブセットのみを表します。

追加された列に *chapter-alias* がない場合、その列に対して名前が自動的に生成されます。列の [Field](field-object-ado.md) オブジェクトが **Recordset** オブジェクトの [Fields](fields-collection-ado.md) コレクションに追加され、データ型は **adChapter** になります。

階層 **Recordset** の移動については、「 [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。

