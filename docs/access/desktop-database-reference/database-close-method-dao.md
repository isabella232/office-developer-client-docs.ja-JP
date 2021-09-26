---
title: Database.Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5676ad0289891fad442e5670fc0d3d9c8d769419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618267"
---
# <a name="databaseclose-method-dao"></a>Database.Close メソッド (DAO)


**適用先**: Access 2013、Office 2013

開いている **Database** を閉じます。

## <a name="syntax"></a>構文

*式* .Close

*式* **Database** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Close** を使用したときに **Database** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。

**Close** メソッドに代わる方法は、オブジェクト変数の値を **Nothing** に設定することです (Set dbsTemp = Nothing)。

