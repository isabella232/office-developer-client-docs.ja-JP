---
title: 分離レベルが繰り返し可能な読み取りのときにデッドロックが発生する
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a5fbf4686fc5b8bffc984b4b483f1ee506eb7dd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882988"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>分離レベルが繰り返し可能な読み取りのときにデッドロックが発生する


**適用されます**Access 2013、Office 2013。

カスタム ビジネス オブジェクトが繰り返し可能な読み取りの分離レベルを使用して SQL Server にアクセスする場合に、そのビジネス オブジェクトが、同じトランザクションでクエリを送信し更新する 2 つのクライアントによって同時に呼び出されると、デッドロックが発生する可能性があります。リモート データ サービスは、いずれか 1 つのプロセスをタイムアウトにしてデッドロックを解除できるように設計されていますが、そのクライアントの更新は失敗します。

タイムアウトの長さを変更するのにには、[カーソル サービス](microsoft-cursor-service-for-ole-db-ado-service-component.md)**コマンドのタイムアウト**の動的プロパティを使用します。

