---
title: RDS には、[ストリーム未読"のエラーが返されます。
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 56bd90daef7b7571d8f0c6adca239ef24955f65a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944628"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS を返します\"ストリームの未読\"エラー


**適用されます**Access 2013、Office 2013。

"現在の位置がストリームの終わりにあるか、空のためストリーム オブジェクトを読み取れません。空でないストリームについては、現在の位置を Position プロパティで設定してください。ストリームが空かどうかを見るには、Size プロパティを確認してください。"

このエラーが発生した場合、http でパラメーター化された階層クエリを使用しようとしたことが原因である可能性があります。RDS では、パラメーター化された階層をリモートで操作できません。

