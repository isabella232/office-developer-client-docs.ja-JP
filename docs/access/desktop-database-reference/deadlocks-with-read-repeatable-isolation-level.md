---
title: 反復可能な読み取りの分離レベルでのデッドロック
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e742a9157c3f2f26d70351fc05afa35472654af9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944328"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>反復可能な読み取りの分離レベルでのデッドロック


**適用されます**Access 2013、Office 2013。

カスタム ビジネス オブジェクトが繰り返し可能な読み取りの分離レベルを使用して SQL Server にアクセスする場合に、そのビジネス オブジェクトが、同じトランザクションでクエリを送信し更新する 2 つのクライアントによって同時に呼び出されると、デッドロックが発生する可能性があります。リモート データ サービスは、いずれか 1 つのプロセスをタイムアウトにしてデッドロックを解除できるように設計されていますが、そのクライアントの更新は失敗します。

タイムアウトの長さを変更するのにには、[カーソル サービス](microsoft-cursor-service-for-ole-db-ado-service-component.md)**コマンドのタイムアウト**の動的プロパティを使用します。

