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
ms.openlocfilehash: 4cb0c51f454e4792a64fc55416464373ac667dcf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476494"
---
# <a name="indexclustered-property-dao"></a>Index.Clustered プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

**Index** オブジェクトがテーブルのクラスター化インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。ブール型 ( **Boolean**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。クラスター化

*式***インデックス**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

**Index** オブジェクトがクラスター化インデックスを表す場合、設定値または戻り値は、ブール データ型 (Boolean) の **True** です。

クラスター化インデックスは、一部の IISAM デスクトップ データベース形式で使用されます。クラスター化インデックスは、組み合わせてテーブル内のすべてのレコードを定義済みの順序に配列する、1 つ以上の非キー フィールドで構成されます。クラスター化インデックスを使用すると、インデックス値が一意ではないテーブル内のレコードにも効率的にアクセスできます。

**Clustered** プロパティは、コレクションに追加されていない新しい **Index** オブジェクトの場合は値の設定と取得が可能で、 **Indexes** コレクションの既存の **Index** オブジェクトの場合は値の取得のみが可能です。


> [!NOTE]
> <UL>
> <LI>
> <P>Microsoft Access データベース エンジンはクラスター化インデックスをサポートしていないため、Microsoft Access データベース エンジン データベースでは <STRONG>Clustered</STRONG> プロパティは無視されます。</P>
> <LI>
> <P>ODBC データ ソースの場合、 <STRONG>Clustered</STRONG> プロパティは常に <STRONG>False</STRONG> を返し、ODBC データ ソースにクラスター化インデックスがあるかどうかは検出しません。</P></LI></UL>


