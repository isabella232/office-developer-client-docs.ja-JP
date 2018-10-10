---
title: Count プロパティ (ADO)
TOCTitle: Count Property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad02d854a560e3fa99bf7454c97083e88638c520
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477815"
---
# <a name="count-property-ado"></a>Count プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

コレクション内のオブジェクト数を示します。

## <a name="return-value"></a>戻り値

長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**Count** プロパティは、特定のコレクション内のオブジェクトの数を調べるために使います。

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使う場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。Microsoft Visual Basic で **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For** **Each...Next** コマンドを使います。

**Count** が 0 の場合、コレクションにはオブジェクトが含まれていないことを意味します。

