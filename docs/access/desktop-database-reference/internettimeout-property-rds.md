---
title: InternetTimeout プロパティ (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fb247396b5e7e65c9fbfe86ab4f06b6a69037522
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631938"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout プロパティ (RDS)


**適用先**: Access 2013、Office 2013

要求がタイムアウトするまでの待機時間をミリ秒単位で示します。

## <a name="settings-and-return-values"></a>設定および戻り値

要求がタイムアウトするまでのミリ秒数単位の時間を表す長整数型 (**Long**) の値を設定または取得します。

## <a name="remarks"></a>注釈

このプロパティは、HTTP プロトコルまたは HTTPS プロトコルで送信された要求にのみ適用されます。

3 層環境での要求の場合、実行が終了するまでに数分間かかることがあります。このプロパティを使って、長時間かかる要求に対する待機時間を指定します。

