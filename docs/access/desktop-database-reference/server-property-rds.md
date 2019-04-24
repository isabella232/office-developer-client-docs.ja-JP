---
title: Server プロパティ (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f35910591d86e0e5a2b92d680be3c5f64504088
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308688"
---
# <a name="server-property-rds"></a>Server プロパティ (RDS)

**適用先:** Access 2013、Office 2013

インターネット インフォメーション サービス (IIS) 名および通信プロトコルを示します。

**Server** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグで設定するか、実行時にスクリプト コードで設定できます。

## <a name="syntax"></a>構文

|プロトコル|デザイン時の構文|
|:-------|:-----------------|
|プロトコル|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|インプロセス|`<PARAM NAME="Server" VALUE="">`|


|プロトコル|実行時の構文|
|:-------|:--------------|
|プロトコル|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|インプロセス|`DataControl.Server=""`|


## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*awebsrvr* または *computername* |サーバーがリモート コンピューター上にある場合は、インターネット パス、イントラネット パス、またはコンピューター名を含む文字列型 (**String**) の値。サーバーがローカル コンピューター上にある場合は空の文字列。|
|*port* |Optional. A port that is used to connect to an IIS server. The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.|
|*DataControl* |**RDS.DataControl** オブジェクトを表すオブジェクト変数。|

## <a name="remarks"></a>注釈

サーバーは、 **RDS.DataControl** 要求 (クエリまたは更新) が処理される場所です。 既定では、すべての要求は指定されたサーバー上の [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクト、 [MSDFMAP.Handler](datafactory-customization.md) コンポーネント、および [MSDFMAP.INI](understanding-the-customization-file.md) ファイルによって処理されます。 

サーバーを変更する場合は、新旧の **MSDFMAP.INI** ファイルの設定を調整する必要があります。 互換性がないと、一方のサーバーで成功した要求が、もう一方のサーバーでは失敗することがあります。 Server プロパティが "" に設定されている場合、これらのオブジェクトはローカル コンピューターで使用されます。

