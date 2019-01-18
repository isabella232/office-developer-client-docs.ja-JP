---
title: Database.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699977"
---
# <a name="databaseclose-method-dao"></a>Database.Close メソッド (DAO)


**適用されます**Access 2013、Office 2013。

開いている **Database** を閉じます。

## <a name="syntax"></a>構文

*式*です。閉じる

*式***データベース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** を使用したときに **Database** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。

代わりに、 **Close**メソッドは**Nothing**をオブジェクト変数の値を設定するのには、(dbsTemp の設定 = なし)。

