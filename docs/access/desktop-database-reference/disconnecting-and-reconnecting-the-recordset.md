---
title: レコードセットを切断し、再接続する
TOCTitle: Disconnecting and Reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 094c68fbf5b62a7a1b3af16b826bf9c2c26a2af4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882421"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>レコードセットを切断し、再接続する


**適用されます**Access 2013、Office 2013。

## <a name="disconnecting-and-reconnecting-the-recordset"></a>レコードセットの切断および再接続

ADO の最も強力な機能の 1 つは、クライアント側の**Recordset**を開くと、データ ソース、データ ソースから**レコード セット***を切断*する機能です。 **レコード セット**を切断すると、データ ソースへの接続を終了できます、それを維持するために使用するサーバー上のリソースを解放します。 表示し切断されているときに、**レコード セット**内のデータを編集後、データ ソースに再接続し、更新をバッチ モードで送信を続行できます。

**Recordset** を切断するには、カーソル位置を **adUseClient** に設定して開いたうえで、**ActiveConnection** プロパティを *Nothing* に設定します (C++ を使用している場合は、**ActiveConnection** を NULL に設定して切断する必要があります)。

切断された **Recordset** は、この章の後半で **Recordset** の保存について説明するときに使用します。この保存操作は、クライアント コンピューターがネットワークに接続されていないときに、アプリケーションが **Recordset** 内のデータを使用できるようにする必要がある場合に対処するためのものです。

