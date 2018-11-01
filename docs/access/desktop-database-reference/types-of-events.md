---
title: (デスクトップ データベース参照のアクセス) のイベントの種類
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a420623e467fd4ba0609db5023ca0d5cec25eb38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884493"
---
# <a name="types-of-events"></a>イベントの種類


**適用されます**Access 2013、Office 2013。



2 種類の基本的なイベントがあります。"Will イベント" は、操作の開始前に呼び出され、通常は **WillChangeRecordset** や **WillConnect** のように名前に "Will" が含まれます。イベントの完了後に呼び出されるイベントは、通常、 **RecordChangeComplete** や **ConnectComplete** のように名前に "Complete" が含まれます。 **InfoMessage** のような例外もありますが、このようなイベントは関連する操作の完了後に発生します。

## <a name="will-events"></a>Will イベント

操作の開始前に呼び出されるイベント ハンドラーを使用すると、操作パラメーターを検査または変更し、その操作を取り消したり、実行を許可したりすることができます。 これらのイベント ハンドラー ルーチンは通常のフォームの名前を持つ **は*イベント。。

## <a name="complete-events"></a>Complete イベント

操作の完了後に呼び出されるイベント ハンドラーを使用すると、アプリケーションに操作の完了を通知することができます。 また、このようなイベント ハンドラーは、保留中の操作が Will イベント ハンドラーによって取り消されたときにも通知を受け取ります。 これらのイベント ハンドラー ルーチンは通常のフォームの名前を持つ ***イベント * 完了**。

Will イベントと Complete イベントは、通常、対で使用されます。

## <a name="other-events"></a>その他のイベント

他のイベント ハンドラー、名前の形式ではないイベントは、**は * イベント*** または ***イベント * 完了-** 操作の完了後にのみ呼び出されます。 このようなイベントとしては、 **Disconnect** 、 **EndOfRecordset** 、および **InfoMessage** があります。

