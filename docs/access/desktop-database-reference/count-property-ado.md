---
title: Count プロパティ (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c31bd1d3c811fdb0faa8036e247c4aafe5223409
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586034"
---
# <a name="count-property-ado"></a>Count プロパティ (ADO)


**適用先**: Access 2013、Office 2013

コレクション内のオブジェクト数を示します。

## <a name="return-value"></a>戻り値

長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

**Count** プロパティは、特定のコレクション内のオブジェクトの数を調べるために使います。

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使う場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。Microsoft Visual Basic で **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For** **Each...Next** コマンドを使います。

**Count** が 0 の場合、コレクションにはオブジェクトが含まれていないことを意味します。

