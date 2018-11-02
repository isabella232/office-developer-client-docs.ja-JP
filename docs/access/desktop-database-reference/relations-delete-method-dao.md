---
title: Relations.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462581e5b1ab3f09b697ee7f4b763a889d8119fd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925528"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="806fb-102">Relations.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="806fb-102">Relations.Delete method (DAO)</span></span>


<span data-ttu-id="806fb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="806fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="806fb-104">指定された **Relation** を **Relations** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="806fb-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="806fb-105">構文</span><span class="sxs-lookup"><span data-stu-id="806fb-105">Syntax</span></span>

<span data-ttu-id="806fb-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="806fb-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="806fb-107">\*式\***関係**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="806fb-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="806fb-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="806fb-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="806fb-109">名前</span><span class="sxs-lookup"><span data-stu-id="806fb-109">Name</span></span></p></th>
<th><p><span data-ttu-id="806fb-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="806fb-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="806fb-111">データ型</span><span class="sxs-lookup"><span data-stu-id="806fb-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="806fb-112">説明</span><span class="sxs-lookup"><span data-stu-id="806fb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="806fb-113">名前</span><span class="sxs-lookup"><span data-stu-id="806fb-113">Name</span></span></p></td>
<td><p><span data-ttu-id="806fb-114">必須</span><span class="sxs-lookup"><span data-stu-id="806fb-114">Required</span></span></p></td>
<td><p><span data-ttu-id="806fb-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="806fb-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="806fb-116">削除するリレーションシップの名前です。</span><span class="sxs-lookup"><span data-stu-id="806fb-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="806fb-117">注釈</span><span class="sxs-lookup"><span data-stu-id="806fb-117">Remarks</span></span>

<span data-ttu-id="806fb-118">**Delete** メソッドは、 **Relation** オブジェクトが何も追加されていない新しいオブジェクトである場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="806fb-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

