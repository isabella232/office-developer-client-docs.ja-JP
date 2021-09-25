---
title: RDS によって返される「ストリームが読み取れません」のエラー
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b67aa319e645aa0a17a20e3545679e6e6385a4fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568601"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS はストリームの \" 読み取りエラーを返 \" します


**適用先:** Access 2013、Office 2013

"現在の位置がストリームの終わりにあるか、空のためストリーム オブジェクトを読み取れません。空でないストリームについては、現在の位置を Position プロパティで設定してください。ストリームが空かどうかを見るには、Size プロパティを確認してください。"

このエラーが発生した場合、http でパラメーター化された階層クエリを使用しようとしたことが原因である可能性があります。RDS では、パラメーター化された階層をリモートで操作できません。

