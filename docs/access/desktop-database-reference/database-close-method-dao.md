---
title: Close メソッド (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295024"
---
# <a name="databaseclose-method-dao"></a>Close メソッド (DAO)


**適用先:** Access 2013、Office 2013

開いている **Database** を閉じます。

## <a name="syntax"></a>構文

*式*。いったん

*式***Database**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Close** を使用したときに **Database** オブジェクトが既に閉じていた場合は、実行時エラーが発生します。

**Close**メソッドの代わりに、オブジェクト変数の値を**nothing**に設定します (dbsTemp = nothing を設定します)。

