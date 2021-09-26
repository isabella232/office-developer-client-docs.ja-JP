---
title: Field2.VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 82e3e113290bd34adfcf79e5bc429c539c757f29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626695"
---
# <a name="field2visiblevalue-property-dao"></a>Field2.VisibleValue プロパティ (DAO)


**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .VisibleValue

*式***Field2** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

このプロパティには、サーバーのデータベース内に現在あるフィールドの値が含まれます。共有的バッチ更新を実行しているとき、最初のクライアントがデータを取得してからそれを更新するまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生することがあります。競合が発生した場合、このプロパティを使用すると 2 番目のクライアントが設定した値にアクセスできます。

