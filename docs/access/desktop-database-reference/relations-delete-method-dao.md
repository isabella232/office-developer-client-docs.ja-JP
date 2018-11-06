---
title: Relations.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998925"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="c29ef-102">Relations.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="c29ef-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="c29ef-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c29ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c29ef-104">指定された **Relation** を **Relations** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="c29ef-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c29ef-105">構文</span><span class="sxs-lookup"><span data-stu-id="c29ef-105">Syntax</span></span>

<span data-ttu-id="c29ef-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="c29ef-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="c29ef-107">\*式\***関係**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c29ef-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c29ef-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29ef-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c29ef-109">名前</span><span class="sxs-lookup"><span data-stu-id="c29ef-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c29ef-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="c29ef-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c29ef-111">データ型</span><span class="sxs-lookup"><span data-stu-id="c29ef-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c29ef-112">説明</span><span class="sxs-lookup"><span data-stu-id="c29ef-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c29ef-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="c29ef-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="c29ef-114">必須</span><span class="sxs-lookup"><span data-stu-id="c29ef-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c29ef-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="c29ef-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c29ef-116">削除するリレーションシップの名前です。</span><span class="sxs-lookup"><span data-stu-id="c29ef-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c29ef-117">注釈</span><span class="sxs-lookup"><span data-stu-id="c29ef-117">Remarks</span></span>

<span data-ttu-id="c29ef-118">**Delete** メソッドは、 **Relation** オブジェクトが何も追加されていない新しいオブジェクトである場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c29ef-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

