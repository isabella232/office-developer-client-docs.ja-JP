---
title: Index.Clustered プロパティ (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 5ef312233b77170f0f6b42c9aa8e133ff4851ab3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626408"
---
# <a name="indexclustered-property-dao"></a>Index.Clustered プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**Index** オブジェクトがテーブルのクラスター化インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。ブール型 ( **Boolean**) の値を使用します。

## <a name="syntax"></a>構文

*式* .クラスター化

*式* Index オブジェクトを返す **式** 。

## <a name="remarks"></a>注釈

**Index** オブジェクトがクラスター化インデックスを表す場合、設定値または戻り値は、ブール データ型 (Boolean) の **True** です。

クラスター化インデックスは、一部の IISAM デスクトップ データベース形式で使用されます。クラスター化インデックスは、組み合わせてテーブル内のすべてのレコードを定義済みの順序に配列する、1 つ以上の非キー フィールドで構成されます。クラスター化インデックスを使用すると、インデックス値が一意ではないテーブル内のレコードにも効率的にアクセスできます。

**Clustered** プロパティは、コレクションに追加されていない新しい **Index** オブジェクトの場合は値の設定と取得が可能で、 **Indexes** コレクションの既存の **Index** オブジェクトの場合は値の取得のみが可能です。

> [!NOTE]
> - Microsoft Access データベース エンジンはクラスター化インデックスをサポートしていないため、Microsoft Access データベース エンジン データベースでは **Clustered** プロパティは無視されます。
> - ODBC データ ソースの場合 **、Clustered プロパティ** は常に False を **返します**。ODBC データ ソースにクラスター化インデックスがあるかどうかは検出されません。


