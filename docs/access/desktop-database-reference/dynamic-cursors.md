---
title: 動的カーソル (Access デスクトップ データベースリファレンス)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 874f63e765e50ee127c9f2e0009dd164f247450d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602767"
---
# <a name="dynamic-cursors"></a>動的カーソル


**適用先**: Access 2013、Office 2013

動的カーソルは、結果セット内の行に対して加えられる変更を、それがカーソルの内側から行われたのか、カーソルの外側の他のユーザーによって行われたのかにかかわらず、すべて検出します。すべてのユーザーが実行したすべての挿入、更新、および削除のステートメントは、このカーソルを通じて確認できます。動的カーソルは、カーソルが開かれた後に結果セットに対して加えられた行、順序、および値の変更を、すべて検出できます。カーソルの外側で行われた更新は、コミットされるまで表示されません (ただし、カーソルのトランザクション分離レベルが "uncommitted" に設定されている場合を除きます)。

たとえば、カーソルが 2 つの行と他のアプリケーションをフェッチし、その後それらの行のうち 1 つを更新し、もう 1 つを削除した場合を考えてみます。その後、動的カーソルがこれらの行をフェッチすると、削除された行は検出されませんが、更新された行の新しい値は表示されます。

動的カーソルは、他のユーザーが同時に行った更新操作を、アプリケーションですべて検出する必要がある場合に便利です。ADO で動的カーソルを使用することを示すには、 **adOpenDynamic** **CursorTypeEnum** を使用します。

[前方のみカーソル](forward-only-cursors.md) | [静的カーソル](static-cursors.md) | [キーセット カーソル](keyset-cursors.md)

