---
title: BeginTrans メソッド、CommitTrans メソッド、および RollbackTrans メソッド (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d8c641c43df1a0f035d37f14727e42f89475d16a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558801"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a>BeginTrans メソッド、CommitTrans メソッド、および RollbackTrans メソッド (ADO)

**適用先:** Access 2013、Office 2013

これらのトランザクション メソッドは、[Connection](connection-object-ado.md) オブジェクト内のトランザクション処理を次のように管理します。

- **BeginTrans** は、新しいトランザクションを開始します。

- **CommitTrans** は、すべての変更を保存して現在のトランザクションを終了します。新しいトランザクションを開始する場合もあります。

- **RollbackTrans** は、現在のトランザクションの間に行われたすべての変更をキャンセルし、トランザクションを終了します。新しいトランザクションを開始する場合もあります。

## <a name="syntax"></a>構文

*level*  = *object*.BeginTrans()

*object*.BeginTrans

*object*.CommitTrans

*object*.RollbackTrans

## <a name="return-value"></a>戻り値

**BeginTrans** は、トランザクションの入れ子レベルを示す長整数型 (**Long**) の変数を返す関数として呼び出すことができます。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*object* |**Connection** オブジェクトです。|

### <a name="connection"></a>Connection

**Connection** オブジェクトでこれらのメソッドを使用すると、ソース データに対して行った一連の変更を、1 つの単位として保存または取り消すことができます。たとえば、銀行口座間でお金を移すには、一方の口座からその金額を引き出し、他方の口座に入金するという 2 つの操作が行われます。どちらかの更新が失敗すると、口座の残高が合わなくなります。開いているトランザクションでこのような変更を行うと、すべての変更が正しく処理されるか、またはまったく変更が行われないことが保証されます。

> [!NOTE]
> [!メモ] すべてのプロバイダーでトランザクションがサポートされているわけではありません。 プロバイダー定義プロパティ Transaction DDL が **Connection** オブジェクトの **Properties** [](properties-collection-ado.md)コレクションに表示され、プロバイダーがトランザクションをサポートするかどうかを示します。 プロバイダーがトランザクションをサポートしていない場合、これらのメソッドを呼び出すと、エラーが発生します。

いったん **BeginTrans** メソッドを呼び出すと、 **CommitTrans** メソッドまたは **RollbackTrans** メソッドを呼び出してトランザクションを終了するまで、変更がコミットされることはありません。

入れ子になったトランザクションをサポートするプロバイダーの場合、開いているトランザクションで **BeginTrans** メソッドを呼び出すと、入れ子になった新しいトランザクションが開始されます。戻り値は、入れ子のレベルを示します。戻り値 "1" は最上位レベルのトランザクション (他のトランザクションの入れ子になっていないトランザクション) が開いたことを示し、"2" は第 2 レベルのトランザクション (最上位レベルのトランザクションの入れ子になっているトランザクション) が開いたことを示します ("3" 以下も同様です)。 **CommitTrans** メソッドまたは **RollbackTrans** メソッドを呼び出すと、最後に開いたトランザクションだけが処理されます。さらに上のレベルのトランザクションを処理するには、現在のトランザクションを閉じるか、またはロールバックする必要があります。

**CommitTrans** メソッドを呼び出すと、その接続で開いているトランザクションで行われた変更が保存され、トランザクションが終了します。 **RollbackTrans** メソッドを呼び出すと、開いているトランザクションで行われたすべての変更が元に戻され、トランザクションが終了します。開いているトランザクションが存在しない状態でいずれかのメソッドを呼び出すと、エラーが発生します。

**Connection** オブジェクトの [Attributes](attributes-property-ado.md) プロパティによっては、 **CommitTrans** メソッドまたは **RollbackTrans** メソッドを呼び出すと、新しいトランザクションが自動的に開始する場合があります。 **Attributes** プロパティが **adXactCommitRetaining** に設定されている場合は、 **CommitTrans** メソッドを呼び出すと、プロバイダーが新しいトランザクションを自動的に開始します。 **Attributes** プロパティが **adXactAbortRetaining** に設定されている場合は、 **RollbackTrans** メソッドを呼び出すと、プロバイダーが新しいトランザクションを自動的に開始します。

### <a name="remote-data-service"></a>リモート データ サービス

**BeginTrans** メソッド、**CommitTrans** メソッド、および **RollbackTrans** メソッドは、クライアント側の **Connection** オブジェクトでは利用できません。

