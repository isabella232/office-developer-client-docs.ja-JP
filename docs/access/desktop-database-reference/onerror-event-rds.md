---
title: onError イベント (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49a9f5340ac12218ef2c1a85e9930566a147a3fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626261"
---
# <a name="onerror-event-rds"></a>onError イベント (RDS)

**適用先**: Access 2013、Office 2013

**onError** イベントは、処理中にエラーが発生するたびに呼び出されます。

## <a name="syntax"></a>構文

onError *SCode*, *Description*, *Source*, *CancelDisplay*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*SCode* |エラーの状態コードを表す整数型の値です。|
|*Description* |エラーの説明を表す文字列型 ( **String** ) の値です。|
|*Source* |エラーを発生させたクエリまたはコマンドを表す文字列型 ( **String** ) の値です。|
|*CancelDisplay* |ブール型 ( **Boolean** ) の値であり、 **True** に設定するとダイアログ ボックスにエラーが表示されなくなります。|

