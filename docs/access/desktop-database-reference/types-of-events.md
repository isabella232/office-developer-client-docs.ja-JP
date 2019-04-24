---
title: イベントの種類 (Access デスクトップデータベースリファレンス)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314155"
---
# <a name="types-of-events"></a>イベントの種類


**適用先:** Access 2013、Office 2013



2 種類の基本的なイベントがあります。"Will イベント" は、操作の開始前に呼び出され、通常は **WillChangeRecordset** や **WillConnect** のように名前に "Will" が含まれます。イベントの完了後に呼び出されるイベントは、通常、 **RecordChangeComplete** や **ConnectComplete** のように名前に "Complete" が含まれます。 **InfoMessage** のような例外もありますが、このようなイベントは関連する操作の完了後に発生します。

## <a name="will-events"></a>Will イベント

操作の開始前に呼び出されるイベント ハンドラーを使用すると、操作パラメーターを検査または変更し、その操作を取り消したり、実行を許可したりすることができます。 これらのイベントハンドラールーチンの名前は、通常、* * * **と*いう形式になっています。

## <a name="complete-events"></a>Complete イベント

操作の完了後に呼び出されるイベント ハンドラーを使用すると、アプリケーションに操作の完了を通知することができます。 また、このようなイベント ハンドラーは、保留中の操作が Will イベント ハンドラーによって取り消されたときにも通知を受け取ります。 これらのイベントハンドラールーチンの名前は、通常、***event * Complete**の形式です。

Will イベントと Complete イベントは、通常、対で使用されます。

## <a name="other-events"></a>その他のイベント

その他のイベントハンドラー (つまり、名前が form ではないイベント * **** または ***event * Complete)** は、操作が完了した後にのみ呼び出されます。 このようなイベントとしては、 **Disconnect** 、 **EndOfRecordset** 、および **InfoMessage** があります。

