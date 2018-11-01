---
title: 基になるデータ プロバイダーにコマンドを発行する
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0379d38b6c38145a72d5ab41b7ee0e7ec45531b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889078"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>基になるデータ プロバイダーにコマンドを発行する


**適用されます**Access 2013、Office 2013。

図形で始まらない任意のコマンドは、データ プロバイダーから渡されます。 これは、「形状 {プロバイダー コマンド}」という形式での図形コマンドを発行するのと同じです。 これらのコマンドを実行*しない***レコード セット**を生成する必要があります。 たとえば、"図形 {ドロップ テーブル 'mytable'} は完全に有効なシェイプ コマンドでは、データ プロバイダーは、テーブルのドロップをサポートするいると仮定した場合します。

この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。

