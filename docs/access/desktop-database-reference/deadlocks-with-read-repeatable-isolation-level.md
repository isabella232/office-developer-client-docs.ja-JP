---
title: 読み取り反復可能な分離レベルを持つデッドロック
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c3b28c8d9be6a81ecc03ccf02d5361110de32f07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558409"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>読み取り反復可能な分離レベルを持つデッドロック


**適用先:** Access 2013、Office 2013

カスタム ビジネス オブジェクトが繰り返し可能な読み取りの分離レベルを使用して SQL Server にアクセスする場合に、そのビジネス オブジェクトが、同じトランザクションでクエリを送信し更新する 2 つのクライアントによって同時に呼び出されると、デッドロックが発生する可能性があります。リモート データ サービスは、いずれか 1 つのプロセスをタイムアウトにしてデッドロックを解除できるように設計されていますが、そのクライアントの更新は失敗します。

Cursor [Service Command Time](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Out 動的** プロパティを使用して、タイムアウトの長さを変更します。

