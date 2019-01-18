---
title: 基になるデータ プロバイダーへのコマンドの発行
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709615"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>基になるデータ プロバイダーへのコマンドの発行

**適用されます**Access 2013、Office 2013。

図形で始まらない任意のコマンドは、データ プロバイダーから渡されます。 これは、「形状 {プロバイダー コマンド}」という形式での図形コマンドを発行するのと同じです。 これらのコマンドを実行*しない***レコード セット**を生成する必要があります。 たとえば、"図形 {ドロップ テーブル 'mytable'} は完全に有効なシェイプ コマンドでは、データ プロバイダーは、テーブルのドロップをサポートするいると仮定した場合します。

この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。

