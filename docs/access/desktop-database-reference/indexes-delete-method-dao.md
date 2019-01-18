---
title: Indexes.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703546"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="06362-102">Indexes.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="06362-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="06362-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="06362-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06362-104">指定した **Index** を **Indexes** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="06362-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="06362-105">構文</span><span class="sxs-lookup"><span data-stu-id="06362-105">Syntax</span></span>

<span data-ttu-id="06362-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="06362-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="06362-107">\*式\***インデックス**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="06362-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="06362-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="06362-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06362-109">名前</span><span class="sxs-lookup"><span data-stu-id="06362-109">Name</span></span></p></th>
<th><p><span data-ttu-id="06362-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="06362-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="06362-111">データ型</span><span class="sxs-lookup"><span data-stu-id="06362-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="06362-112">説明</span><span class="sxs-lookup"><span data-stu-id="06362-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06362-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="06362-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="06362-114">必須</span><span class="sxs-lookup"><span data-stu-id="06362-114">Required</span></span></p></td>
<td><p><span data-ttu-id="06362-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="06362-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="06362-116">削除するインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="06362-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="06362-117">注釈</span><span class="sxs-lookup"><span data-stu-id="06362-117">Remarks</span></span>

<span data-ttu-id="06362-118">**削除**メソッドは、**インデックス**オブジェクトは、新しいされ、データベースに追加されていない場合にのみでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="06362-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

