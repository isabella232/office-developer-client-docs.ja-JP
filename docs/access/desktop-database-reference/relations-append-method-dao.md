---
title: Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b8374832ad6cd6bac30fa9d129e54fb6ab4c8fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306987"
---
# <a name="relationsappend-method-dao"></a><span data-ttu-id="67399-102">Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="67399-102">Relations.Append method (DAO)</span></span>

<span data-ttu-id="67399-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="67399-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67399-104">新しい **Relation** を **Relations** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="67399-104">Adds a new **Relation** to the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="67399-105">構文</span><span class="sxs-lookup"><span data-stu-id="67399-105">Syntax</span></span>

<span data-ttu-id="67399-106">*式*。Append (***Object***)</span><span class="sxs-lookup"><span data-stu-id="67399-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="67399-107">\*式\***Relations**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="67399-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="67399-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="67399-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67399-109">名前</span><span class="sxs-lookup"><span data-stu-id="67399-109">Name</span></span></p></th>
<th><p><span data-ttu-id="67399-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="67399-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="67399-111">データ型</span><span class="sxs-lookup"><span data-stu-id="67399-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="67399-112">説明</span><span class="sxs-lookup"><span data-stu-id="67399-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67399-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="67399-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="67399-114">必須</span><span class="sxs-lookup"><span data-stu-id="67399-114">Required</span></span></p></td>
<td><p><span data-ttu-id="67399-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="67399-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="67399-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="67399-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="67399-117">注釈</span><span class="sxs-lookup"><span data-stu-id="67399-117">Remarks</span></span>

<span data-ttu-id="67399-118">追加されたオブジェクトは、ディスクに格納され、**Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="67399-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="67399-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける場合は、そのコレクションの **Refresh** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67399-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="67399-p101">追加しようとしているオブジェクトが不完全である (たとえば、**Indexes** コレクションに追加する前に **Index** オブジェクトの **Fields** コレクションに **Field** オブジェクトが 1 つも追加されていない) 場合や、1 つ以上の従属オブジェクトのプロパティが正しく設定されていない場合、**Append** メソッドを使用すると、エラーが発生します。たとえば、フィールドの種類が指定されていないのに、**TableDef** オブジェクトの **Fields** コレクションに **Field** オブジェクトを追加しようとすると、**Append** メソッドで実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="67399-p101">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error. For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

