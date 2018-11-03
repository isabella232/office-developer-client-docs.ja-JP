---
title: コマンドを基になるデータ プロバイダーに発行します。
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 142772aaff5080a6e2522ab31884f2ff2319c8a7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944635"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>コマンドを基になるデータ プロバイダーに発行します。

**適用されます**Access 2013、Office 2013。

図形で始まらない任意のコマンドは、データ プロバイダーから渡されます。 これは、「形状 {プロバイダー コマンド}」という形式での図形コマンドを発行するのと同じです。 これらのコマンドを実行*しない***レコード セット**を生成する必要があります。 たとえば、"図形 {ドロップ テーブル 'mytable'} は完全に有効なシェイプ コマンドでは、データ プロバイダーは、テーブルのドロップをサポートするいると仮定した場合します。

この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。

