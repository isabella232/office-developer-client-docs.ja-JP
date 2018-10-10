---
title: Workspaces.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: bc7c5a11-13d3-27bd-1be4-5d069e888ac2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822719(v=office.15)
ms:contentKeyID: 48547414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 354b2e6efad810a4c817ba8569dd47c270c2fa8d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476181"
---
# <a name="workspacescount-property-dao"></a>Workspaces.Count プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。

## <a name="syntax"></a>構文

*式*です。カウント

*式***ワークスペース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。

**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。

