---
title: InternetTimeout プロパティ (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06e844b9e6e0976679820fbc2ac79eae14131d36
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879050"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout プロパティ (RDS)


**適用されます**Access 2013、Office 2013。

要求がタイムアウトするまでの待機時間をミリ秒単位で示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

要求がタイムアウトするまでのミリ秒数単位の時間を表す長整数型 ( **Long** ) の値を設定または取得します。

## <a name="remarks"></a>解説

このプロパティは、HTTP プロトコルまたは HTTPS プロトコルで送信された要求にのみ適用されます。

3 層環境での要求の場合、実行が終了するまでに数分間かかることがあります。このプロパティを使って、長時間かかる要求に対する待機時間を指定します。

