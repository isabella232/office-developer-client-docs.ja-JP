---
title: EndOfRecordset イベント (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89ca397c4e95dd6f18de41862e9383f77fe14aa8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928839"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset イベント (ADO)


**適用されます**Access 2013、Office 2013。



**EndOfRecordset** イベントは、 [Recordset](recordset-object-ado.md) の末尾を越える行に移動しようとすると呼び出されます。

## <a name="syntax"></a>構文

EndOfRecordset*fMoreData*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

  - *fMoreData*

  - A**バリアント\_BOOL**値をバリアント型に設定\_true の場合、複数の行は、**レコード セット**に追加されていることを示します。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    **EndOfRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。イベントを発生させた操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。
    
    **EndOfRecordset** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。

  - *pRecordset*

  - **Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。

## <a name="remarks"></a>解説

**EndOfRecordset** イベントは、 [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 操作が失敗した場合に発生することがあります。

このイベント ハンドラーは、たとえば **MoveNext** を呼び出して、 **Recordset** オブジェクトの末尾を越えて移動しようとすると呼び出されます。 ただし、このイベントの中で、データベースからさらにレコードを取得し、それらを **Recordset** の末尾に追加することもできます。 その場合は、 *fMoreData*をバリアント型に設定\_true に設定し、 **EndOfRecordset**からの戻り値です。 その後で **MoveNext** を再度呼び出して、新たに取得したレコードにアクセスします。

