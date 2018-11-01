---
title: Database.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92b4075f09bb34eca465f49d30a9ba8777b3e583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869653"
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

