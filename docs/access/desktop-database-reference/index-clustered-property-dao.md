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
# <a name="indexclustered-property-dao"></a><span data-ttu-id="13b5b-102">Index.Clustered プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="13b5b-102">Index.Clustered Property (DAO)</span></span>


<span data-ttu-id="13b5b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="13b5b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="13b5b-p101">**Index** オブジェクトがテーブルのクラスター化インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。ブール型 ( **Boolean**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="13b5b-p101">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b5b-106">構文</span><span class="sxs-lookup"><span data-stu-id="13b5b-106">Syntax</span></span>

<span data-ttu-id="13b5b-107">*式*です。クラスター化</span><span class="sxs-lookup"><span data-stu-id="13b5b-107">*expression* .Clustered</span></span>

<span data-ttu-id="13b5b-108">\*式\***インデックス**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="13b5b-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="13b5b-109">注釈</span><span class="sxs-lookup"><span data-stu-id="13b5b-109">Remarks</span></span>

<span data-ttu-id="13b5b-110">**Index** オブジェクトがクラスター化インデックスを表す場合、設定値または戻り値は、ブール データ型 (Boolean) の **True** です。</span><span class="sxs-lookup"><span data-stu-id="13b5b-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="13b5b-p102">クラスター化インデックスは、一部の IISAM デスクトップ データベース形式で使用されます。クラスター化インデックスは、組み合わせてテーブル内のすべてのレコードを定義済みの順序に配列する、1 つ以上の非キー フィールドで構成されます。クラスター化インデックスを使用すると、インデックス値が一意ではないテーブル内のレコードにも効率的にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="13b5b-p102">Some IISAM desktop database formats use clustered indexes. A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order. A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="13b5b-114">**Clustered** プロパティは、コレクションに追加されていない新しい **Index** オブジェクトの場合は値の設定と取得が可能で、 **Indexes** コレクションの既存の **Index** オブジェクトの場合は値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="13b5b-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="13b5b-115">Microsoft Access データベース エンジンはクラスター化インデックスをサポートしていないため、Microsoft Access データベース エンジン データベースでは <STRONG>Clustered</STRONG> プロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="13b5b-115">Microsoft Access database engine databases ignore the <STRONG>Clustered</STRONG> property because the Microsoft Access database engine doesn't support clustered indexes.</span></span></P>
> <LI>
> <P><span data-ttu-id="13b5b-116">ODBC データ ソースの場合、 <STRONG>Clustered</STRONG> プロパティは常に <STRONG>False</STRONG> を返し、ODBC データ ソースにクラスター化インデックスがあるかどうかは検出しません。</span><span class="sxs-lookup"><span data-stu-id="13b5b-116">For ODBC data sources the <STRONG>Clustered</STRONG> property always returns <STRONG>False</STRONG>; it does not detect whether or not the ODBC data source has a clustered index.</span></span></P></LI></UL>


