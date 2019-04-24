---
title: Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 528809495ebefd15a8895b15a9d51f84e6892980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301310"
---
# <a name="propertiesappend-method-dao"></a><span data-ttu-id="6722e-102">Append メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="6722e-102">Properties.Append method (DAO)</span></span>

<span data-ttu-id="6722e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6722e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6722e-104">新しい **Property** を **Properties** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="6722e-104">Adds a new **Property** to the **Properties** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6722e-105">構文</span><span class="sxs-lookup"><span data-stu-id="6722e-105">Syntax</span></span>

<span data-ttu-id="6722e-106">*式*。Append (***Object***)</span><span class="sxs-lookup"><span data-stu-id="6722e-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="6722e-107">\*式\***Properties**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="6722e-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6722e-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6722e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6722e-109">名前</span><span class="sxs-lookup"><span data-stu-id="6722e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6722e-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="6722e-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6722e-111">データ型</span><span class="sxs-lookup"><span data-stu-id="6722e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6722e-112">説明</span><span class="sxs-lookup"><span data-stu-id="6722e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6722e-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="6722e-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="6722e-114">必須</span><span class="sxs-lookup"><span data-stu-id="6722e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6722e-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="6722e-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="6722e-116">コレクションに追加するフィールドを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="6722e-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6722e-117">注釈</span><span class="sxs-lookup"><span data-stu-id="6722e-117">Remarks</span></span>

<span data-ttu-id="6722e-118">追加されたオブジェクトは、ディスクに格納され、**Delete** メソッドを使用して削除するまで持続します。</span><span class="sxs-lookup"><span data-stu-id="6722e-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="6722e-119">新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける場合は、そのコレクションの **Refresh** メソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6722e-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="6722e-p101">追加しようとしているオブジェクトが不完全である (たとえば、**Indexes** コレクションに追加する前に **Index** オブジェクトの **Fields** コレクションに **Field** オブジェクトが 1 つも追加されていない) 場合や、1 つ以上の従属オブジェクトのプロパティが正しく設定されていない場合、**Append** メソッドを使用すると、エラーが発生します。たとえば、フィールドの種類が指定されていないのに、**TableDef** オブジェクトの **Fields** コレクションに **Field** オブジェクトを追加しようとすると、**Append** メソッドで実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6722e-p101">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error. For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

