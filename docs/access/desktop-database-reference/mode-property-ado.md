---
title: Mode プロパティ (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74b0a401c5fbd7e34cbd002020d81b9b0858e4f7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874280"
---
# <a name="mode-property-ado"></a>Mode プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Connection](connection-object-ado.md) オブジェクト、 [Record](record-object-ado.md) オブジェクト、または [Stream](stream-object-ado.md) オブジェクトで使用可能なデータ変更権限を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

[ConnectModeEnum](connectmodeenum.md) の値を設定または取得します。**Connection** の既定値は **adModeUnknown** です。**Record** オブジェクトの既定値は **adModeRead** です。基になるソースに関連付けられている **Stream** (URL により、ソース、または **Record** の既定 **Stream** として開かれたもの) の既定値は、**adModeRead** です。基になるソースに関連付けられていない (メモリ内でインスタンス化された) **Stream** の既定値は **adModeUnknown** です。

## <a name="remarks"></a>解説

**Mode** プロパティは、プロバイダーが現在の接続で使用しているアクセス権を設定または取得するために使用します。 **Mode** プロパティは、 **Connection** オブジェクトが閉じているときにのみ設定できます。

**Stream** オブジェクトでは、アクセス モードを指定しない場合、 **Stream** オブジェクトを開くときに使うソースのモードが継承されます。たとえば、 **Record** オブジェクトから **Stream** を開くと、既定では **Record** と同じモードで開きます。

このプロパティは、オブジェクトが閉じているときは読み取り/書き込み可能で、オブジェクトが開いているときは読み取り専用になります。

**リモート データ サービスの使用法**クライアント側の Connection オブジェクトで使用すると、[**モード**] プロパティは**adModeUnknown**にのみ設定できます。

