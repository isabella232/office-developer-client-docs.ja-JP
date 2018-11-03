---
title: IIS で仮想サーバーを構成します。
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8ab3bf8e6ffec2b72744d3abacceb4725c98b02
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946728"
---
# <a name="configuring-virtual-servers-on-iis"></a>IIS で仮想サーバーを構成します。

**適用されます**Access 2013、Office 2013。

Internet Information Services 4.0 で仮想サーバーを作成する場合、その仮想サーバーが RDS と共に動作するように設定するには、さらに次の 2 つの手順が必要です。

1.  サーバーをセットアップするときに、[実行アクセスを許可する (スクリプトのアクセスを含む)] チェック ボックスをオンにします。

2.  Msadcs.dll を*vroot*に移動\\msadc、 *vroot*が、仮想サーバーのホーム ディレクトリにあります。

