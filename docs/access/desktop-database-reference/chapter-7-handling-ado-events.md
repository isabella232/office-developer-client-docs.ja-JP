---
title: '7 章: ADO イベントを処理する'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 816dd98e5e4c21f3159edf18b5687b2b0578e399
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860841"
---
# <a name="chapter-7-handling-ado-events"></a>7 章: ADO イベントを処理する


**適用されます**Access 2013 |。Office 2013

ADO イベント モデルでは、特定操作の開始前に、または終了後に、*イベント*、または、通知を発行する同期および非同期 ADO 操作をサポートします。 イベントは、実際には、アプリケーションで定義したイベント ハンドラーのルーチンの呼び出しです。

操作開始前に発生するイベントのグループに対してハンドラー関数またはプロシージャを記述すると、その操作に渡されたパラメーターを確認または変更することができます。この操作はまだ実行されていないので、その操作を取り消すことも、そのまま実行して完了することもできます。

操作完了後に発生するイベントのグループは、ADO を非同期で利用する場合に特に重要です。たとえば、アプリケーションで非同期の [Recordset.Open](open-method-ado-recordset.md) 操作を開始すると、操作の終了時に実行完了イベントによる通知を受け取ります。

ADO イベント モデルを使用するとアプリケーションのオーバーヘッドが増加しますが、オブジェクトの [State](state-property-ado.md) プロパティをループで監視するなどの非同期操作を利用する他の方法に比べて、このモデルの方がはるかに柔軟性があります。

この章では、次のトピックについて説明します。

- [ADO イベント ハンドラーの概要](ado-event-handler-summary.md)

- [イベントの種類](types-of-events.md)

- [イベント パラメーター](event-parameters.md)

- [複数のイベント ハンドラーとの共同作業](how-event-handlers-work-together.md)

- [ADO イベントのインスタンス化 (言語別) (ADO)](ado-event-instantiation-by-language-ado.md)