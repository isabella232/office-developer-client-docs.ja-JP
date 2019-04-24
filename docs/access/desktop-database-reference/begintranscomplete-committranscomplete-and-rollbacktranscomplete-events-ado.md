---
title: begintranscomplete、committranscomplete、RollbackTransComplete events (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296823"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>begintranscomplete イベント、committranscomplete イベント、および RollbackTransComplete イベント (ADO)

**適用先:** Access 2013、Office 2013

これらのイベントは、[Connection](connection-object-ado.md) オブジェクトに対する関連付けられた操作の実行の終了後に呼び出されます。

- **BeginTransComplete** は、 [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。

- **CommitTransComplete** は、 [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。

- **RollbackTransComplete** は、[RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。

## <a name="syntax"></a>構文

begintranscomplete*transactionlevel*、 ** 状態、 *adstatus*、 *pconnection*

committranscomplete** の手順、 *adstatus*、 *pconnection*

RollbackTransComplete** の*状態、adstatus*、 *pconnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*transactionlevel* |長整数型 ( **Long** ) の値であり、このイベントを発生させた **BeginTrans** の新規トランザクション レベルが格納されます。|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。 eventstatusenum の値が**adstatuserrorソケット**の場合に発生したエラーについて説明します。それ以外の場合は、設定されません。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 このパラメーターを **adStatusUnwantedEvent** に設定すると、これらのイベントから制御が戻る前に後続の通知が行われるのを防ぐことができます。|
|*pconnection* |このイベントが発生した **Connection** オブジェクトです。|

## <a name="remarks"></a>注釈

Visual C++ では、複数の **Connection** が同じイベント処理メソッドを共有できます。メソッドは返された **Connection** オブジェクトを使って、どのオブジェクトがイベントを発生させたかを判別します。

[Attributes](attributes-property-ado.md) プロパティを **adXactCommitRetaining** または **adXactAbortRetaining** に設定した場合、トランザクションをコミットまたはロールバックした後に、新規トランザクションが開始されます。 **BeginTransComplete** イベントを使うと、最初のトランザクション開始イベント以外のイベントが無視されます。

