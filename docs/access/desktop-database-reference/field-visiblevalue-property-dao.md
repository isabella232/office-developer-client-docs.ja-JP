---
title: VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292917"
---
# <a name="fieldvisiblevalue-property-dao"></a>VisibleValue プロパティ (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。VisibleValue

*式***Field**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

このプロパティには、サーバーのデータベース内に現在あるフィールドの値が含まれます。共有的バッチ更新を実行しているとき、最初のクライアントがデータを取得してからそれを更新するまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生することがあります。競合が発生した場合、このプロパティを使用すると 2 番目のクライアントが設定した値にアクセスできます。

