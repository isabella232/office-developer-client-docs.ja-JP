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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699248"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>レコードセットの切断および再接続


**適用されます**Access 2013、Office 2013。

## <a name="disconnecting-and-reconnecting-the-recordset"></a>レコードセットの切断および再接続

ADO の最も強力な機能の 1 つは、クライアント側の**Recordset**を開くと、データ ソース、データ ソースから**レコード セット***を切断*する機能です。 **レコード セット**を切断すると、データ ソースへの接続を終了できます、それを維持するために使用するサーバー上のリソースを解放します。 表示し切断されているときに、**レコード セット**内のデータを編集後、データ ソースに再接続し、更新をバッチ モードで送信を続行できます。

**Recordset** を切断するには、カーソル位置を **adUseClient** に設定して開いたうえで、**ActiveConnection** プロパティを *Nothing* に設定します (C++ を使用している場合は、**ActiveConnection** を NULL に設定して切断する必要があります)。

切断された **Recordset** は、この章の後半で **Recordset** の保存について説明するときに使用します。この保存操作は、クライアント コンピューターがネットワークに接続されていないときに、アプリケーションが **Recordset** 内のデータを使用できるようにする必要がある場合に対処するためのものです。

