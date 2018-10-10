---
title: Relations.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b228c21931131023d58efc91d0087ad76ca3b61
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477154"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="82dc3-102">Relations.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="82dc3-102">Relations.Delete Method (DAO)</span></span>


<span data-ttu-id="82dc3-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="82dc3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="82dc3-104">指定された **Relation** を **Relations** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="82dc3-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dc3-105">構文</span><span class="sxs-lookup"><span data-stu-id="82dc3-105">Syntax</span></span>

<span data-ttu-id="82dc3-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="82dc3-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="82dc3-107">\*式\***関係**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="82dc3-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="82dc3-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82dc3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82dc3-109">名前</span><span class="sxs-lookup"><span data-stu-id="82dc3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="82dc3-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="82dc3-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="82dc3-111">データ型</span><span class="sxs-lookup"><span data-stu-id="82dc3-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="82dc3-112">説明</span><span class="sxs-lookup"><span data-stu-id="82dc3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82dc3-113">名前</span><span class="sxs-lookup"><span data-stu-id="82dc3-113">Name</span></span></p></td>
<td><p><span data-ttu-id="82dc3-114">必須</span><span class="sxs-lookup"><span data-stu-id="82dc3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="82dc3-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="82dc3-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="82dc3-116">削除するリレーションシップの名前です。</span><span class="sxs-lookup"><span data-stu-id="82dc3-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="82dc3-117">注釈</span><span class="sxs-lookup"><span data-stu-id="82dc3-117">Remarks</span></span>

<span data-ttu-id="82dc3-118">**Delete** メソッドは、 **Relation** オブジェクトが何も追加されていない新しいオブジェクトである場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="82dc3-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

