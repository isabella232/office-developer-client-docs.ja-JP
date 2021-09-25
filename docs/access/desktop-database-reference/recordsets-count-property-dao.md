---
title: Recordsets.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b39983dcfd0399667c7b19bb67c3fc64c7eac7ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589170"
---
# <a name="recordsetscount-property-dao"></a>Recordsets.Count プロパティ (DAO)


**適用先**: Access 2013、Office 2013

指定したコレクション内のオブジェクトの数を取得します。整数型 ( **Integer**) の値を使用します。

## <a name="syntax"></a>構文

*式* .Count

*式* Recordsets オブジェクトを **表す変数** 。

## <a name="remarks"></a>注釈

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。

**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。

