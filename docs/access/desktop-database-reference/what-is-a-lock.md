---
title: ロックとは (Access デスクトップデータベースリファレンス)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e503fd15d9864cc6ab007de031493e321622246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306763"
---
# <a name="what-is-a-lock"></a>ロックとは


**適用先:** Access 2013、Office 2013

ロックとは、マルチユーザー環境で DBMS が行へのアクセスを制限するプロセスです。行または列が排他的にロックされると、他のユーザーは、ロックが解除されるまでロックされたデータにアクセスできません。これにより、2 人のユーザーが 1 つの行の同じ列を同時に更新できないようにします。

ロックは、リソースの観点から非常に負荷が高い可能性があるため、データの整合性を保持する必要がある場合にのみ使用します。インターネットに接続されたデータベースのように、毎秒数百または数千のユーザーが 1 つのレコードにアクセスしようとする可能性があるデータベースでは、不要なロックが直ちにアプリケーションのパフォーマンスの低下を招くことになります。

適切なロック オプションを選択することで、データ ソースと ADO カーソル ライブラリが同時実行を管理する方法を制御できます。

Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.

プロバイダーによっては、すべての種類のロックをサポートしていない場合もあります。要求した **LockType** 設定がプロバイダーでサポートされていない場合は、別の種類のロックが代用されます。 **Recordset** オブジェクトで実際に使用できるロック機能を調べるには、 [adUpdate](supports-method-ado.md) および **adUpdateBatch** の **Supports** メソッドを使用します。

**CursorLocation** プロパティが [adUseClient](cursorlocation-property-ado.md) に設定されている場合、 **adLockPessimistic** 設定はサポートされません。サポートされていない値を設定しても、エラーは発生せず、サポートされる最も近い種類の **LockType** が代わりに使用されます。

**LockType** プロパティは、 **Recordset** が閉じている場合は読み取り/書き込み可能になっていますが、開いている場合は読み取り専用になります。

ここでは、以下のトピックについて説明します。

- [ロックの種類](types-of-locks.md)

