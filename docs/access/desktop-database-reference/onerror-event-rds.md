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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288477"
---
# <a name="onerror-event-rds"></a>onError イベント (RDS)

**適用先:** Access 2013、Office 2013

**onError** イベントは、処理中にエラーが発生するたびに呼び出されます。

## <a name="syntax"></a>構文

onError*SCode*、 *Description*、 *Source*、 *canceldisplay*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*SCode* |エラーの状態コードを表す整数型の値です。|
|*Description* |エラーの説明を表す文字列型 ( **String** ) の値です。|
|*Source* |エラーを発生させたクエリまたはコマンドを表す文字列型 ( **String** ) の値です。|
|*CancelDisplay* |ブール型 ( **Boolean** ) の値であり、 **True** に設定するとダイアログ ボックスにエラーが表示されなくなります。|

