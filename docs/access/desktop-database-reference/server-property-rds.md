---
title: Server プロパティ (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492602d7150f3080df329d30a38e3af51755cf0f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949503"
---
# <a name="server-property-rds"></a>Server プロパティ (RDS)

**適用されます**Access 2013、Office 2013。

インターネット インフォメーション サービス (IIS) 名および通信プロトコルを示します。

**Server** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグで設定するか、実行時にスクリプト コードで設定できます。

## <a name="syntax"></a>構文

|プロトコル|デザイン時の構文|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|インプロセス|`<PARAM NAME="Server" VALUE="">`|


|プロトコル|実行時の構文|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|インプロセス|`DataControl.Server=""`|


## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*awebsrvr*または*コンピューター名* |サーバーがリモート コンピューター上にある場合は、インターネット パス、イントラネット パス、またはコンピューター名を含む文字列型 ( **String** ) の値。サーバーがローカル コンピューター上にある場合は空の文字列。|
|*port* |省略可能。 IIS サーバーへの接続に使用されるポートです。 Internet Explorer で、ポート番号を設定 ([**ツール**] メニューで、 **[インターネット オプション**] をクリックし、[**接続**] タブを選択し、) または IIS で。|
|*DataControl* |**RDS.DataControl** オブジェクトを表すオブジェクト変数を指定します。|

## <a name="remarks"></a>解説

サーバーは、 **RDS.DataControl** 要求 (クエリまたは更新) が処理される場所です。 既定では、すべての要求は指定されたサーバー上の [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクト、 [MSDFMAP.Handler](datafactory-customization.md) コンポーネント、および [MSDFMAP.INI](understanding-the-customization-file.md) ファイルによって処理されます。 

サーバーを変更する場合は、新旧の **MSDFMAP.INI** ファイルの設定を調整する必要があります。 互換性がないと、一方のサーバーで成功した要求が、もう一方のサーバーでは失敗することがあります。 Server プロパティが "" に設定されている場合、これらのオブジェクトはローカル コンピューターで使用されます。

