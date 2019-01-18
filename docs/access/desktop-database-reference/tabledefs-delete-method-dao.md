---
title: TableDefs.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709321"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="f7e60-102">TableDefs.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7e60-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="f7e60-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f7e60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7e60-104">指定された **TableDef** オブジェクトを **TableDefs** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="f7e60-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e60-105">構文</span><span class="sxs-lookup"><span data-stu-id="f7e60-105">Syntax</span></span>

<span data-ttu-id="f7e60-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="f7e60-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="f7e60-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f7e60-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7e60-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7e60-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7e60-109">名前</span><span class="sxs-lookup"><span data-stu-id="f7e60-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f7e60-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="f7e60-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f7e60-111">データ型</span><span class="sxs-lookup"><span data-stu-id="f7e60-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f7e60-112">説明</span><span class="sxs-lookup"><span data-stu-id="f7e60-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7e60-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="f7e60-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="f7e60-114">必須</span><span class="sxs-lookup"><span data-stu-id="f7e60-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f7e60-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f7e60-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f7e60-116">削除する TableDef の名前です。</span><span class="sxs-lookup"><span data-stu-id="f7e60-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f7e60-117">注釈</span><span class="sxs-lookup"><span data-stu-id="f7e60-117">Remarks</span></span>

<span data-ttu-id="f7e60-118">**テーブル定義**オブジェクトが新しいし、データベースに追加されていない場合にのみ、または**テーブル定義**の**更新できる**プロパティが**True**に設定すると、Delete メソッドはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f7e60-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

