---
title: Field.VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5b99b60edbe6b14091a81cf9f48c6a894932b083
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622334"
---
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue プロパティ (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .VisibleValue

*expression*: **Field** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

このプロパティには、サーバーのデータベース内に現在あるフィールドの値が含まれます。共有的バッチ更新を実行しているとき、最初のクライアントがデータを取得してからそれを更新するまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生することがあります。競合が発生した場合、このプロパティを使用すると 2 番目のクライアントが設定した値にアクセスできます。

