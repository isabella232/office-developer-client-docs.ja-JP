---
title: TableDefs.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999009"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="505ca-102">TableDefs.Delete メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="505ca-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="505ca-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="505ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="505ca-104">指定された **TableDef** オブジェクトを **TableDefs** コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="505ca-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="505ca-105">構文</span><span class="sxs-lookup"><span data-stu-id="505ca-105">Syntax</span></span>

<span data-ttu-id="505ca-106">*式*です。(***名前***) を削除します。</span><span class="sxs-lookup"><span data-stu-id="505ca-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="505ca-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="505ca-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="505ca-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="505ca-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="505ca-109">名前</span><span class="sxs-lookup"><span data-stu-id="505ca-109">Name</span></span></p></th>
<th><p><span data-ttu-id="505ca-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="505ca-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="505ca-111">データ型</span><span class="sxs-lookup"><span data-stu-id="505ca-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="505ca-112">説明</span><span class="sxs-lookup"><span data-stu-id="505ca-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="505ca-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="505ca-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="505ca-114">必須</span><span class="sxs-lookup"><span data-stu-id="505ca-114">Required</span></span></p></td>
<td><p><span data-ttu-id="505ca-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="505ca-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="505ca-116">削除する TableDef の名前です。</span><span class="sxs-lookup"><span data-stu-id="505ca-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="505ca-117">注釈</span><span class="sxs-lookup"><span data-stu-id="505ca-117">Remarks</span></span>

<span data-ttu-id="505ca-118">**テーブル定義**オブジェクトが新しいし、データベースに追加されていない場合にのみ、または**テーブル定義**の**更新できる**プロパティが**True**に設定すると、Delete メソッドはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="505ca-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

