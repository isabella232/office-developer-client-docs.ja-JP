---
title: Field2 value プロパティ (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e3da5f7438ae83010c6ecc109dccf5d7a8eb9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292742"
---
# <a name="field2originalvalue-property-dao"></a>Field2 value プロパティ (DAO)


**適用先:** Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*。OriginalValue

*式***Field2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

共有的バッチ更新の実行中に、最初のクライアントがデータを取得してから、最初のクライアントの更新が試行されるまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生する可能性があります。 **OriginalValue** プロパティには、最後のバッチ **Update** が開始された時点のフィールドの値が含まれています。バッチ **Update** によりデータベースに書き込もうとしたときに、この値が実際にはデータベースの値と一致していない場合、競合が発生します。この場合、 **VisibleValue** プロパティを使用してデータベースの新しい値にアクセスできます。

