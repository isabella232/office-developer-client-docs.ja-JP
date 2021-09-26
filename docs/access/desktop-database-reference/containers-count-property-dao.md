---
title: Containers.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f387b2815240ac8f285e05da434caf7d334e1fcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597577"
---
# <a name="containerscount-property-dao"></a>Containers.Count プロパティ (DAO)


**適用先**: Access 2013、Office 2013

**[Connections](connection-object-dao.md)** コレクション内の **[Connection](connections-collection-dao.md)** オブジェクトの数を返します。

## <a name="syntax"></a>構文

*式* .Count

*式*: **Connections** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。

**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。

