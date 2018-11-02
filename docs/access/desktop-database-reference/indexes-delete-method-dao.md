---
title: Indexes.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66f08fa9733de0b63ca8bb659972abbc59183e16
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922322"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="b4365-102">Indexes.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="b4365-102">Indexes.Delete method (DAO)</span></span>


<span data-ttu-id="b4365-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b4365-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4365-104">指定した **Index** を **Indexes** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="b4365-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4365-105">構文</span><span class="sxs-lookup"><span data-stu-id="b4365-105">Syntax</span></span>

<span data-ttu-id="b4365-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="b4365-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="b4365-107">\*式\***インデックス**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="b4365-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b4365-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b4365-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4365-109">名前</span><span class="sxs-lookup"><span data-stu-id="b4365-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b4365-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="b4365-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b4365-111">データ型</span><span class="sxs-lookup"><span data-stu-id="b4365-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b4365-112">説明</span><span class="sxs-lookup"><span data-stu-id="b4365-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4365-113">名前</span><span class="sxs-lookup"><span data-stu-id="b4365-113">Name</span></span></p></td>
<td><p><span data-ttu-id="b4365-114">必須</span><span class="sxs-lookup"><span data-stu-id="b4365-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b4365-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="b4365-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b4365-116">削除するインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4365-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b4365-117">注釈</span><span class="sxs-lookup"><span data-stu-id="b4365-117">Remarks</span></span>

<span data-ttu-id="b4365-118">**削除**メソッドは、**インデックス**オブジェクトは、新しいされ、データベースに追加されていない場合にのみでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b4365-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

