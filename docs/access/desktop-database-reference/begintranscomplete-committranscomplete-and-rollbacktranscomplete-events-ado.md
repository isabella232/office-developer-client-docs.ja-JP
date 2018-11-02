---
title: BeginTransComplete、CommitTransComplete、RollbackTransComplete イベント (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6a49b08c1b4f7879d50f9dd1d29cfcf89ded50c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928081"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>BeginTransComplete イベント、CommitTransComplete イベント、RollbackTransComplete イベント (ADO)


**適用されます**Access 2013、Office 2013。


これらのイベントは、[Connection](connection-object-ado.md) オブジェクトに対する関連付けられた操作の実行の終了後に呼び出されます。

  - **BeginTransComplete** は、 [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。

  - **CommitTransComplete** は、 [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。

  - **RollbackTransComplete** は、 [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。

## <a name="syntax"></a>構文

BeginTransComplete*TransactionLevel*、 *pError*、 *adStatus* *pConnection*

CommitTransComplete*pError*、 *adStatus*、 *pConnection*

RollbackTransComplete*pError*、 *adStatus*、 *pConnection*

## <a name="parameters"></a>パラメーター

  - *TransactionLevel*

  - 長整数型 ( **Long** ) の値であり、このイベントを発生させた **BeginTrans** の新規トランザクション レベルが格納されます。

  - *pError*

  - [Error](error-object-ado.md) オブジェクトです。EventStatusEnum の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    このパラメーターを **adStatusUnwantedEvent** に設定すると、これらのイベントから制御が戻る前に後続の通知が行われるのを防ぐことができます。

  - *pConnection*

  - このイベントが発生した **Connection** オブジェクトです。

## <a name="remarks"></a>解説

Visual C++ では、複数の **Connection** が同じイベント処理メソッドを共有できます。メソッドは返された **Connection** オブジェクトを使って、どのオブジェクトがイベントを発生させたかを判別します。

[Attributes](attributes-property-ado.md) プロパティを **adXactCommitRetaining** または **adXactAbortRetaining** に設定した場合、トランザクションをコミットまたはロールバックした後に、新規トランザクションが開始されます。 **BeginTransComplete** イベントを使うと、最初のトランザクション開始イベント以外のイベントが無視されます。

