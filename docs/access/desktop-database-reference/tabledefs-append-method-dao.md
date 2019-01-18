---
title: TableDefs.Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31eca3f4ca5993a401bd85a4b04299a8697c16e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702790"
---
# <a name="tabledefsappend-method-dao"></a><span data-ttu-id="95da0-102">TableDefs.Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="95da0-102">TableDefs.Append method (DAO)</span></span>

<span data-ttu-id="95da0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="95da0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95da0-104">新しい **TableDef** を **TableDefs** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="95da0-104">Adds a new **TableDef** to the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="95da0-105">構文</span><span class="sxs-lookup"><span data-stu-id="95da0-105">Syntax</span></span>

<span data-ttu-id="95da0-106">*式*です。(***オブジェクト***) を追加します。</span><span class="sxs-lookup"><span data-stu-id="95da0-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="95da0-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="95da0-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="95da0-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="95da0-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95da0-109">名前</span><span class="sxs-lookup"><span data-stu-id="95da0-109">Name</span></span></p></th>
<th><p><span data-ttu-id="95da0-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="95da0-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="95da0-111">データ型</span><span class="sxs-lookup"><span data-stu-id="95da0-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="95da0-112">説明</span><span class="sxs-lookup"><span data-stu-id="95da0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95da0-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="95da0-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="95da0-114">必須</span><span class="sxs-lookup"><span data-stu-id="95da0-114">Required</span></span></p></td>
<td><p><span data-ttu-id="95da0-115"><strong>オブジェクト型 (Object)</strong></span><span class="sxs-lookup"><span data-stu-id="95da0-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="95da0-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="95da0-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="95da0-117">注釈</span><span class="sxs-lookup"><span data-stu-id="95da0-117">Remarks</span></span>

<span data-ttu-id="95da0-118">追加されたオブジェクトは、ディスクに格納され、 **Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="95da0-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="95da0-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける可能性がある場合は、そのコレクションに対して **Refresh** メソッドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95da0-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="95da0-120">追加するオブジェクトが完全ではない場合 ( **Indexes** コレクションに **Index** オブジェクトを追加する前に、その **Fields** コレクションに **Field** オブジェクトが追加されていない場合など) や、1 つ以上の下位オブジェクトで設定されているプロパティが正しくない場合は、 **Append** メソッドを使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="95da0-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="95da0-121">たとえば、実行時エラーは、フィールドの種類を指定するいないし、 **TableDef**オブジェクトの**Fields**コレクションに**Field**オブジェクトを追加しようとしに**Append**メソッドを使用してトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="95da0-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

