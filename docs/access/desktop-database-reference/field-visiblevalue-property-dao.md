---
title: Field.VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 461b8c43bf9000e5ecde3a3676cebf54be8e4166
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927572"
---
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

## <a name="syntax"></a>構文

*式*です。VisibleValue

*式***Field**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

このプロパティは、サーバーのデータベースに現在存在しているフィールドの値を格納します。共有的バッチ更新中、最初のクライアントがデータを取得してから更新を試行するまでの間に、2 番目のクライアントが同じフィールドとレコードを変更すると、競合が発生する可能性があります。この場合、2 番目のクライアントが設定した値にこのプロパティからアクセスできます。

