---
title: イベントの種類 (Access デスクトップ データベースリファレンス)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 23b4b794b72e06695b633cb6b2dc4540b3aa0356
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562147"
---
# <a name="types-of-events"></a>イベントの種類


**適用先:** Access 2013、Office 2013



2 種類の基本的なイベントがあります。"Will イベント" は、操作の開始前に呼び出され、通常は **WillChangeRecordset** や **WillConnect** のように名前に "Will" が含まれます。イベントの完了後に呼び出されるイベントは、通常、 **RecordChangeComplete** や **ConnectComplete** のように名前に "Complete" が含まれます。 **InfoMessage** のような例外もありますが、このようなイベントは関連する操作の完了後に発生します。

## <a name="will-events"></a>Will イベント

操作の開始前に呼び出されるイベント ハンドラーを使用すると、操作パラメーターを検査または変更し、その操作を取り消したり、実行を許可したりすることができます。 これらのイベント ハンドラー ルーチンは、通常、フォーム **Will Event**** の名前を持っています。

## <a name="complete-events"></a>Complete イベント

操作の完了後に呼び出されるイベント ハンドラーを使用すると、アプリケーションに操作の完了を通知することができます。 また、このようなイベント ハンドラーは、保留中の操作が Will イベント ハンドラーによって取り消されたときにも通知を受け取ります。 これらのイベント ハンドラー ルーチンは、通常、フォーム ***Event*Complete の名前を持ちます**。

Will イベントと Complete イベントは、通常、対で使用されます。

## <a name="other-events"></a>その他のイベント

その他のイベント ハンドラー (名前が **Will*Event*** または _Event_Complete の形式ではないイベント **)** は、操作が完了した後にのみ呼び出されます。 このようなイベントとしては、 **Disconnect** 、 **EndOfRecordset** 、および **InfoMessage** があります。

