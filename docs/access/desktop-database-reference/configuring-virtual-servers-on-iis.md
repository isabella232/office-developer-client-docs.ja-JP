---
title: IIS での仮想サーバーの構成
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: db240ef561de9ba653dbad3453a2ee4d894baa25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602893"
---
# <a name="configuring-virtual-servers-on-iis"></a>IIS での仮想サーバーの構成

**適用先**: Access 2013、Office 2013

Internet Information Services 4.0 で仮想サーバーを作成する場合、その仮想サーバーが RDS と共に動作するように設定するには、さらに次の 2 つの手順が必要です。

1.  サーバーをセットアップするときに、[実行アクセスを許可する (スクリプトのアクセスを含む)] チェック ボックスをオンにします。

2.  仮想msadcs.dll *vroot* msadc に移動します \\ *。vroot* は仮想サーバーのホーム ディレクトリです。

