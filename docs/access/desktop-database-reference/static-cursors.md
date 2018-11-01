---
title: 静的カーソル (デスクトップ データベース参照のアクセス)
TOCTitle: Static Cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f60bce47f76214d26f75d13dece5bc062fd4db61
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889827"
---
# <a name="static-cursors"></a>静的カーソル


**適用されます**Access 2013、Office 2013。

静的カーソルは、カーソルを最初に開いたときの状態の結果セットを常に表示します。実装によって、静的カーソルは読み取り専用または読み取り/書き込みのいずれかで、前方および後方のスクロール機能を提供します。通常、静的カーソルでは、カーソルを開いた後にメンバーシップ、順序、または結果セットの値に加えられた変更を検出しません。静的カーソルは、カーソル自体の更新、削除、および挿入を検出できますが、そのような機能は不要です。

静的カーソルが、他の更新、削除、および挿入を検出することはありません。たとえば、静的カーソルが行をフェッチした後、別のアプリケーションがその行を更新したとします。アプリケーションが静的カーソルからその行を再フェッチすると、他のアプリケーションが変更を加えたにもかかわらず、表示される行の値は変わりません。すべての種類のスクロールがサポートされますが、ブックマークのサポートはプロバイダーによって異なります。

アプリケーションでデータの変更を検出する必要がなく、スクロールが必要な場合は、静的カーソルを選択することをお勧めします。ADO で静的カーソルを使用するように指定するには、 **adOpenStatic** **CursorTypeEnum** を使用します。

