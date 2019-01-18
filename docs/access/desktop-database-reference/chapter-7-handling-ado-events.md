---
title: '第 7 章: ADO イベントの処理'
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7357cc60a3bddbf96c2abae39fecfb7107025e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699045"
---
# <a name="chapter-7-handling-ado-events"></a>第 7 章: ADO イベントの処理

**適用されます**Access 2013、Office 2013。

ADO イベント モデルでは、特定操作の開始前に、または終了後に、*イベント*、または、通知を発行する同期および非同期 ADO 操作をサポートします。 イベントは、実際には、アプリケーションで定義したイベント ハンドラーのルーチンの呼び出しです。

操作開始前に発生するイベントのグループに対してハンドラー関数またはプロシージャを記述すると、その操作に渡されたパラメーターを確認または変更することができます。この操作はまだ実行されていないので、その操作を取り消すことも、そのまま実行して完了することもできます。

操作完了後に発生するイベントのグループは、ADO を非同期で利用する場合に特に重要です。たとえば、アプリケーションで非同期の [Recordset.Open](open-method-ado-recordset.md) 操作を開始すると、操作の終了時に実行完了イベントによる通知を受け取ります。

ADO イベント モデルを使用するとアプリケーションのオーバーヘッドが増加しますが、オブジェクトの [State](state-property-ado.md) プロパティをループで監視するなどの非同期操作を利用する他の方法に比べて、このモデルの方がはるかに柔軟性があります。

この章では、次のトピックについて説明します。

- [ADO イベント ハンドラーの概要](ado-event-handler-summary.md)
- [イベントの種類](types-of-events.md)
- [イベント パラメーター](event-parameters.md)
- [イベント ハンドラーの共同作業の方法](how-event-handlers-work-together.md)
- [(ADO) の言語によって、ADO イベントのインスタンス化](ado-event-instantiation-by-language-ado.md)
