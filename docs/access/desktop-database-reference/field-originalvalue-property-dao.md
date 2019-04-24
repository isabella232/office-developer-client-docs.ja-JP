---
title: フィールドの originalvalue プロパティ (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293001"
---
# <a name="fieldoriginalvalue-property-dao"></a>フィールドの originalvalue プロパティ (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。OriginalValue

*式***Field**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

共有的バッチ更新の実行中に、最初のクライアントがデータを取得してから、最初のクライアントの更新が試行されるまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生する可能性があります。 **OriginalValue** プロパティには、最後のバッチ **Update** が開始された時点のフィールドの値が含まれています。バッチ **Update** によりデータベースに書き込もうとしたときに、この値が実際にはデータベースの値と一致していない場合、競合が発生します。この場合、 **[VisibleValue](field-visiblevalue-property-dao.md)** プロパティを使用してデータベースの新しい値にアクセスできます。

