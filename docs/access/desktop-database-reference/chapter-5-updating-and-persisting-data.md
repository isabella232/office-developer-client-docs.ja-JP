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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721711"
---
# <a name="chapter-5-updating-and-persisting-data"></a>第 5 章: データの更新および永続化

**適用されます**Access 2013、Office 2013。

これまでの章では、ADO を使用してデータ ソース内のデータにアクセスする方法、データ内を移動する方法、およびデータを編集する方法について説明しました。ユーザーがデータを変更できるようにするアプリケーションを構築する場合、これらの変更を保存する方法を理解しておく必要があります。 **Save** メソッドを使用して **Recordset** の変更をファイルに保存することも、 **Update** メソッドまたは **UpdateBatch** メソッドを使用して、変更内容をデータ ソースに返送して保存することもできます。

これまでの章では、 **Recordset** の複数の行で変更を行いました。ADO では、データ行の追加、削除、および変更に関連する 2 つの基本的な概念をサポートしています。

最初の概念はすぐに変更する**レコード セット**です。代わりに、内部*バッファーのコピー*に加えられました。 変更したくない場合は、コピー バッファー内の変更は破棄されます。 変更を維持することにした場合は、コピー バッファー内の変更が**レコード セット**に適用されます。

変更は、行を完全な (つまり、*イミディ エイト*モード) の操作を宣言するか (つまり完全な一連の作業時間を宣言するまでの行のセットに対するすべての変更を収集すると、すぐにデータ ソースに反映かの 2 つ目の概念は、します。、*バッチ*モード)。 **LockType**プロパティは、基になるデータ ソースへの変更があったときを決定します。 **adLockOptimistic**または**adLockPessimistic**は、 **adLockBatchOptimistic**はバッチ モードを指定するときにイミディ エイト モードを指定します。 **LockType**設定が使用可能な**CursorLocation**プロパティに影響します。 **CursorLocation**プロパティが**adUseClient**に設定されて場合、 **adLockPessimistic**設定はサポートされません。

即時モードでは、 **Update** メソッドを呼び出すたびに、変更がデータ ソースに反映されます。バッチ モードでは、 **Update** を呼び出すか、現在の行の位置が移動されるたびに、変更内容がコピー バッファーに保存されますが、データ ソースに変更を反映するのは **UpdateBatch** メソッドのみです。

この章では、次のトピックについて説明します。

- [(ADO) のデータを更新します。](updating-data.md)
- [(ADO) データを保持します。](persisting-data.md)
