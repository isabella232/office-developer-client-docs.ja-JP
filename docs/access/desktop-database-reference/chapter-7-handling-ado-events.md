---
title: '第 7 章: ADO イベントの処理'
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e5cd1d46441cb073d1b5a9b5361c8ea3bac15aa8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627087"
---
# <a name="chapter-7-handling-ado-events"></a>第 7 章: ADO イベントの処理

**適用先**: Access 2013、Office 2013

ADO イベント モデルでは、特定の同期および非同期の ADO 操作のうち、その操作の開始前または完了後に "イベント"、つまり通知を発行する操作をサポートしています。イベントの実体は、アプリケーション内に定義されたイベント ハンドラー ルーチンへの呼び出しです。

操作開始前に発生するイベントのグループに対してハンドラー関数またはプロシージャを記述すると、その操作に渡されたパラメーターを確認または変更することができます。この操作はまだ実行されていないので、その操作を取り消すことも、そのまま実行して完了することもできます。

操作完了後に発生するイベントのグループは、ADO を非同期で利用する場合に特に重要です。たとえば、アプリケーションで非同期の [Recordset.Open](open-method-ado-recordset.md) 操作を開始すると、操作の終了時に実行完了イベントによる通知を受け取ります。

ADO イベント モデルを使用するとアプリケーションのオーバーヘッドが増加しますが、オブジェクトの [State](state-property-ado.md) プロパティをループで監視するなどの非同期操作を利用する他の方法に比べて、このモデルの方がはるかに柔軟性があります。

この章では、次のトピックについて説明します。

- [ADO イベント ハンドラーの概要](ado-event-handler-summary.md)
- [イベントの種類](types-of-events.md)
- [イベント パラメーター](event-parameters.md)
- [イベント ハンドラーの共同作業の方法](how-event-handlers-work-together.md)
- [言語による ADO イベントのインスタンス化 (ADO)](ado-event-instantiation-by-language-ado.md)
