---
title: onError イベント (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712177"
---
# <a name="onerror-event-rds"></a>onError イベント (RDS)

**適用されます**Access 2013、Office 2013。

**onError** イベントは、処理中にエラーが発生するたびに呼び出されます。

## <a name="syntax"></a>構文

onError*SCode*、*説明*、*ソース*、 *CancelDisplay*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*SCode* |エラーの状態コードを表す整数型の値です。|
|*Description* |エラーの説明を表す文字列型 ( **String** ) の値です。|
|*Source* |エラーを発生させたクエリまたはコマンドを表す文字列型 ( **String** ) の値です。|
|*CancelDisplay* |ブール型 ( **Boolean** ) の値であり、 **True** に設定するとダイアログ ボックスにエラーが表示されなくなります。|

