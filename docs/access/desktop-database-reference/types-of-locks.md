---
title: ロック (デスクトップ データベース参照のアクセス) の種類
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e141abdd915257abdb8499efea1aded3cee4cb1c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477689"
---
# <a name="types-of-locks"></a>ロックの種類


**適用されます**Access 2013 |。Office 2013



## <a name="adlockbatchoptimistic"></a>adLockBatchOptimistic

共有的バッチ更新を示します。バッチ更新モードの場合に必要です。

多くのアプリケーションでは、一度に多数の行をフェッチした後、挿入、更新、または削除される行セット全体に対して調整したうえでの更新を行う必要があります。バッチ カーソルを使用すると、サーバーへの往復が 1 回で済むため、更新パフォーマンスが向上し、ネットワーク トラフィックが軽減されます。バッチ カーソル ライブラリを使用すると、静的カーソルを作成した後、データ ソースから切断できます。この時点で、行を変更した後、再接続し、変更内容をデータ ソースにまとめて送信することができます。

## <a name="adlockoptimistic"></a>adLockOptimistic

**Update** メソッドを呼び出したときのみレコードをロックする、共有的ロックの使用を指定します。これは、レコードを編集してから **Update** を呼び出すまでに、他のユーザーがデータを変更し、競合が発生する可能性があることを示します。この種類のロックは、競合が発生する可能性が低いか、競合をすぐに解決できる状況で使用します。

## <a name="adlockpessimistic"></a>adLockPessimistic

レコード単位の排他的ロックを指定します。プロバイダーは、レコードの編集が正常に行われることを確実にするために必要な操作 (通常は編集の直前にレコードに対するデータ ソースでのロック) を実行します。これは、編集を開始すると、 **Update** を呼び出してロックを解除するまで、他のユーザーがそのレコードを使用できないことを意味します。この種類のロックは、予約システムなど、データを同時に変更できないシステムで使用します。

## <a name="adlockreadonly"></a>adLockReadOnly

読み取り専用のレコードを指定します。データの変更はできません。読み取り専用ロックは、サーバーでレコードのロックを保持する必要がないため、"最も高速な" ロックです。

## <a name="adlockunspecified"></a>adLockUnspecified

ロックの種類を指定しません。

