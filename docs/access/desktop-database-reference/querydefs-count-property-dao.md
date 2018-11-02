---
title: QueryDefs.Count プロパティ (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5efc7479f69d379f406a9a7cda5d4c522df6325
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930897"
---
# <a name="querydefscount-property-dao"></a>QueryDefs.Count プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。

## <a name="syntax"></a>構文

*式*です。カウント

*式***クエリ定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使用する場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。 **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For Each...Next** コマンドを使用できます。

**Count** プロパティの設定値は、Null になることはありません。値が 0 の場合、そのコレクションにはオブジェクトがありません。

