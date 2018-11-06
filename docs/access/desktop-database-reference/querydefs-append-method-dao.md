---
title: QueryDefs.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84c7756515343d4a8d3493ac8b5949557785210f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998687"
---
# <a name="querydefsappend-method-dao"></a><span data-ttu-id="327b2-102">QueryDefs.Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="327b2-102">QueryDefs.Append method (DAO)</span></span>

<span data-ttu-id="327b2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="327b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="327b2-104">新しい **QueryDef** を **QueryDefs** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="327b2-104">Adds a new **QueryDef** to the **QueryDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="327b2-105">構文</span><span class="sxs-lookup"><span data-stu-id="327b2-105">Syntax</span></span>

<span data-ttu-id="327b2-106">*式*です。(***オブジェクト***) を追加します。</span><span class="sxs-lookup"><span data-stu-id="327b2-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="327b2-107">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="327b2-107">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="327b2-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="327b2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="327b2-109">名前</span><span class="sxs-lookup"><span data-stu-id="327b2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="327b2-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="327b2-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="327b2-111">データ型</span><span class="sxs-lookup"><span data-stu-id="327b2-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="327b2-112">説明</span><span class="sxs-lookup"><span data-stu-id="327b2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="327b2-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="327b2-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="327b2-114">必須</span><span class="sxs-lookup"><span data-stu-id="327b2-114">Required</span></span></p></td>
<td><p><span data-ttu-id="327b2-115"><strong>オブジェクト型 (Object)</strong></span><span class="sxs-lookup"><span data-stu-id="327b2-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="327b2-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="327b2-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="327b2-117">注釈</span><span class="sxs-lookup"><span data-stu-id="327b2-117">Remarks</span></span>

<span data-ttu-id="327b2-118">追加されたオブジェクトは、ディスクに格納され、 **Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="327b2-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="327b2-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける可能性がある場合は、そのコレクションに対して **Refresh** メソッドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="327b2-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="327b2-120">追加するオブジェクトが完全ではない場合 ( **Indexes** コレクションに **Index** オブジェクトを追加する前に、その **Fields** コレクションに **Field** オブジェクトが追加されていない場合など) や、1 つ以上の下位オブジェクトで設定されているプロパティが正しくない場合は、 **Append** メソッドを使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="327b2-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="327b2-121">たとえば、実行時エラーは、フィールドの種類を指定するいないし、 **TableDef**オブジェクトの**Fields**コレクションに**Field**オブジェクトを追加しようとしに**Append**メソッドを使用してトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="327b2-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

