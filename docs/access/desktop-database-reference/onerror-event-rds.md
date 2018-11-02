---
title: onError イベント (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c67e277c35e3cf6c75226dc138aa4b288843e6bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930862"
---
# <a name="onerror-event-rds"></a>onError イベント (RDS)


**適用されます**Access 2013、Office 2013。

**onError** イベントは、処理中にエラーが発生するたびに呼び出されます。

## <a name="syntax"></a>構文

onError*SCode*、*説明*、*ソース*、 *CancelDisplay*

## <a name="parameters"></a>パラメーター

  - *SCode*

  - エラーの状態コードを表す整数型の値です。

  - *Description*

  - エラーの説明を表す文字列型 ( **String** ) の値です。

  - *Source*

  - エラーを発生させたクエリまたはコマンドを表す文字列型 ( **String** ) の値です。

  - *CancelDisplay*

  - ブール型 ( **Boolean** ) の値であり、 **True** に設定するとダイアログ ボックスにエラーが表示されなくなります。

