---
title: レコードセットの切断および再接続
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c028a7d867a105f35b4848ecbe95339f5fcd4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293862"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>レコードセットの切断および再接続


**適用先:** Access 2013、Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>レコードセットを切断し、再接続する

ADO の最も強力な機能の1つとして、データソースからクライアント側の**recordset**を開き、その**recordset**をデータソースから*切断*する機能があります。 Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it. You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.

**Recordset** を切断するには、カーソル位置を **adUseClient** に設定して開いたうえで、**ActiveConnection** プロパティを *Nothing* に設定します (C++ を使用している場合は、**ActiveConnection** を NULL に設定して切断する必要があります)。

切断された **Recordset** は、この章の後半で **Recordset** の保存について説明するときに使用します。この保存操作は、クライアント コンピューターがネットワークに接続されていないときに、アプリケーションが **Recordset** 内のデータを使用できるようにする必要がある場合に対処するためのものです。

