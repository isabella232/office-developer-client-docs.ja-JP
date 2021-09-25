---
title: Parameters.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: bc8c814b-da55-22b7-431f-a0f7e6cac994
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822720(v=office.15)
ms:contentKeyID: 48547415
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ceb75ee4c4e262b39ecd30957270228b94dd0fb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581015"
---
# <a name="parameterscount-property-dao"></a>Parameters.Count プロパティ (DAO)


**適用先:** Access 2013、Office 2013

指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。

## <a name="syntax"></a>構文

*式* .Count

*式*: **Parameters** オブジェクトを表す変数。

## <a name="remarks"></a>解説

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。

**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。

