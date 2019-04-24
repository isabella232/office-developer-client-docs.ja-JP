---
title: '第 5 章: データの更新および永続化'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18dd63acd733624fba522ee7382f305d34019905
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296431"
---
# <a name="chapter-5-updating-and-persisting-data"></a>第 5 章: データの更新および永続化

**適用先:** Access 2013、Office 2013

これまでの章では、ADO を使用してデータ ソース内のデータにアクセスする方法、データ内を移動する方法、およびデータを編集する方法について説明しました。ユーザーがデータを変更できるようにするアプリケーションを構築する場合、これらの変更を保存する方法を理解しておく必要があります。 **Save** メソッドを使用して **Recordset** の変更をファイルに保存することも、 **Update** メソッドまたは **UpdateBatch** メソッドを使用して、変更内容をデータ ソースに返送して保存することもできます。

これまでの章では、 **Recordset** の複数の行で変更を行いました。ADO では、データ行の追加、削除、および変更に関連する 2 つの基本的な概念をサポートしています。

最初の概念は、変更が直ちに**Recordset**に加えられないことです。代わりに、内部*コピーバッファー*に対して行われます。 If you decide you don't want the changes, the modifications in the copy buffer are discarded. If you decide to keep the changes, the changes in the copy buffer are applied to the **Recordset**.

2番目の概念は、変更がデータソースに反映されるのは、行の作業が完了した直後 (つまり*即時*モード)、または一連の行に対するすべての変更が、設定完了の作業を宣言するまで収集される (つまり、、*バッチ*モード)。 The **LockType** property determines when the changes are made to the underlying data source. **adLockOptimistic** or **adLockPessimistic** specifies immediate mode, while **adLockBatchOptimistic** specifies batch mode. The **CursorLocation** property can affect which **LockType** settings are available. For instance, the **adLockPessimistic** setting is not supported if the **CursorLocation** property is set to **adUseClient**.

即時モードでは、**Update** メソッドを呼び出すたびに、変更がデータ ソースに反映されます。バッチ モードでは、**Update** を呼び出すか、現在の行の位置が移動されるたびに、変更内容がコピー バッファーに保存されますが、データ ソースに変更を反映するのは **UpdateBatch** メソッドのみです。

この章では、次のトピックについて説明します。

- [データを更新する (ADO)](updating-data.md)
- [データを永続化する (ADO)](persisting-data.md)
