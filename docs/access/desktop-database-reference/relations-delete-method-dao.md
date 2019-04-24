---
title: Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0b7fbf20a8732e8f4db525fd32bf4e5737b4d79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306966"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="f2107-102">Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="f2107-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="f2107-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2107-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2107-104">指定された **Relation** を **Relations** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="f2107-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2107-105">構文</span><span class="sxs-lookup"><span data-stu-id="f2107-105">Syntax</span></span>

<span data-ttu-id="f2107-106">*式*。削除 (***名前***)</span><span class="sxs-lookup"><span data-stu-id="f2107-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="f2107-107">\*式\***Relations**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2107-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2107-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2107-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2107-109">名前</span><span class="sxs-lookup"><span data-stu-id="f2107-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f2107-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="f2107-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f2107-111">データ型</span><span class="sxs-lookup"><span data-stu-id="f2107-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f2107-112">説明</span><span class="sxs-lookup"><span data-stu-id="f2107-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2107-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="f2107-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="f2107-114">必須</span><span class="sxs-lookup"><span data-stu-id="f2107-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f2107-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f2107-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f2107-116">削除するリレーションシップの名前です。</span><span class="sxs-lookup"><span data-stu-id="f2107-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f2107-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f2107-117">Remarks</span></span>

<span data-ttu-id="f2107-118">**Delete** メソッドは、 **Relation** オブジェクトが何も追加されていない新しいオブジェクトである場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f2107-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

