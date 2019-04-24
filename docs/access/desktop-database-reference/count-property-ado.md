---
title: Count プロパティ (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295472"
---
# <a name="count-property-ado"></a>Count プロパティ (ADO)


**適用先:** Access 2013、Office 2013

コレクション内のオブジェクト数を示します。

## <a name="return-value"></a>戻り値

長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

**Count** プロパティは、特定のコレクション内のオブジェクトの数を調べるために使います。

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使う場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。Microsoft Visual Basic で **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For** **Each...Next** コマンドを使います。

**Count** が 0 の場合、コレクションにはオブジェクトが含まれていないことを意味します。

